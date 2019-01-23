# Code Base Size

## 1. Description
How many lines of code in a project repository has

## 2. Use Cases

## 3. Formula

## 4. Sample Filter and Visualization

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
## 6. Known Implementations

[Kibble](https://github.com/apache/kibble)

## 7. Test Cases (Examples)

## 8. External References (Literature)
