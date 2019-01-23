# Contributor Diversity

## 1. Description
Ratio of contributors from a single company over all contributors.
Also described as: Maintainers from different companies. Diversity of contributor affiliation.

The SQL queries below provide a total number of organizations or companies in relation to pull requests.  If pull requests are not the best indicator of contributions, the queries can be modified to match the most helpful definition of contributions.  Queries are for the GHTorrent database.

Another option for contributor diversity is percentage of the repository written by an organization.  Code for this is under development and is not fully tested.  In progress example code may be found [here](https://github.com/OSSHealth/ghdata/blob/dev/organizationHistory/pythonBlameHistoryTree.py).  This code uses Git Blame and the GHTorrent database for its data sources.

## 2. Use Cases

## 3. Sample Filter and Visualization

## 4. Sample Implementations

###  GHTorrent: Total number of organizations by project making pull requests (approved or not):

```SQ:
SELECT count(distinct org_id) as num_organizations, projects.name as project_name, url
FROM
	organization_members
    join users on organization_members.user_id = users.id
    join pull_request_history on pull_request_history.actor_id = users.id
    join pull_requests on pull_request_history.pull_request_id = pull_requests.id
    join projects on pull_requests.base_repo_id = projects.id
WHERE pull_request_history.action = 'opened'
group by projects.id
```

###  GHTorrent: Alternately, using the "company" field in the users table instead of the organization:

```SQL
SELECT count(distinct company) as num_companies, projects.name as project_name, url
FROM
    users
    join pull_request_history on pull_request_history.actor_id = users.id
    join pull_requests on pull_request_history.pull_request_id = pull_requests.id
    join projects on pull_requests.base_repo_id = projects.id
WHERE pull_request_history.action = 'opened'
GROUP BY projects.id
```

###  GHTorrent: Number of organizations by project making pull requests that are approved:

```SQL
SELECT count(distinct org_id) as num_organizations, projects.name as project_name, url
FROM
	organization_members
    join users on organization_members.user_id = users.id
    join pull_request_history on pull_request_history.actor_id = users.id
    join pull_requests on pull_request_history.pull_request_id = pull_requests.id
    join projects on pull_requests.base_repo_id = projects.id
WHERE pull_request_history.action = 'opened'
	AND pull_requests.id in
    (SELECT pull_request_id
		from pull_request_history
	where action = 'merged')
group by projects.id
```

## 5. Known Implementations

## 6. External References (Literature)
