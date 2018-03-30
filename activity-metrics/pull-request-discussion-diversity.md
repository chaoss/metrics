# Pull Request Discussion Diversity

## 1. Description
Number of different people discussing each pull request

## 2. Use Cases

## 3. Sample Filter and Visualization

## 4. Sample Implementation

### GHTorrent: Average unique users commenting per pull request by project

```SQL
select avg(num_users) as average_num_users_commenting_per_pull_request, project_name, url
from
    (
    select projects.id as project_id, projects.name as project_name,
    projects.url as url, pull_requests.id as pull_request_id,
    count(distinct users.id) as num_users
    from pull_request_comments
    join pull_requests on pull_requests.id = pull_request_comments.pull_request_id
    join projects on projects.id = pull_requests.base_repo_id
    join users on pull_request_comments.user_id = users.id
    group by projects.id, pull_requests.id
    ) as user_count
group by project_id
```

## 5. Known Implementations

## 6. External References (Literature)
