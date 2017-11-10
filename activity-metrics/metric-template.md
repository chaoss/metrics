# Template for Metric
The following is a draft for the template that all 'Metric Detail' pages can follow.

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

## 1. Description
A description of what the metric is and what it captures.
The first few sentences have to match the description in the [metrics list](../activity-metrics-list.md).

## 2. Use Cases
Provide examples of how the metric might inform different stakeholders through use cases.

## 3. Sample Visualization
Include a sample visualization (screenshot) of the metric from any implementation.

## 4. Sample Implementation
A generic calculation (code) or SQL query that generates the metric.

## 5. Known Implementations
Examples of where and how metric is used. (include links to dashboard or location where metric is visible or is talked about having been used).

## 6. External References (Literature)
Blog posts, websites, academic papers, or books that mention the metric.
```
