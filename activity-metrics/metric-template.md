# Template for Metrics
The following is the current template that all 'Metric Detail' pages follow.

## Instructions

To create a new 'Metric Detail' page follow these steps:

  - In the __[metrics list](../activity-metrics-list.md)__, convert the name of a metric into a link
    - The link looks like this: `__[Name of Metric](activity-metrics/name-of-metric.md)__`.
  - Copy the text below the horizontal bar into the new wiki page.
  - Remove explanations in all sections and leave sections empty if no information is available at the moment.
    - **Important:** Do not delete a section heading because we want all 'Metric Detail' pages to be structured the same.


----
```markdown
# {Name of Metric}

Question: 

## Description
A description of what the metric is and what it captures.
The first few sentences should match the description in the [metrics list](../activity-metrics-list.md).

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

### Success Metrics (optional)
If a metric could be expressed through different ways, this is the place to detail how to do it.

## References
Blog posts, websites, academic papers, or books that mention the metric and provide more background.
```
