# Issue Comments

## 1. Description
Number of Comments per Issue

## 2. Use Cases

## 3. Sample Filter and Visualization

## 4. Sample Implementation

### Average Comments per Issue per Project

```SQL
SELECT avg(avg_num_comments), project_name
FROM
(
	SELECT count(comment_id) as avg_num_comments, projects.name as project_name, projects.id as project_id
	FROM msr14.issue_comments
		join issues on issue_comments.issue_id = issues.id
		join projects on issues.repo_id = projects.id
	GROUP BY projects.id, issues.id
) as comments_per_issue
GROUP BY project_id
```

### Number of Issue Comments Over Time

```SQL
SELECT projects.name as project_name, COUNT(issue_comments.comment_id), DATE(issue_comments.created_at) AS date_commented
FROM issue_comments
    JOIN issues ON issues.id = issue_comments.issue_id
    JOIN projects ON projects.id = issues.repo_id
    GROUP BY projects.id, date_commented
```

### Number of Comments per Issue

```SQL
SELECT projects.name as project_name, issue_comments.issue_id, COUNT(issue_comments.comment_id)
FROM issue_comments
    JOIN issues ON issues.id = issue_comments.issue_id
    JOIN projects ON projects.id = issues.repo_id
    GROUP BY issue_comments.issue_id
```

## 5. Known Implementations

## 6. External References (Literature)
