# Issue Response Rate

## 1. Description
Time between a new issue is opened and a maintainer responds
Also called: bug response rate. The maintainer is believed to not “pile on” but try to solve an issue.

Below queries are using users with commit rights, not maintainer.

## 2. Use Cases

## 3. Sample Filter and Visualization

## 4. Example Implementation
### GHTorrent: Average days an issue tagged with 'bug' exists until a project member comments (all projects)

```SQL
SELECT avg(time_to_member_comment_in_days) as avg_days_to_member_comment, project_name, url
FROM
(
	SELECT DATEDIFF(earliest_member_comment, issue_created) time_to_member_comment_in_days, project_id, issue_id, project_name, url
	FROM
		(SELECT projects.id as project_id,
				MIN(issue_comments.created_at) as earliest_member_comment,
				issues.created_at as issue_created,
				issues.id as issue_id, projects.name as project_name, url
		FROM msr14.repo_labels
			join projects on repo_labels.repo_id = projects.id
			join issue_labels on issue_labels.label_id = repo_labels.id
			join project_members on projects.id = project_members.repo_id
			join issues on issue_labels.issue_id = issues.id
			join issue_comments on issue_comments.issue_id = issues.id
		where repo_labels.name = 'bug'
			and issue_comments.user_id = project_members.user_id
		group by issues.id) as earliest_member_comments) as time_to_member_comment
group by project_id
```

### GHTorrent: Average days an issue (any tag or no tag) exists until a project member comments (all projects)

```SQL
SELECT avg(time_to_member_comment_in_days) as avg_days_to_member_comment, project_name, url
FROM
(
	SELECT DATEDIFF(earliest_member_comment, issue_created) time_to_member_comment_in_days, project_id, issue_id, project_name, url
	FROM
		(SELECT projects.id as project_id,
				MIN(issue_comments.created_at) as earliest_member_comment,
				issues.created_at as issue_created,
				issues.id as issue_id, projects.name as project_name, url
		FROM projects
			join project_members on projects.id = project_members.repo_id
			join issues on issues.repo_id = projects.id
			join issue_comments on issue_comments.issue_id = issues.id
		where issue_comments.user_id = project_members.user_id
		group by issues.id) as earliest_member_comments) as time_to_member_comment
group by project_id
```

### GHTorrent: Time between opening and a committer responding to an issue (single project)

```SQL
SELECT issues.id                       AS "issue_id",
       issues.created_at               AS "created_at",
       MIN(issue_comments.created_at)  AS "responded_to"
FROM issues
JOIN issue_comments
ON issue_comments.issue_id = issues.id
WHERE issue_comments.user_id IN
     (SELECT users.id
    FROM users
    JOIN commits
    WHERE commits.author_id = users.id
    AND commits.project_id = 78852)
AND issues.repo_id = 78852
GROUP BY issues.id
```

## 5. Known Implementations

[GHData](https://github.com/OSSHealth/ghdata)

## 6. External References (Literature)
