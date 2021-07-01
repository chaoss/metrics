# Template for Metric
The following is a draft for the template that all 'Metric Detail' pages can follow.

----
```markdown
# {Name of Metric}

### This metric is a release candidate. To comment on this metric please see Issue [#[put the respective Issue Number here]](URL to issue). Following a comment period, this metric will be included in the next regular release.

Question: _____

## Description
A description of what the metric is and what it captures.

## Objectives
Answer the question for why someone wants to measure this metric and what can be known with it.

## Implementation
Provide details on how to measure the metric, collect the data, and analyze it. The following sub-headings are optional but help to structure the different aspects of implementation.

### Filters (optional)
Include a Filter

### Visualizations (optional)
Include visualizations such as screenshot of the metric. There may be many more visualizations for this metric, we only want to provide a flavor for what this metric is about.

### Tools Providing the Metric (optional)
Metric must be currently deployed/available, in contrast to a tool having the "potential" to provide the metric. Provide direct link to implementation/documentation, if applicable

### Data Collection Strategies (Optional)
If there are several different ways to collect data for this metric, list them here. 
This may include expressing a metric in different ways.

## References
Blog posts, websites, academic papers, or books that mention the metric and provide more background.

## Contributors
List of people who would like to be mentioned as contributors to this metric 
```

In cases where the metric name is also a descriptor, please use this convention:

"specific thing being measured"-"further description if needed"

EX: `pull-requests-open.md`
EX: `issues-first-response.md`
