# Contributor Demographics

## 1. Description
Gender, age, location, education, and skills over time.

## 2. Use Cases

## 3. Formula

## 4. Sample Filter and Visualization

## 5. Sample Implementation

### GHData (gender only)

```Python
def contributors_gender(self, owner, repo=None):
    contributors = self.__api.get_repo((owner + "/" + repo)).get_contributors()
    names = pd.DataFrame(columns=['name'])
    i = 0
    for contributor in contributors:
        if contributor.name is not None:
            names.loc[i] = [contributor.name.split()[0]]
            i += 1
    genderized = names.merge(LocalCSV.name_gender, how='inner', on=['name'])
    return genderized
```

## 6. Known Implementations

[GHData (gender only)](https://github.com/OSSHealth/ghdata/blob/master/ghdata/githubapi.py#L202)

## 7. Test Cases (Examples)

## 8. External References (Literature)
