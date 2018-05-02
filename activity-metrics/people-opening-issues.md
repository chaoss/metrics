# People Opening Issues 
## 1. Description
How many people are opening issues.

## 2. Use Cases

## 3. Formula

## 4. Sample Filter and Visualization

## 5. Sample Implementation

###  Kibble: People opening issues this period:

```python
        query = {
                'query': {
                    'bool': {
                        'must': [
                            {'range':
                                {
                                    'created': {
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
        query['query']['bool']['should'] = [{'term': {'issueCreator': indata.get('email')}}, {'term': {'issueCloser': indata.get('email')}}]
        query['query']['bool']['minimum_should_match'] = 1
    
    query['aggs'] = {
            'opener': {
                'cardinality': {
                    'field': 'issueCreator'
                }
            }
        }
```
	
## 6. Known Implementations

[Kibble](https://github.com/apache/kibble)

## 7. Test Cases (Examples)

## 8. External References (Literature)
