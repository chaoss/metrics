# Pull Request Comment Duration

## 1. Description
The difference between the timestamp of the pull request creation date and the most recent comment on the pull request.

## 2. Use Cases
To understand the dynamics of pull request discussion I want to know how long the comment period is on pull requests for a repository over time.

## 3. Formula
max(pull_request)comment.created_at) - pull_request.created_at

## 4. Sample Visualization
not implemented yet.

## 5. Sample Implementation
Note that the left join on pull_request_comments will show records for pull requests that do not have any comments associated with them. 
```sql
SELECT
	pull_request_history.id AS "pull_request_id" ,
	pull_requests.base_repo_id AS "repo_id" ,
	pull_request_history.created_at AS "pull_request_created_at" ,
	TIMESTAMPDIFF( MINUTE ,
	pull_request_history.created_at ,
	MIN( pull_request_comments.created_at )) AS "first_pr_comment" ,
	TIMESTAMPDIFF( MINUTE ,
	pull_request_history.created_at ,
	MAX( pull_request_comments.created_at )) AS "most_recent_pr_comment" ,
	count(*) AS "total_issue_pr_comments"
FROM
	pull_request_history
JOIN pull_requests ON pull_request_history.id = pull_requests.id
LEFT JOIN pull_request_comments ON pull_request_comments.pull_request_id = pull_request_history.id
WHERE
	pull_requests.base_repo_id = 1334
GROUP BY
	pull_request_history.id ,
	pull_requests.base_repo_id ,
	pull_request_history.created_at
ORDER BY
	pull_request_history.created_at
```

## 6. Known Implementations
GHData

## 7. Test Cases (Examples)
None to date.

## 8. External References (Literature)
None to date.
