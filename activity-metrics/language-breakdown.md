# Language Makeup

## 1. Description
The makeup of the project in terms of the amount of whitespace, comments, and code. 

## 2. Use Cases

## 3. Sample Visualization
### Kibble
![Language Makeup visual](https://user-images.githubusercontent.com/22136995/38279225-ea70651e-3764-11e8-87fa-a521c1bb1a45.png)
## 4. Example Implementation
### Kibble 

```
while (scroll_size > 0):
    for doc in res['hits']['hits']:
        updates = doc['_source']
        ts = updates['time'] #round(updates['time']/86400) * 86400
        if updates['time'] % 86400 != 0:
            continue
        tstmp[ts] = tstmp.get(ts, {})
        item = tstmp[ts]
        if breakdown:
            pass
        else:

            item['blanks'] = item.get('blanks', 0) + (updates['blank'] or 0)
            item['comments'] = item.get('comments', 0) + (updates['comments'] or 0)
            item['code'] = item.get('code', 0) + (updates['loc'] or 0)

    res = session.DB.ES.scroll(scroll_id = sid, scroll = '1m')
    sid = res['_scroll_id']
    scroll_size = len(res['hits']['hits'])
```

## 5. Known Implementations

[Kibble](https://kibble.apache.org/)

## 6. External References (Literature)
