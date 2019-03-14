# Reopened Issues

## 1. Description
Rate of issues closed but discussion continues or issues that were closed and re-opened

## 2. Use Cases

## 3. Sample Filter and Visualization

## 4. Sample Implementation

###  GHTorrent: Reopened issues

#### Total closed issues by project

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

#### Reopened issues

```SQL
select count(distinct issues.id) as total_reopened_issues, projects.name as project_name
from
    issues join projects
    on issues.repo_id = projects.id
    join issue_events
    on issue_events.issue_id = issues.id
where issue_events.action = 'reopened'
group by projects.id
```

#### issues with comments after issue is closed:

```SQL
select count(distinct comment_issue_id) as num_issues_with_comments_after_closed, comment_project_name as project_name
from
    (select issues.id as comment_issue_id, projects.id as comment_project_id, issue_comments.created_at as comment_date, projects.name as comment_project_name
    from issue_comments
         join issues on issue_comments.issue_id = issues.id
         join projects on projects.id = issues.repo_id) as comment_issues
join
    (select issues.id as closed_issue_id, projects.id as closed_project_id, issue_events.created_at as closed_date
    from
         issues join projects
         on issues.repo_id = projects.id
         join issue_events
         on issue_events.issue_id = issues.id
    where issue_events.action = 'closed') as closed_issues
    on closed_issue_id = comment_issue_id AND comment_project_id = closed_project_id AND comment_date > closed_date
    group by comment_project_id
```

#### Issues with no comments after issue closed:

```SQL
select count(distinct issues.id) as num_issues_no_comments_after_close, projects.name as project_name
from
     issues join projects
     on issues.repo_id = projects.id
     join issue_events
     on issue_events.issue_id = issues.id
where issue_events.action = 'closed' AND (issues.id, projects.id)
    not in(
             select comment_issue_id, comment_project_id
         from
             (select issues.id as comment_issue_id, projects.id as comment_project_id, issue_comments.created_at as comment_date, projects.name as comment_project_name
             from issue_comments
                 join issues on issue_comments.issue_id = issues.id
                 join projects on projects.id = issues.repo_id) as comment_issues
             join
             (select issues.id as closed_issue_id, projects.id as closed_project_id, issue_events.created_at as closed_date
             from
                  issues join projects
                  on issues.repo_id = projects.id
                  join issue_events
                  on issue_events.issue_id = issues.id
             where issue_events.action = 'closed') as closed_issues
         on closed_issue_id = comment_issue_id AND comment_project_id = closed_project_id AND comment_date > closed_date)
 group by projects.id
```

## 5. Known Implementations

## 6. External References (Literature)
