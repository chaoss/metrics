# {Name of Metric}

### This metric is a release candidate. To comment on this metric please see Issue [#[put the respective Issue Number here]](URL to issue). Following a comment period, this metric will be included in the next regular release.

Question: 

Synonyms: [Known synonyms for the metric - only common synonyms - this not meant to be a diffinitive list]

## Description
A description of what the metric is and what it captures.

## Objectives
Answer the question for why someone wants to measure this metric and what can be known with it. 

[Each metric has the potential to influence diversity, equity, and inclusion on an open source project. Please consider these factors when framing metrics objectives.] 

## Implementation
__The usage and dissemination of health metrics may lead to privacy violations. Organizations may be exposed to risks. These risks may flow from compliance with the GDPR in the EU, with state law in the US, or with other law. There may also be contractual risks flowing from terms of service for data providers such as GitHub and GitLab. The usage of metrics must be examined for risk and potential data ethics problems. Please see [CHAOSS Data Ethics document]() for additional guidance__ 

Provide details on how to measure the metric, collect the data, and analyze it. The following sub-headings are optional but help to structure the different aspects of implementation.

### Filters (optional)
Include a Filter

### Visualizations (optional)
Include visualizations such as screenshot of the metric. There may be many more visualizations for this metric, we only want to provide a flavor for what this metric is about.

Please provide attribution where the screenshot was taken, e.g. what software.

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

***This metric was last reviewed on [date] as part of [ release version ] [or recurring review process]***

--------
# Notes about document formatting
***The following rules are applicable for the above defined metric template:***
* Metrics naming - In cases where the metric name is also a descriptor, please use this convention:

"specific thing being measured"-"further description if needed"

EX: `pull-requests-open.md`
EX: `issues-first-response.md`

* Please provide attribution for where the image was taken, e.g. what software.
* All the images should be using the markdown syntax: `![]()`
* All the images should be using an absolute path to the images directory (Absolute paths are necessary, becuase these documents will be presented on a different platform/server).
    * Eg. `![alt text](https://github.com/chaoss/working-group/focus-area//images/metric-name_img.png)`
* No tables should be used in the metrics, alternatively you can insert an image of the table
* No HTML code should be used in the metrics, only markdown 
* Please remove formatting text and (Optional) tags from the metric prior to publishing
* There should be at least one `\n` (newline) between:
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
