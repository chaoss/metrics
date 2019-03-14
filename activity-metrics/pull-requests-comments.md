# Pull Request Comments

## 1. Description
Number of comments per pull request

## 2. Use Cases

## 3. Sample Filter and Visualization

## 4. Sample Implementation

###  GHTorrent
```SQL
select avg(num_comments), project_name, url
from
(
    (select count(pull_request_comments.comment_id) as num_comments, projects.id as project_id, projects.name as project_name, projects.url as url, pull_requests.id as pull_request_id
    from pull_request_comments
    join pull_requests on pull_requests.id = pull_request_comments.pull_request_id
    join projects on projects.id = pull_requests.base_repo_id
    group by projects.id, pull_requests.id) comment_nums
)
group by project_id
```

## 5. Known Implementations
[GHData](https://github.com/OSSHealth/ghdata)

## 6. External References (Literature)
