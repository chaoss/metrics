# Repository Size
## 1. Description
Overall size of the repository or number of commits

## 2. Use Cases

## 3. Sample Filter and Visualization

## 4. Sample Implementation
###  GHTorrent: Total number of commits per project:

	select count(commits.id) as num_commits, projects.name as project_name, projects.url as url
	from commits
		join project_commits on commits.id = project_commits.project_id
		join projects on projects.id = project_commits.project_id
	group by projects.id

###  Git: Lines of code and documentation in a repository:
[Lines of Code](https://github.com/OSSHealth/ghdata/blob/dev/busFactor/pythonBlameLinesInRepo.py)


## 5. Known Implementations

[GHdata](https://github.com/OSSHealth/ghdata)

## 6. External References (Literature)
