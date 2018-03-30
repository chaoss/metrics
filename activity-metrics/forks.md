# Forks

## 1. Description
Number of forks

## 2. Use Cases

## 3. Sample Filter and Visualization

## 4. Sample Implementation
### GHTorrent: Number of direct forks for each project that is not itself a fork (does not take into account forks of forks)

```SQL
select base_projects.base_project_id, base_projects.name as base_project_name,
base_projects.url as base_project_url, count(forks.id) as num_forks from
(select * from projects) as forks
right join
(select id as base_project_id, name, url from projects
where forked_from is null) as base_projects
on forks.forked_from = base_projects.base_project_id
group by base_projects.base_project_id
```

## 5. Known Implementations

[GHData](https://github.com/OSSHealth/ghdata)

## 6. External References (Literature)
