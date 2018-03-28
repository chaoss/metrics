# Pull Request made/closed

## 1. Description
Pull requests made vs. pull requests closed

[Example](http://repocheck.com/#https%3A%2F%2Fgithub.com%2Ftwbs%2Fbootstrap)

Encompasses number of pull requests rejected

## 2. Use Cases

## 3. Sample Filter and Visualization

## 4. Sample Implementation

###  GHTorrent: All pull requests that were created

```SQL
SELECT count(distinct pull_request_id) as num_opened, projects.name as project_name, projects.url as url
FROM msr14.pull_request_history
    join pull_requests on pull_request_history.pull_request_id = pull_requests.id
    join projects on pull_requests.base_repo_id = projects.id
where action = 'opened'
group by projects.id
```

###  GHTorrent: Pull Requests Closed

```SQL
SELECT count(distinct pull_request_id) as num_closed, projects.name as project_name, projects.url as url
FROM msr14.pull_request_history
    join pull_requests on pull_request_history.pull_request_id = pull_requests.id
    join projects on pull_requests.base_repo_id = projects.id
where action = 'closed'
group by projects.id
```

## 5. Known Implementations

## 6. External References (Literature)
