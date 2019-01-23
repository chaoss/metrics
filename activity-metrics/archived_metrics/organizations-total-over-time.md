# Contributing Organizations Total Over Time

## 1. Description
The total number of organizations contributing over time.

## 2. Use Cases
Identifies organizational support.

## 3. Formula

## 4. Sample Filter and Visualization

## 5. Sample Implementation

### GHTorrent

```SQL
SELECT id AS company, SUM(commits) AS commits, SUM(issues) AS issues,
                   SUM(commit_comments) AS commit_comments, SUM(issue_comments) AS issue_comments,
                   SUM(pull_requests) AS pull_requests, SUM(pull_request_comments) AS pull_request_comments,
      SUM(a.commits + a.issues + a.commit_comments + a.issue_comments + a.pull_requests + a.pull_request_comments) AS total
FROM
(
   (SELECT users.company AS id, COUNT(*) AS commits, 0 AS issues, 0 AS commit_comments, 0 AS issue_comments, 0 AS pull_requests, 0 AS pull_request_comments
   FROM commits INNER JOIN project_commits ON project_commits.commit_id = commits.id INNER JOIN users ON users.id = commits.committer_id WHERE project_commits.project_id = :repoid GROUP BY users.company)
   UNION ALL
   (SELECT reporter_id AS id, 0 AS commits, COUNT(*) AS issues, 0 AS commit_comments, 0 AS issue_comments, 0, 0 FROM issues WHERE issues.repo_id = :repoid GROUP BY issues.reporter_id)
   UNION ALL
   (SELECT commit_comments.user_id AS id, 0 AS commits, 0 AS commit_comments, COUNT(*) AS commit_comments, 0 AS issue_comments, 0 , 0 FROM commit_comments JOIN project_commits ON project_commits.commit_id = commit_comments.commit_id WHERE project_commits.project_id = :repoid GROUP BY commit_comments.user_id)
   UNION ALL
   (SELECT issue_comments.user_id AS id, 0 AS commits, 0 AS commit_comments, 0 AS issue_comments, COUNT(*) AS issue_comments, 0, 0 FROM issue_comments JOIN issues ON issue_comments.issue_id = issues.id WHERE issues.repo_id = :repoid GROUP BY issue_comments.user_id)
   UNION ALL
   (SELECT actor_id AS id, 0, 0, 0, 0, COUNT(*) AS pull_requests, 0 FROM pull_request_history JOIN pull_requests ON pull_requests.id = pull_request_history.id WHERE pull_request_history.action = 'opened' AND pull_requests.`base_repo_id` = 1334 GROUP BY actor_id)
   UNION ALL
   (SELECT user_id AS id, 0, 0, 0, 0, 0, COUNT(*) AS pull_request_comments FROM pull_request_comments JOIN pull_requests ON pull_requests.base_commit_id = pull_request_comments.commit_id WHERE pull_requests.base_repo_id = 1334 GROUP BY user_id)
) a
WHERE id IS NOT NULL
GROUP BY id
ORDER BY total DESC;
```

Relies on self declared organization affiliation.

## 6. Known Implementations

## 7. Test Cases (Examples)

## 8. External References (Literature)
