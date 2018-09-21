# Forks

## 1. Description
Number of forks

## 2. Use Cases

We have to distinguish two main use cases for Forks.

1) On GitHub, forks are used in the regular contribution workflow. A developer first needs to fork a repository, before being able to create pull requests. In this use case, forks indicate the level of engagement with developers. These developers belong to the same community and contribute back to the same repository.

2) From a community perspective, forks are the option to develop an alternative version of a software and to build a separate community. A forked community (e.g., LibreOffice forked OpenOffice.org, NextCloud forked OwnCloud) develops it own practices and often does not contribute back. Forks of communities can indicate disagreements over governance but more often are disagreements about the technical future of a project.

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
