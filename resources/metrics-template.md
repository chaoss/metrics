# Template for Metric
The following is a draft for the template that all 'Metric Detail' pages can follow.

**Each metric has the potential to influence diversity, equity, and inclusion on an open source project. Please consider these factors when writing metric definitions, and framing metrics objectives**. More specific guidance will be emerging through Fall, 2021. 

----
```markdown
# {Name of Metric}

### This metric is a release candidate. To comment on this metric please see Issue [#[put the respective Issue Number here]](URL to issue). Following a comment period, this metric will be included in the next regular release.

Question: _____

## Description
A description of what the metric is and what it captures.

## Objectives
Answer the question for why someone wants to measure this metric and what can be known with it. This can include a brief description of how the metric could be used to help better understand issues of diversity, equity, and/or inclusion.

## Implementation
Provide details on how to measure the metric, collect the data, and analyze it. The following sub-headings are optional but help to structure the different aspects of implementation.

The CHAOSS project recognizes that there are ethical and legal challenges when using the metrics and software provided by the CHAOSS community. Ethical challenges exist around protecting community members and empowering them with their personal information. Legal challenges exist around GDPR and similar laws or regulations that protect personal information of community members. Particular challenges may arise in the use that is specific to your context.

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


The following rules are applicable for the above defined metric template:
* All the images should be using the markdown syntax: `![]()`
* All the images should be using a relative path to the images directory
    * Eg. `![alt text](images/metric-name_img.png)`
* No tables should be used in the metrics, alternatively you can insert an image of the table
* No HTML code should be used in the metrics, only markdown in preferred
* There should be atleast one `\n` (newline) between:
    * 2 images
    * An image and text
    * An image and heading \
This is to solve the wrapping issue in the release PDF \
Eg. -
    ```
    # Some heading

    ![alt text](images/metric-name_test-img1.png)

    ![alt text](images/metric-name_test-img2.png)

    * Some random text

    ![alt text](images/metric-name_test-img3.png)

    Another text line
    ```
