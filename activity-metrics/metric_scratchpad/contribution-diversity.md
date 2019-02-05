# Contribution Diversity

## 1. Description
Ratio of code committed by contributors other than original project initiator
Contributions are going up beyond the core team

## 2. Use Cases


## 3. Sample Filter and Visualization


## 4. Sample Implementation

### GHTorrent:

The assumption is that the first person to commit to a GitHub repository after it is created is the creator of the repository.

We need to figure out how many commits were made by that user.

```SQL
SELECT count(commits.id), projects.name, WEEK(commits.created_at)
FROM users
JOIN commits on users.id = commits.author_id
JOIN projects on projects.id = commits.project_id
WHERE (users.id, projects.id) IN
	(SELECT user_id, project_id FROM
    	(SELECT users.id as user_id, projects.id as project_id, min(commits.created_at)
	    FROM commits
	    JOIN projects on projects.id = commits.project_id
	    JOIN users on commits.author_id = users.id
	    WHERE commits.created_at > projects.created_at
	    group by projects.id) as earliest_committers)
GROUP BY projects.id, WEEK(commits.created_at)
```

Commits made by users other than that user:

```SQL
SELECT count(commits.id), projects.name, WEEK(commits.created_at)
FROM users
JOIN commits on users.id = commits.author_id
JOIN projects on projects.id = commits.project_id
WHERE (users.id, projects.id) NOT IN
    (SELECT user_id, project_id FROM
	    (SELECT users.id as user_id, projects.id as project_id, min(commits.created_at)
	    FROM commits
	    JOIN projects on projects.id = commits.project_id
	    JOIN users on commits.author_id = users.id
	    WHERE commits.created_at > projects.created_at
	    group by projects.id) as earliest_committers)
GROUP BY projects.id, WEEK(commits.created_at)
```

## 5. Known Implementations


## 6. External References (Literature)
