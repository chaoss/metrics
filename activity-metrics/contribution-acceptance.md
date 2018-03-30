# Contribution Acceptance

## 1. Description
Ratio of contributions accepted vs. closed without acceptance

## 2. Use Cases

## 3. Sample Filter and Visualization

## 4. Sample Implementations

### GHTorrent: Pull Request Acceptance Rate (Merged over Opened)

```SQL
SELECT projects.name as project_name, DATE(date_created), CAST(num_approved AS DECIMAL)/CAST(num_open AS DECIMAL) AS approved_over_opened
FROM (SELECT COUNT(DISTINCT pull_request_id) AS num_approved, projects.name AS project_name, DATE(pull_request_history.created_at) AS accepted_on
    FROM pull_request_history
        JOIN pull_requests ON pull_request_history.pull_request_id = pull_requests.id
        JOIN projects ON pull_requests.base_repo_id = projects.id
    WHERE action = 'merged'
    GROUP BY projects.id, accepted_on) accepted
JOIN (SELECT count(distinct pull_request_id) AS num_open, projects.id as repo_id, DATE(pull_request_history.created_at) AS date_created
  FROM pull_request_history
      JOIN pull_requests ON pull_request_history.pull_request_id = pull_requests.id
      JOIN projects ON pull_requests.base_repo_id = projects.id
      WHERE pull_request_id IN
      (SELECT pull_request_id
      FROM pull_request_history
      WHERE ACTION = 'opened')
        GROUP BY projects.id, date_created) opened ON opened.date_created = accepted.accepted_on
 JOIN projects ON repo_id = projects.id
```

### GHTorrent: Pull Requests Accepted

Assume that a pull request with a history record of being 'merged' has been accepted

pull_request table includes both head_repo_id and base_repo_id
base repo is where the changes will go
head repo is where the changes are coming from
http://stackoverflow.com/questions/14034504/change-base-repo-for-github-pull-requests

Since we are talking about the approval of pull requests, I will choose the base repo since that is where the changes are going.

Note: some of these results look unusual, in that projects that I would believe would be very active have few approved pull requests.

Possibly these groups do not use pull requests as often and edit master directly?

```SQL
SELECT count(distinct pull_request_id) as num_approved, projects.name as project_name, projects.url as url
FROM msr14.pull_request_history
	join pull_requests on pull_request_history.pull_request_id = pull_requests.id
	join projects on pull_requests.base_repo_id = projects.id
where action = 'merged'
group by projects.id
```

### GHTorrent: Pull Requests Accepted Over Time
```SQL
SELECT COUNT(DISTINCT pull_request_id) AS num_approved, projects.name AS project_name, DATE(pull_request_history.created_at) AS accepted_on
FROM pull_request_history
    JOIN pull_requests ON pull_request_history.pull_request_id = pull_requests.id
    JOIN projects ON pull_requests.base_repo_id = projects.id
WHERE action = 'merged'
GROUP BY projects.id, accepted_on
```


### GHTorrent: Pull Requests Rejected

Assume that a pull request with a history record of being 'closed' but lacking one of being 'merged' has been rejected.

```SQL
SELECT count(distinct pull_request_id) as num_rejected, projects.name as project_name, projects.url as url
FROM msr14.pull_request_history
	join pull_requests on pull_request_history.pull_request_id = pull_requests.id
	join projects on pull_requests.base_repo_id = projects.id
where action = 'closed' AND pull_request_id not in
	(SELECT pull_request_id
	FROM msr14.pull_request_history
	where action = 'merged')
group by projects.id
```

## 5. Known Implementations

[GHData](https://github.com/OSSHealth/ghdata)

## 6. External References (Literature)
