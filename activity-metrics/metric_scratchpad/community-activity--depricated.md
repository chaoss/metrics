# Community Activity

## 1. Description
Community Activity is observable in the frequency of contributions. Contributions to a community include code commits, bug reports, issue comments, mailing list posts, wiki edits, conference call participation, responding to questions in chat, or even organizing user groups. To simplify the data collection, typically only a subset of contributions are aggregated.

The value of this metric is in observing changes over time.

## 2. Use Cases


## 3. Sample Filter and Visualization


## 4. Sample Implementation

### GHTorrent: Community Activity
```SQL
/*
Timeseries of all the contributions to a project, optionally limited to a specific user
:param repoid: The id of the project in the projects table.
:param userid: The id of user if you want to limit the contributions to a specific user.
:return: DataFrame with all of the contributions seperated by day.
*/
rawContributionsSQL =
    SELECT  DATE(coms.created_at) as "date",
            coms.count            as "commits",
            pulls.count           as "pull_requests",
            iss.count             as "issues",
            comcoms.count         as "commit_comments",
            pullscoms.count       as "pull_request_comments",
            isscoms.count         as "issue_comments",
            coms.count + pulls.count + iss.count + comcoms.count + pullscoms.count + isscoms.count as "total"
    FROM (SELECT created_at AS created_at, COUNT(*) AS count FROM commits INNER JOIN project_commits ON project_commits.commit_id = commits.id WHERE project_commits.project_id = :repoid[[ AND commits.author_id = :userid]] GROUP BY DATE(created_at)) coms
    LEFT JOIN (SELECT pull_request_history.created_at AS created_at, COUNT(*) AS count FROM pull_request_history JOIN pull_requests ON pull_requests.id = pull_request_history.pull_request_id WHERE pull_requests.base_repo_id = :repoid AND pull_request_history.action = 'merged'[[ AND pull_request_history.actor_id = :userid]] GROUP BY DATE(created_at)) AS pulls
    ON DATE(pulls.created_at) = DATE(coms.created_at)
    LEFT JOIN (SELECT issues.created_at AS created_at, COUNT(*) AS count FROM issues WHERE issues.repo_id = :repoid[[ AND issues.reporter_id = :userid]] GROUP BY DATE(created_at)) AS iss
    ON DATE(iss.created_at) = DATE(coms.created_at)
    LEFT JOIN (SELECT commit_comments.created_at AS created_at, COUNT(*) AS count FROM commit_comments JOIN project_commits ON project_commits.commit_id = commit_comments.commit_id WHERE project_commits.project_id = :repoid[[ AND commit_comments.user_id = :userid]] GROUP BY DATE(commit_comments.created_at)) AS comcoms
    ON DATE(comcoms.created_at) = DATE(coms.created_at)
    LEFT JOIN (SELECT pull_request_comments.created_at AS created_at, COUNT(*) AS count FROM pull_request_comments JOIN pull_requests ON pull_request_comments.pull_request_id = pull_requests.id WHERE pull_requests.base_repo_id = :repoid[[ AND pull_request_comments.user_id = :userid]] GROUP BY DATE(pull_request_comments.created_at)) AS pullscoms
    ON DATE(pullscoms.created_at) = DATE(coms.created_at)
    LEFT JOIN (SELECT issue_comments.created_at AS created_at, COUNT(*) AS count FROM issue_comments JOIN issues ON issue_comments.issue_id = issues.id WHERE issues.repo_id = :repoid[[ AND issue_comments.user_id = :userid]] GROUP BY DATE(issue_comments.created_at)) AS isscoms
    ON DATE(isscoms.created_at) = DATE(coms.created_at)
    ORDER BY DATE(coms.created_at)

```

## 5. Known Implementations


## 6. External References (Literature)
