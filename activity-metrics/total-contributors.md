# Total Contributors 

## 1. Description
The total number of contributors over time on any platform.

## 2. Use Cases

## 3. Sample Visualization
![Total Contributors visual](https://user-images.githubusercontent.com/22136995/38274804-6583433a-3755-11e8-9871-0de4c300a2ff.png)

## 4. Sample Implementations
### Kibble - GitHub
First, it grabs all the committers for one or multiple projects.
```
if not committer_email in people or len(people[committer_email]['name']) < len(commiter_name):
    people[commiter_email] = people[commiter_email] if committer_email in people else {'projects': [git_repo_name]}
    people[committer_email]['name'] = committer_name
    if not git_repo_name in people[commiter_email]['projects']:
        people[commiter_email]['projects'].append(git_repo_name)

```
Then, it ignores the committers as those are already accounted for and collects all the authors. 
```
if not author_email in people or len(people[author_email]['name']) < len(author_name):
    people[author_email] = people[author_email] if author_email in people else {'projects': [git_repo_name]}
    people[author_email]['name'] = author_name
    if not git_repo_name in people[author_email]['projects']:
        people[author_email]['projects'].append(git_repo_name)
```

## 5. Known Implementations

[Kibble](https://kibble.apache.org/)

## 6. External References (Literature)
