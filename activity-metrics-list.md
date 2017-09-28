# List of Activity Metrics

We list and describe activity metrics. For different situations, the metrics have different meanings. Each activity metric can be used in association with other metrics in the creations of value-oriented health metrics. We have a __[template for the metrics](oss-health-metrics:metric-template)__ to be used for new detail metric pages.


|Name|Description|
|---|---|
|Age of Community|*Time since repository/organization was registered; or Time since first release.*\\ "Results showed that the age of the project played a marginally significant role in attracting active users, but not developers. We attribute this differential effect of age on users and developers to the fact that age may be seen as an indicator of application maturity by users, and hence taken as a positive signal, whereas it may convey more ambiguous signals to developers." (Chengalur-Smith et al., 2010, p.674) (Grewal, Lilien, & Mallapragada, 2006)|
|All Licenses|*List of licenses*|
|Apache Maturity Model| The [Apache Project Maturity Model](https://community.apache.org/apache-way/apache-project-maturity-model.html) provides guidelines for assessing the maturity of a project |
|Blogposts|*Number of blogposts that mention the project*|
|Bug Age|*Age of known bugs in issue tracker*\\ Use label for determining bugs?|
|Bugs after Release|*Number of bugs reported after a release*|
|Bus Factor|The number of developers it would need to lose to destroy its progress. Alternatively: Number of companies that would have to stop support.|
|CII Best Practices Badge|The [CII Best Practices Badge Program](https://bestpractices.coreinfrastructure.org/) provide maturity self-certification: passing, silver, and gold.|
|Code Modularity|Modular code allows parallel development, which Linus Torvalds drove for Linux (OSLS Torvalds)\\ (Baldwin & Clark, 2006)|
|Commit Bias|Diversity metric: acceptance rate (and time to acceptance) differences per gender, ethnicity, etc...|
|[Community Activity](activity-metrics/community-activity.md)|*Contribution Frequency*\\ (Contribution = commit, issue, comment, ...)|
|[Contribution Acceptance](activity-metrics/contribution-acceptance.md)|*Ratio of contributions accepted vs. closed without acceptance* |
|Contribution Age|*Time since last contribution*\\ Gives a sense of how active the community is. (Contribution = commit, issue, comment, ...)|
|[Contribution Diversity](activity-metrics/contribution-diversity.md)|*Ratio of code committed by contributors other than original project initiator*\\ Contributions are going up beyond the core team|
|Contributor Activity|Activity level of individual contributors|
|[Contributor Breadth](activity-metrics/contributor-breadth.md)|*Ratio of non-core committers (drive-by committers)*\\ Can indicate openess to outsiders|
|[Contributor Diversity](activity-metrics/contributor-diversity.md)| *Ratio of contributors from a single company over all contributors*\\ Also described as: Maintainers from different companies. Diversity of contributor affiliation.|
|Contributor Seniority|*For each active contributor, time since first contribution*\\ Experienced contributors can add some unique value to the community, since they carry with them (in part) the history of the project.|
|[Contributors](activity-metrics/contributors.md)|*Number of contributors* |
|Decision Distribution|*Central vs. distributed decision making*\\ Governance model, scalability of community|
|Dependency Depth|*Number of projects included in code base + number of projects relying on focal project (recursive)*\\ Indicator about centrality in open source Dependency network|
|Distribution of Work|How much recent activity is distributed?|
|Downloads|*Number of downloads*\\ ! beware: downloads might be skewed by builders\\ Used as measure for 'success' (Grewal, Lilien, & Mallapragada, 2006) |
|[Forks](activity-metrics/forks.md)|*Number of forks*|
|Gatherings|*Number of face-to-face/in-person meetings per year*\\ Resets contentious issues; Resolve tensions; Avoid longstanding grudges|
|[Issue Comments](activity-metrics/issue-comments.md)|*Number of Comments per Issue* |
|[Issue Response Rate](activity-metrics/issue-response-rate.md)| *Time between a new issue is opened and a maintainer responds*\\ Also called: bug response rate. The maintainer is believed to not "pile on" but try to solve an issue.|
|[Issues Open](activity-metrics/issues-open.md)|*Number of open issues* |
|[Issues submitted/closed](activity-metrics/issues-submitted-closed.md)|*Issues submitted vs. issues closed*\\ [Example](http://repocheck.com/#https%3A%2F%2Fgithub.com%2Ftwbs%2Fbootstrap)|
|Job Postings|*Number of job postings that mention the project as a preferred or required skill* |
|Known Vulnerabilities|*Number of reported vulnerabilities*\\ Could be limited to issue-tracker or extended vulnerability databases (e.g. CVE)|
|Language Bias|Diversity metric: Bias against gender, ethnicity, ... in use of language (maybe use sentiment analysis)|
|License Conflict|*Does the project contain incompatible licenses*|
|License Count|*Number of licenses*|
|License Coverage|*Number of files with a file notice (copyright notice + license notice)*|
|License Declared|*What license does the project declare*|
|Non-Source Contributions|Track contributions like running tests in test environment, writing blog posts, producing videos, giving talks, etc...|
|Onion Layers|*Distance between onion model layers (users, contributors, committers, and steering committee)*\\ Rule of thumb: factor of 10x between layers. (OSLS'17 Node.js keynote)|
|Path to Leadership|*A communicated path from lurker to contributor to maintainer. (or. track members: time from user to maintainer/leader)*\\ Rational: If active contributors are not included in leadership decisions they might lose interest and leave. (Focus on least likely contributor)|
|Project Life Cycle|*Community assigned label*\\ Some communities have a project life cycle for example: proposal, incubaton, active, deprecated, end of life (Source: [Hyperledger](https://wiki.hyperledger.org/community/project-lifecycle)).|
|[Pull Request Comments](activity-metrics/pull-request-comments.md)|*Number of comments per pull request* |
|[Pull Request Discussion Diversity](activity-metrics/pull-request-discussion-diversity.md)|*Number of different people discussing each pull request* |
|[Pull Request made/closed](activity-metrics/pull-requests-made-closed.md)|*Pull requests made vs. pull requests closed*\\ [Example](http://repocheck.com/#https%3A%2F%2Fgithub.com%2Ftwbs%2Fbootstrap)\\ Encompasses number of pull requests rejectet|
|[Pull Requests Open](activity-metrics/pull-requests-open.md)|*Number of open pull requests*\\ Might be more telling than total pull requests|
|Relative Activity| * I sum up the activities (GH issues+comments, GH pull requests+comments and GH commits) for the project members and for the non-project members, then I create a ratio of the two.*\\ Compare the activity between committers-as-a-group and contributors-as-a-group. It easily shows when a project is not yet popular, or when a project is not paying attention to its users. I also feel that a balance between the two groups is essential; ie) a project with a lot more contributor than committer activity is one that is failing to 'recruit' committers quickly enough. |
|Release Maturity|*Ratio of major and minor releases*|
|Release Note Completeness|*Number of functionality changes and bug fixes represented in release notes vs. release.*\\ Good for users, also shows diligence of community|
|Release Velocity|*Time between releases*\\ Regular releases are a reliability metric|
|[Reopened issues](activity-metrics/reopened-issues.md)|*Rate of issues closed but discussion continues or issues that were closed and re-opened* |
|[Repository Size](activity-metrics/repository-size.md)|Overall size of the repository or number of commits|
|Retrospectives|*Existence of after release meetings*\\ Collect lessons learned, improve processes, recognize contributors|
|Rewards|Rewards, shout-outs, recognition, and mentions in pull-requests or change logs - might improve contribution levels|
|Roadmap|*Existence and quality of roadmap*\\ Best Practice: community engagement and scalability (might not be automatically computable)|
|Role Definitions|*Existence and quality of role definitions*\\ Governance related. Relates to "Path do Leadership"|
|[Size of Code Base](activity-metrics/size-of-code-base.md)|Lines of code|
|Stack Overflow|*Several metrics: # of questions asked, response rate, number of responding people that have verified solutions*|
|Stars|*Number of stars* (GitHub)|
|Test Coverage| |
|Time to Contributor|*Time to becoming a contributor*|
|[Transparency](activity-metrics/transparency.md)|*Number of comments per issue*\\ Discussion is occuring openly - could also indicate level of agreement|
|Unity|Rivalry or unity of community (sentiment analysis?)|
|Update Age|*Time since last update*|
|Update Rate|*Number of updates over period x*|
|Update Regularity|How consistently and frequently are updates provided.|
|Use of Acronym|*Frequency of acronyms used*\\ Specialized language can be a barrier for new contributors.|
|User Groups|user groups perform a variety of crucial marketing, service support, and business-development functions at the grassroots level\\ (Bagozzi & Dholakia, 2006)|
|[Watchers](activity-metrics/watchers.md)|*Number of watchers* (GitHub)|
|YouTube Videos|*Number of Youtube videos that mention or specifically deal with the project (e.g. tutorials)*|

# Additional Thoughts
The following section are a collection of random thoughts that might be helpful in a future discussion.

## Reasons why community health is assessed

This includes reasons why metrics are considered for other reasons This section collects notes on what possible goals might be.

  * Track Corporate Engagement (is an organization creating value, are organizational goals met, employee contributions)
  * Risk mitigation
  * Identify open source projects that need support.
  * Identify single points of failure (and hopefully prevent them)
  * Assess value generated through community and engagement
  * Show that active community management bears desired results. (Measurable outcomes)
  * Avoid in-take of an inactive project, because it makes it difficult to maintain and might carry unknown bugs and security issues.
  * Sustainability: "we define a sustainable project as one that exhibits software development and maintenance activity over the long run." (Chengalur-Smith, Sidorova, & Daniel, 2010, p.660)

## Broad categories of indicators that we hear often

These categories are meta-concepts that cannot be assessed with a single metric and the combination of metrics will be different depending on the context.

  * Growth of community
  * Momentum of community
  * Timeliness of maintainers
  * Diversity of community, contributions, and in code base
  * Distribution of code contributions (beyond project creator)
  * Activity level - Responsiveness
  * Viability (e.g. Bus Factor - individual contributors and clustered by employer)
  * Maturity
  * Ecosystem health (upstream, downstream, and related projects)
  * Vanity metrics (might have use in other cases, e.g. stars)
  * Aggregate project-tree health (combined health metrics of all linked dependencies)
  * Attentiveness of maintainers to users. See [Mailing list](https://lists.linuxfoundation.org/pipermail/oss-health-metrics/2017-March/000007.html.md)

## Context: Considerations when evaluating health

  * Style of project
  * Programming language
  * Maturity of project (Projects might seem inactive but rather have fulfilled their goal and community remains responsive to bug reports and security issues, just no new features)
  * Quality of Ecosystem (metrics of related projects)
  * Value driven metrics (not just activity)
  * Development of metrics over time
  * External users might not be a homogenous group - consider different metrics
  * Compare similar projects (manually determine which projects to compare)
  * Classifications (based on a set of metrics, which projects 'behave' similar)
  * Interrelationships between categories of indicators (maturity might be high while activity low and response rate is up)
  * Aggregate from repository, to project, to community, (to company)

## Other classifications for indicators

We have heard other classifications that we simply list here.

Ideas for these classifications is to
1. generate a uniform classification and through conversations merge the different classifications.
2. create mappings of the indicators to the different classifications

  * Community/Code/Risk
  * Activity/Viability/Risk

## References

* Arantes, F. L., & Freire, F. M. P. (2011). Aspects of an open source software sustainable life cycle. In IFIP International Conference on Open Source Systems (pp. 325–329). Springer. Retrieved from http://link.springer.com/chapter/10.1007/978-3-642-24418-6_26

* Bagozzi, R. P., & Dholakia, U. M. (2006). Open Source Software User Communities: A Study of Participation in Linux User Groups. Management Science, 52(7), 1099–1115. Retrieved from http://www.jstor.org/stable/20110583

* Baldwin, C. Y., & Clark, K. B. (2006). The Architecture of Participation: Does Code Architecture Mitigate Free Riding in the Open Source Development Model? Management Science, 52(7), 1116–1127. Retrieved from http://www.jstor.org/stable/20110584

* Chengalur-Smith, I., Sidorova, A., & Daniel, S. (2010). Sustainability of Free/Libre Open Source Projects: A Longitudinal Study. Journal of the Association for Information Systems, 11(11). Retrieved from http://aisel.aisnet.org/jais/vol11/iss11/5

* Cosentino, V., Izquierdo, J. L. C., & Cabot, J. (2015). Assessing the bus factor of Git repositories. In 2015 IEEE 22nd International Conference on Software Analysis, Evolution, and Reengineering (SANER) (pp. 499–503). https://doi.org/10.1109/SANER.2015.7081864

* Crowston, K., Howison, J., & Annabi, H. (2006). Information systems success in free and open source software development: theory and measures. Software Process: Improvement and Practice, 11(2), 123–148. https://doi.org/10.1002/spip.259

* Grewal, R., Lilien, G. L., & Mallapragada, G. (2006). Location, Location, Location: How Network Embeddedness Affects Project Success in Open Source Systems. Management Science, 52(7), 1043–1056. Retrieved from http://www.jstor.org/stable/20110579

* Jansen, S. (2014). Measuring the health of open source software ecosystems: Beyond the scope of project health. Information and Software Technology, 56(11), 1508–1519.Retrieved from http://www.sciencedirect.com/science/article/pii/S0950584914000871

* Schweik, C. M., & English, R. C. (2012). Internet success: a study of open-source software commons. Cambridge, Mass.: MIT Press.
