# Watchers

## 1. Description
Number of watchers

## 2. Use Cases

## 3. Sample Filter and Visualization

## 4. Sample Implementation

###  GitHub: Project Watchers

```SQL
select count(user_id) as num_watchers, projects.name as project_name, url
from watchers
    join projects on watchers.repo_id = projects.id
group by projects.id
```

## 5. Known Implementations

## 6. External References (Literature)
