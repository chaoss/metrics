## 1. Description

These are the issues considered 'open' at some given point in time. The definition of 'open' differs from platform to platform and should be pre-defined.

Note: do not confuse this with the opened tickets in a specific period of time regardless their current status. The open issues metric is a snapshot while the opened issues one needs of a period of time.

### Parameters

Mandatory: 
* Point in time. This is the time for which the snapshot of the open issues is computed.
* Statuses. These are the statuses considered as open. Platform and project dependant.

### GitHub Case

* Platform: The platform provides only two statuses: *open* and *closed* tickets. 
* Case Definition: Open issues are defined as those with status *open*. In this case the definition of the statuses is not necessary.

### Bugzilla Case

* Platform: The platform provides several statuses and those depends on the configuration of each project. By default Bugzilla has a [workflow](https://www.bugzilla.org/docs/3.6/en/html/lifecycle.html) where the open statuses may be considered: all but *closed* and *resolved*.
* Case Definition: Open issues need the statuses parameter to be defined. By default this may be all statuses but *closed* and *resolved*. 

## 2. Use Cases

* Many people would like an at-a-glance visualization of all the open issues in a project, this visualization would provide that without having to look inside every sub-project in the repository and sum the issues manually
* First approach to measure the total effort to close all of the remaining open tickets.

 
 ## 3. Sample Filter and Visualization

![img](https://github.com/Illuminatian/Assets/blob/master/openIssues.PNG)
 ## 4. Sample Implementation

### GrimoireLab: Number of Open Issues 
![img](https://github.com/Illuminatian/Assets/blob/master/OpenIssuesCreate.PNG)

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
