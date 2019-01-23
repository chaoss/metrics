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

###  Kibble: Commit trends:
```python
    query = {
                'query': {
                    'bool': {
                        'must': [
                            {'range':
                                {
                                    'tsday': {
                                        'from': dateFrom,
                                        'to': dateTo
                                    }
                                }
                            },
                            {
                                'term': {
                                    'organisation': dOrg
                                }
                            }
                        ]
                    }
                }
            }
    # Source-specific or view-specific??
    if indata.get('source'):
        query['query']['bool']['must'].append({'term': {'sourceID': indata.get('source')}})
    elif viewList:
        query['query']['bool']['must'].append({'terms': {'sourceID': viewList}})
    if indata.get('email'):
        query['query']['bool']['should'] = [{'term': {'committer_email': indata.get('email')}}, {'term': {'author_email': indata.get('email')}}]
        query['query']['bool']['minimum_should_match'] = 1
```
## 5. Known Implementations

[GHdata](https://github.com/OSSHealth/ghdata)

[Kibble](https://github.com/apache/kibble)

## 6. External References (Literature)
