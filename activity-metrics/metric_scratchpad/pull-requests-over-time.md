# Pull Requests Over Time

## 1. Description
How many pull requests have been submitted over a specified time period?

## 2. Use Cases
This metric will provide an easy to view graph of how many pull requests have been submitted to the project over time.
Stakeholders would be interested in this because a healthy community should show an increasing number of pull requests up to a point, then eventaully leveling out. An unhealthy
community would show a steadily (or sharply) decreasing amount of pull requests, showing a lack of interest/supoprt for the project.

## 3. Formula

### GrimoireLab
![img](https://github.com/Illuminatian/Assets/blob/master/PullRequestCode1.PNG)
![img](https://github.com/Illuminatian/Assets/blob/master/PullRequestCode2.PNG)

GrimoireLab takes the indexed grimoire_creation_date bucket as a date histogram over time, splits it byt the state of
the "Pull Request" metric (open/closed), and then aggregates it as "Count" giving a graphical split comparison of open/closed pull requests
over time
## 4. Sample Filter and Visualization

### GrimoireLab
![img](https://github.com/Illuminatian/Assets/blob/master/PullRequestsVis.PNG)

## 5. Sample Implementation


## 6. Known Implementations
[GrimoireLab](https://github.com/chaoss/grimoirelab)

## 7. Test Cases (Examples)


## 8. External References (Literature)

