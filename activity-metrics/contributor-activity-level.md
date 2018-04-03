# Contributor Activity 

## 1. Description
Activity level of individual contributors.

## 2. Use Cases

## 3. Sample Visualization
### Kibble - GitHub
![Total Contributors visual](https://user-images.githubusercontent.com/22136995/38274799-60629e0a-3755-11e8-9327-ce7ff5b73853.png)

## 4. Sample Implementations
### Kibble
```
people = {}
for bucket in res['aggregations']['committers']['buckets']:
    email = bucket['key']
    count = bucket['doc_count']
    sha = hashlib.sha1( ("%s%s" % (dOrg, email)).encode('utf-8') ).hexdigest()
    if session.DB.ES.exists(index=session.DB.dbname,doc_type="person",id = sha):
        pres = session.DB.ES.get(
            index=session.DB.dbname,
            doc_type="person",
            id = sha
            )
        person = pres['_source']
        person['name'] = person.get('name', 'unknown')
        people[email] = person
        people[email]['gravatar'] = hashlib.md5(person.get('email', 'unknown').encode('utf-8')).hexdigest()
        people[email]['count'] = count
        people[email]['subcount'] = {
            'insertions': int(bucket['byinsertions']['buckets'][0]['stats']['value']),
            'deletions': int(bucket['bydeletions']['buckets'][0]['stats']['value'])
        }
```

## 5. Known Implementations

[Kibble](https://kibble.apache.org/)

## 6. External References (Literature)
