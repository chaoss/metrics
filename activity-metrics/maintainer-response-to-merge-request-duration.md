# Time to First Maintainer Response to Merge Request

## 1. Description
How much time passes between the issuance of a merge request and the first response from a repository maintainer?

Candidate definition of a repository maintainer: A user who is responsible for either 2% of the commits OR 15% of the pull request comments (implemented in Augur)

How do we decide who a maintainer is? What is the signal in data? Commit rights? Active commit work? If a project is structured around pull requests is there a type of maintainer that can be referenced which does not have commit rights? 

Things to consider:
How do we deal with open merge requests with no comments by maintainers?
How do deal with closed merge requests with no comments by maintainers?

How do we want to show this metric?
Possible implementation: Mean (by week), Min (by week), Max (by week)

## 2. Use Cases
Provide examples of how the metric might inform different stakeholders through use cases.

## 3. Formula
A generic formula (in pseudo code) to generate the metric.

## 4. Sample Filter and Visualization
Include a Sample Filter and Visualization (screenshot) of the metric from any implementation.

## 5. Sample Implementation
An example implementation, for example a SQL or Elasticsearch query.

## 6. Known Implementations
[Augur](http://augurlabs.io/)

## 7. Test Cases (Examples)
Sample inputs (including contexts) and expected outputs for this metric. Implementers can test their implementations against these test cases. For quantitative metrics, this could include a static repository with known metric results, or just inputs and output. For qualitative metrics, this may be more difficult.

## 8. External References (Literature)
Blog posts, websites, academic papers, or books that mention the metric.
