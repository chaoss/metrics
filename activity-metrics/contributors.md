# Contributors

##  1. Description
Number of contributors

##  2. Use Cases

##  3. Sample Filter and Visualization

##  4. Sample Implementation

### GHTorrent: Contributions by user

```SQL
# Gets the count of types of contributions by user, only returning users who have interacted with a project in some way
SET @owner = "rails";
SET @repo  = "rails";
USE msr14; # Test database
# USE ghtorrent; # Production database
SET @proj = (SELECT projects.id FROM projects INNER JOIN users ON projects.owner_id = users.id WHERE projects.name = @repo AND users.login = @owner);
SELECT * FROM
   (
   SELECT       users.id        as "user_id",
            users.login     as "login",
            com.count       as "commits",
            pulls.count     as "pull_requests",
            iss.count       as "issues",
            comcoms.count   as "commit_comments",
            pullscoms.count as "pull_request_comments",
            isscoms.count   as "issue_comments"
   FROM users
   LEFT JOIN (SELECT committer_id AS id, COUNT(*) AS count FROM commits INNER JOIN project_commits ON project_commits.commit_id = commits.id WHERE project_commits.project_id = @proj GROUP BY commits.committer_id) AS com
   ON com.id = users.id
   LEFT JOIN (SELECT pull_request_history.actor_id AS id, COUNT(*) AS count FROM pull_request_history JOIN pull_requests ON pull_requests.id = pull_request_history.pull_request_id WHERE pull_requests.base_repo_id = @proj AND pull_request_history.action = 'merged' GROUP BY pull_request_history.actor_id) AS pulls
ON pulls.id = users.id
   LEFT JOIN (SELECT reporter_id AS id, COUNT(*) AS count FROM issues WHERE issues.repo_id = @proj GROUP BY issues.reporter_id) AS iss
ON iss.id = users.id
   LEFT JOIN (SELECT commit_comments.user_id AS id, COUNT(*) AS count FROM commit_comments JOIN project_commits ON project_commits.commit_id = commit_comments.commit_id WHERE project_commits.project_id = @proj GROUP BY commit_comments.user_id) AS comcoms
ON comcoms.id = users.id
   LEFT JOIN (SELECT pull_request_comments.user_id AS id, COUNT(*) AS count FROM pull_request_comments JOIN pull_requests ON pull_request_comments.pull_request_id = pull_requests.id WHERE pull_requests.base_repo_id = @proj GROUP BY pull_request_comments.user_id) AS pullscoms
ON pullscoms.id = users.id
   LEFT JOIN (SELECT issue_comments.user_id AS id, COUNT(*) AS count FROM issue_comments JOIN issues ON issue_comments.issue_id = issues.id WHERE issues.repo_id = @proj GROUP BY issue_comments.user_id) AS isscoms
ON isscoms.id = users.id
   GROUP BY users.id
   ORDER BY com.count DESC
   ) user_activity
WHERE commits IS NOT NULL
OR    pull_requests IS NOT NULL
OR    issues IS NOT NULL
OR    commit_comments IS NOT NULL
OR    pull_request_comments IS NOT NULL
OR    issue_comments IS NOT NULL;
```

### GHTorrent: Number of Contributors (committers) per Project:

GitHub defines contributors as those who have made "Contributions to master, excluding merge commits"

I do not see in the GHTorrent database schema a way to determine commits to master vs other branches,
Nor a way to differentiate merge commits from other commits.

Because of this, for the following SQL query I will define contributors as "users who have made a commit"

When viewing the table, one may notice that there is a separate author_id and committer_id for each commit
the commit author has written the code of the commit.
the commit committer has made the commit
example: author writes some code and does a pull request.  committer approves/merges the pull request

For the following SQL, I am considering the author to be the contributor.

```SQL
select projects.name as project_name, projects.url as url, count(distinct commits.author_id) as num_contributers
from commits
join project_commits on commits.id = project_commits.commit_id
join projects on projects.id = project_commits.project_id
group by project_commits.project_id
```

##  5. Known Implementations
[GHData](https://github.com/OSSHealth/ghdata)

##  6. External References (Literature)
