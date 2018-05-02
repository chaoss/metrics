# Total Contributors 

## 1. Description
The total number of contributors over time on any platform.

## 2. Use Cases

## 3. Formula

## 4. Sample Filter and Visualization
### GHData
Shows a line graph of the number of contributers by month

### Kibble - GitHub
![Total Contributors visual](https://user-images.githubusercontent.com/22136995/38274804-6583433a-3755-11e8-9871-0de4c300a2ff.png)

## 5. Sample Implementations
### Kibble - GitHub
First, it grabs all the committers for one or multiple projects.
```python
if not committer_email in people or len(people[committer_email]['name']) < len(commiter_name):
    people[commiter_email] = people[commiter_email] if committer_email in people else {'projects': [git_repo_name]}
    people[committer_email]['name'] = committer_name
    if not git_repo_name in people[commiter_email]['projects']:
        people[commiter_email]['projects'].append(git_repo_name)

```
Then, it ignores the committers as those are already accounted for and collects all the authors. 
```python
if not author_email in people or len(people[author_email]['name']) < len(author_name):
    people[author_email] = people[author_email] if author_email in people else {'projects': [git_repo_name]}
    people[author_email]['name'] = author_name
    if not git_repo_name in people[author_email]['projects']:
        people[author_email]['projects'].append(git_repo_name)
```

### [GHTorrent](http://ghtorrent.org/relational.html)

```SQL
SELECT total_committers.created_at AS "date", MAX(@number_of_committers:=@number_of_committers+1) total_total_committers
FROM (
    SELECT author_id, MIN(DATE(created_at)) created_at
    FROM commits
    WHERE project_id = :repoid
    GROUP BY author_id
    ORDER BY created_at ASC) AS total_committers,
(SELECT @number_of_committers:= 0) AS number_of_committers
GROUP BY DATE(total_committers.created_at)
```

## 6. Known Implementations
- [Kibble](https://kibble.apache.org/)
- [GHData](https://github.com/OSSHealth/ghdata)

## 7. Test Cases (Examples)

## 8. External References (Literature)
