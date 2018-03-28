# Pull Requests Open

## 1. Description
Number of open pull requests

Might be more telling than total pull requests

## 2. Use Cases

## 3. Sample Filter and Visualization

## 4. Sample Implementation

###  GHTorrent

```SQL
SELECT count(distinct pull_request_id) as num_still_open, projects.name as project_name, projects.url as url
FROM msr14.pull_request_history
    join pull_requests on pull_request_history.pull_request_id = pull_requests.id
    join projects on pull_requests.base_repo_id = projects.id
where pull_request_id not in
    (SELECT pull_request_id
    FROM msr14.pull_request_history
    where action = 'closed')
group by projects.id
```

## 5. Known Implementations

## 6. External References (Literature)
