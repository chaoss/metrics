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

## 3. Formula
A generic formula (in pseudo code) to generate the metric.

## 4. Sample Filter and Visualization
Include a Sample Filter and Visualization (screenshot) of the metric from any implementation.

## 5. Sample Implementation
An example implementation, for example a SQL or Elasticsearch query.

## 6. Known Implementations
Examples of where and how metric is used. (include links to dashboard or location where metric is visible or is talked about having been used).

## 7. Test Cases (Examples)
Sample inputs (including contexts) and expected outputs for this metric. Implementers can test their implementations against these test cases. For quantitative metrics, this could include a static repository with known metric results, or just inputs and output. For qualitative metrics, this may be more difficult.

## 8. External References (Literature)
Blog posts, websites, academic papers, or books that mention the metric.
```
