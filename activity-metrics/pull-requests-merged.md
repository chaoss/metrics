# Merged Pull Requests

## 1. Description
What is the number of merged pull requests?

What constitutes a merged pull request?
	- does the code have to be merged into the "master" or "default" branch to be considered "merged"?
	- is there a difference between an "accepted" and "merged" pull request? Can we rigourously define a difference?
	- can we trust the version control hosting platform (i.e. GitHub, BitBucket, etc) to just tell us when a PR is merged?
		- similarly, what are the discrepancies in both the definition a of pull request and the definition of a "merged" pull request among these platforms, if they exist?
	- do merged intra-project (i.e. between branches) pull requests count? 

## 2. Use Cases

## 3. Formula

`number of merged pull requests` = `number of total pull requests` - `number of rejected pull requests` - `number of open pull requests`

## 4. Sample Filter and Visualization

## 5. Sample Implementation
Counting weekly pull requests merged into Ruby on Rails on GitHub, using GHTorrent:
```SQL
SELECT SUBDATE(DATE(created_at), WEEKDAY(DATE(created_at))) AS "date", count(*) as merged	
FROM pull_request_history
WHERE action = 'merged'
AND pull_request_id IN (SELECT id FROM pull_requests WHERE base_repo_id = 1334)
GROUP BY SUBDATE(DATE(created_at), WEEKDAY(DATE(created_at)))
```

## 6. Known Implementations

## 7. Test Cases (Examples)

## 8. External References (Literature)
