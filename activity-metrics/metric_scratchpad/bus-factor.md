# Bus Factor

## 1. Description
The minimum number of developers performing 50% of the commits.

## 2. Use Cases
Indicates the danger of the project losing key developers (higher bus factor is less likely to fail due to losing a developer).

## 3. Formula

## 4. Sample Filter and Visualization

### [Augur](https://github.com/OSSHealth/augur)

![Bus Factor visualization](https://user-images.githubusercontent.com/16946799/39537727-0992fcb6-4e00-11e8-81f0-14ea3e8f8998.PNG)

## 5. Sample Implementation

### [Augur](https://github.com/OSSHealth/augur)

```Python
def bus_factor(self, owner, repo, filename=None, start=None, end=None, threshold=50):
    """
    Calculates bus factor by adding up percentages from highest to lowest until they exceed threshold
    :param owner: repo owner username
    :param repo: repo name
    :param filename: optional; file or directory for function to run on
    :param start: optional; start time for analysis
    :param end: optional; end time for analysis
    :param threshold: Default 50;
    """

    if start != None:
        start = parse(start)
    else:
        start = github.GithubObject.NotSet

    if end != None:
        end = parse(end)
    else:
        end = github.GithubObject.NotSet

    commits = self.__api.get_repo((owner + "/" + repo)).get_commits(since=start, until=end)

    if filename != None:
        self.__api.get_repo((owner + "/" + repo)).get_contents(filename)

    df = []

    if filename != None:
        for commit in commits:
            for file in commit.files:
                if file.filename == filename:
                    try:
                        df.append({'userid': commit.author.id})
                    except AttributeError:
                        pass
                    break
    else:
        for commit in commits:
            try:
                df.append({'userid': commit.author.id})
            except AttributeError:
                pass

    df = pd.DataFrame(df)

    df = df.groupby(['userid']).userid.count() / df.groupby(['userid']).userid.count().sum() * 100

    i = 0
    for num in df.cumsum():
        i = i + 1
        if num >= threshold:
            worst = i
            break

    i = 0
    for num in df.sort_values(ascending=True).cumsum():
        i = i + 1
        if num >= threshold:
            best = i
            break

    bus_factor = [{'worst': worst, 'best' : best}]

    return pd.DataFrame(bus_factor)
```

## 6. Known Implementations
[Augur](https://github.com/OSSHealth/augur/blob/master/ghdata/githubapi.py#L22)

## 7. Test Cases (Examples)

## 8. External References (Literature)
[The Math](https://ke4qqq.wordpress.com/2015/02/08/pony-factor-math/)
