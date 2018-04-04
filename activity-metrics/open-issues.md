# Open Issues

## 1. Description
Number of open issues

## 2. Use Cases

## 3. Sample Filter and Visualization

## 4. Sample Implementation

### GHTorrent: Number of Open Issues (current)

```SQL
SELECT count(distinct issue_events.issue_id) as num_open_issues, projects.name as project_name, url as url
FROM msr14.issue_events
	join issues on issues.id = issue_events.issue_id
	join projects on issues.repo_id = projects.id
where issue_events.issue_id not in
	(SELECT issue_id FROM msr14.issue_events
	where action = 'closed')
group by projects.id
```

## 5. Known Implementations

## 6. External References (Literature)
