# Size of Code Base

## 1. Description
Lines of code

## 2. Use Cases

## 3. Sample Filter and Visualization

## 4. Sxample Implementation

### Git
[Lines in Repository](https://github.com/OSSHealth/ghdata/blob/master/busFactor/pythonBlameLinesInRepo.py)

###  Kibble: Repos by lines of code:
```python
    query = {
                'query': {
                    'bool': {
                        'must': [
                            {'terms':
                                {
                                    'type': ['git', 'svn', 'github']
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
```
## 5. Known Implementations

[Kibble](https://github.com/apache/kibble)

## 6. External References (Literature)
