# Transparency

## 1. Description
Number of comments per issue.
Discussion is occurring openly - could also indicate level of agreement.

## 2. Use Cases

## 3. Sample Filter and Visualization

## 4. Sample Implementation

###  GitHub

```SQL
SELECT avg(avg_num_comments), project_name
FROM
(
    SELECT count(comment_id) as avg_num_comments, projects.name as project_name, projects.id as project_id
    FROM msr14.issue_comments
    join issues on issue_comments.issue_id = issues.id
    join projects on issues.repo_id = projects.id
    GROUP BY projects.id, issues.id
) as comments_per_issue
GROUP BY project_id
```

## 5. Known Implementations

## 6. External References (Literature)
