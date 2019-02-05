# Contributor Breadth

## 1. Description
Contributor breadth is the ratio of non-core committers to core committers. This metric indicates how open a community is to contributions from outsiders. Drive-by committers (also known as one-time committers) do not build rapport with core committers but their contributions might be accepted based on their quality.

In the below queries, non-core committers are defined as committers who do not have commit rights.

## 2. Use Cases

## 3. Sample Filter and Visualization

## 4. Sample Implementation

### Commits from project members vs non-members
Project members have commit rights for the repo.

### GHTorrent: Number of Commits from Project Members

```SQL
	select count(commits.id) as num_member_commits, projects.name as project_name, projects.url as url
	from
	commits
	join projects on projects.id = commits.project_id
	join users on commits.author_id = users.id
	join project_members on project_members.repo_id = projects.id
	where project_members.user_id = commits.author_id
	group by projects.id
```

### GHTorrent: Number of Commits from non project members

```SQL
	select count(commits.id) as num_commits, projects.name as project_name, projects.url as url
	from
	commits
	join projects on commits.project_id = projects.id
	join users on users.id = commits.author_id
	where (projects.id, users.id) not in
		(select repo_id, user_id from project_members)
	group by projects.id
```

## 5. Known Implementations


## 6. External References (Literature)
