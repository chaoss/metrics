# Issues submitted/closed

## 1. Description
Issues submitted vs. issues closed

## 2. Use Cases

## 3. Sample Filter and Visualization

## 4. Sample Implementation

### GHTorrent: Total issues by project

```SQL
select count(issues.id) as total_issues, projects.name as project_name, projects.url as project_url
from issues
join projects on issues.repo_id = projects.id
group by projects.id
```

### GHTorrent: Total closed issues by project

```SQL
select count(distinct issues.id) as total_issues, projects.name as project_name, projects.url as project_url
from
issues join projects
on issues.repo_id = projects.id
join issue_events
on issue_events.issue_id = issues.id
where issue_events.action = 'closed'
group by projects.id
```

## 5. Known Implementations
[GHData](https://github.com/OSSHealth/ghdata}

## 6. External References (Literature)
