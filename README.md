# CHAOSS Metrics

Welcome to the CHAOSS Metrics repository. CHAOSS Metrics repository captures metrics for assessing open source community health and sustainability. Such metrics are aimed at understanding project diversity & inclusion, growth-maturity-decline, risk, and value. For more information about the CHAOSS project go to our website at: https://chaoss.community/

## Goals of CHAOSS Metrics 

(1) Capturing metrics based on the work of community members who have participated at CHAOSS events, worked in the repo, and discussed through on email. We capture the metrics that people find meaningful to their particular contexts when understanding project health and sustatinability. In this, we work to represent metrics through concise definitions, known uses cases, sample visualizations, and sample implementations. The CHAOSS Metrics repository captures all potential metrics. It is the WGs that make these metrics meaningful, leading to our second goal. 

(2) Participating with the CHAOSS workgroups. Through thes workgroups, we consolidate metrics in meaningful ways and inform the metrics by questioning how to capture and deploy (or not) them:

[CHAOSS Diversity & Inclusion Workgroup](https://github.com/chaoss/wg_diversity_inclusion)

[CHAOSS Growth, Maturity, Decline Workgroup](https://github.com/chaoss/wg-gmd)

## Some Reasons to Assess Community Health

  * Risk Mitigation
  * Track Corporate Engagement
  * Identify Sustainable Projects
  * Identify Single Points of Failure
  * Avoid In-take of an Inactive Project
  * Identify Open Source Projects that Need Support
  * Assess Value Generated through Community and Engagement
  * Show that Active Community Management Bears Desired Results

## Some Issues To Look At

  * Project Maturity
  * Project Viability
  * Growth of Community
  * Momentum of Community
  * Diversity of Community
  * Timeliness of Maintainers
  * Attentiveness of Maintainers
  * Activity Level - Responsiveness
  * Distribution of Code Contributions
  * Vanity metrics (might have use in other cases, e.g. stars)
  * Ecosystem Health (upstream, downstream, and related projects)
  * Aggregate Project-tree Health (combined health metrics of all linked dependencies)

## Some Contexts to Consdider When Evaluating Health

  * Value Derivation
  * Style of Project
  * Project Comparison
  * Maturity of Project
  * Programming Language
  * Quality of Ecosystem
  * Community Composition

# Full List of Activity Metrics

The following is a full list of identified metrics. How the metrics live in practice is work that happens in the workgroups. 


|Name|Description|
|---|---|
|Accepted Code Contributions|Percentage of new contributor code versus total code over time.|
|Age of Community|Time since repository/organization was registered; or time since first release. "Results showed that the age of the project played a marginally significant role in attracting active users, but not developers. We attribute this differential effect of age on users and developers to the fact that age may be seen as an indicator of application maturity by users, and hence taken as a positive signal, whereas it may convey more ambiguous signals to developers." (Chengalur-Smith et al., 2010, p.674) (Grewal, Lilien, & Mallapragada, 2006).|
|All Licenses|List of licenses.|
|Apache Maturity Model| The [Apache Project Maturity Model](https://community.apache.org/apache-way/apache-project-maturity-model.html) provides guidelines for assessing the maturity of a project.|
|Availability of Add-on Products|Availability of 3rd party plug-ins, modules, utilities, etc. that provide additional functionality for the project's software.|
|Blogposts|Number of blogposts that mention the project.|
|Average Time of First Maintainer Response to Code Merge Request|The average amount of time it takes for a maintainer to make the first response to a code merge request.|
|Average Time of First Response to Issue|The average amount of time it takes for the first response to an issue.|
|Average Time of Open Issues|The average amount of time open issues have remained open.|
|Average Issue Resolution Time|The average amount of time it takes for issues to be closed.|
|Bug Age|Age of known bugs in issue tracker. Use label for determining bugs?|
|Bugs after Release|Number of bugs reported after a release.|
|[Bus Factor](activity-metrics/bus-factor.md)|The number of developers it would need to lose to destroy its progress. Alternatively: Number of companies that would have to stop support.|
|Change in Maintainer Number|Number of maintainers added/removed over time.|
|CII Best Practices Badge|The [CII Best Practices Badge Program](https://bestpractices.coreinfrastructure.org/) provide maturity self-certification: passing, silver, and gold.|
|[Closed Issues](activity-metrics/closed-issues.md) | What is the number of closed issues? |
|[Closed Issue Resolution Duration](activity-metrics/closed-issue-resolution-duration.md) | What is the duration of time for issues to be resolved?|
|[Code Commits](activity-metrics/code-commits.md)| What is the number of code commits?|
|[Code Merge Duration](activity-metrics/code-merge-duration.md) | What is the duration of time between code merge request and code commit?|
|Code Modularity|Modular code allows parallel development, which Linus Torvalds drove for Linux (OSLS Torvalds). (Baldwin & Clark, 2006).|
|[Code Review Efficiency](activity-metrics/code-review-efficiency.md) | What is the number of merged code changes/number of abandoned code change requests?|
|[Code Review Iteration](activity-metrics/code-review-iteration.md) | What is the number of iterations that occur before a merge request is accepted or declined?|
|[Code Reviews](activity-metrics/code-reviews.md) | What is the number of code reviews?|
|Commercial Offerings|Availability of commercial products or services based on the project.|
|Commit Bias|Acceptance rate (and time to acceptance) differences per gender, ethnicity, and relevant diversity characteristics.|
|[Community Activity](activity-metrics/community-activity.md)|Contribution Frequency. Contribution = commit, issue, comment, etc.).|
|[Contributing Organizations](activity-metrics/contributing-organizations.md) | What is the number of contributing organizations?|
|[Contribution Acceptance](activity-metrics/contribution-acceptance.md)|Ratio of contributions accepted vs. closed without acceptance.|
|Contribution Age|Time since last contribution. Contribution = commit, issue, comment, etc.).|
|[Contribution Diversity](activity-metrics/contribution-diversity.md)|Ratio of code committed by contributors other than original project initiator. Contributions going up beyond the core team.|
|[Contributor Activity](activity-metrics/contributor-activity-level.md)|Activity level of individual contributors.|
|[Contributor Breadth](activity-metrics/contributor-breadth.md)|Ratio of non-core committers (drive-by committers). Can indicate openness to outsiders.|
|[Contributor Demographics](activity-metrics/contributor-demographics.md)| Gender, age, location, education, and skills over time.|
|[Contributor Diversity](activity-metrics/contributor-diversity.md)| Ratio of contributors from a single company over all contributors. Also described as: Maintainers from different companies. Diversity of contributor affiliation.|
|Contributor Importance|Percentage of commits by individual contributors from identified organizations over time.|
|Contributor Seniority|For each active contributor, time since first contribution. Experienced contributors can provide value to the community, since they carry with them (in part) the history of the project.|
|[Contributors](activity-metrics/contributors.md)| What is the number of contributors?|
|Copyright Declaration|The degree to which the project properly declares copyright ownership, including the copyright symbol or 'copyright' word, the year of the creation, the name of the author, and a rights statement.|
|Decision Distribution|Central vs. distributed decision making. Governance model, scalability of community.|
|Dependency Depth|Number of projects included in code base + number of projects relying on focal project (recursive). Indicator about centrality in open source Dependency network.|
|Distribution of Work|How much recent activity is distributed?|
|Downloads of Non-software Artifacts|Number of downloads of non-software artifacts (e.g. documentation, sample apps, test suites, etc.).|
|Elephant Factor|If 50% of community members are employed by the same company, it is the elephant in the room. Formally: The minimum number of companies whose employees perform 50% of the commits|
|File License Declarations|A list of license declarations on the software package files.|
|[Followers](activity-metrics/followers.md)|Number of followers (GitHub).|
|[Forks](activity-metrics/forks.md)|Number of forks.|
|Gatherings|Number of face-to-face/in-person meetings per year. Resets contentious issues; Resolve tensions; Avoid longstanding grudges.|
|Installs|Number of software installations of the project.|
|[Issue Comments](activity-metrics/issue-comments.md)|Number of comments per issue.|
[Issue Resolution Efficiency](activity-metrics/issue-resolution-efficiency.md) | What is the number of closed issues/number of abandoned issues?
|[First Response to Issue Duration](activity-metrics/first-response-to-issue-duration.md)| Time between a new issue is opened and a maintainer responds. Also called: bug response rate. The maintainer is believed to not "pile on" but try to solve an issue.|
|[Issues submitted/closed](activity-metrics/issues-submitted-closed.md)|Issues submitted vs. issues closed. [Example](http://repocheck.com/#https%3A%2F%2Fgithub.com%2Ftwbs%2Fbootstrap).|
|Job Postings|Number of job postings that mention the project as a preferred or required skill.|
|Known Vulnerabilities|Number of reported vulnerabilities. Could be limited to issue-tracker or extended vulnerability databases (e.g. CVE).|
|Language Bias|Bias against gender, ethnicity, ... in use of language (maybe use sentiment analysis).|
|[Language Makeup](activity-metrics/language-makeup.md)|Makeup of a project in terms of whitepsace, code, and comments.|
|Leadership Demographics|Demographics of project's leadership (e.g. Board, Technical Steering Committee, Maintainers, etc.) over time.|
|License Conflicts|Project containing incompatible licenses.|
|License Count|Number of licenses.|
|License Coverage|Number of files with a file notice (copyright notice + license notice).|
|License Declared|What license does the project declare.|
|License Identification Methods|A list of methods or tools used for identifying licenses in files.|
|[Lines of Code Changed](activity-metrics/lines-of-code-changed.md) | What is the number of lines of code changed?|
|Maintainer Promotion|Last time a maintainer was added.|
|[Maintainer Response to Merge Request Duration](activity-metrics/maintainer-response-to-merge-request-duration.md) | What is the duration of time for a maintainer to make a first response to a code merge request?|
|[New Contributing Organizations](activity-metrics/new-contributing-organizations.md) | What is the number of new contributing organizations?|
|New Contributions|Percentage of contributions (patches, pull requests, etc.) from new contributors vs all accepted contributions over time.|
|New Contributor Organizations|New organizations contributing to the project over time.|
|[New Contributors](activity-metrics/new-contributors.md) | What is the number of new contributors?|
|New Contributors* vs Maintainers**|Ratio of new contributors to maintainers over time.|
|Non-Source Contributions|Track contributions like running tests in test environment, writing blog posts, producing videos, giving talks, etc...|
|Number of Active Users|Number of active users of the project.|
|Number of Contributing Organizations|Number of organizations participating in the project over time.|
|Onion Layers|Distance between onion model layers (users, contributors, committers, and steering committee). Rule of thumb: factor of 10x between layers. (OSLS'17 Node.js keynote).|
|[Open Issues](activity-metrics/open-issues.md)| What is the number of open issues?|
|[Open Issue Age](activity-metrics/open-issue-age.md) | What is the the age of open issues?|
|Package License Declaration|A list of license declarations on the software package.|
|Paid Developers|Number of paid developers in community over time.|
|Path to Leadership|A communicated path from lurker to contributor to maintainer. (or. track members: time from user to maintainer/leader). If active contributors are not included in leadership decisions they might lose interest and leave. (Focus on least likely contributor).|
|Path to Maintainership|Path to maintainership published.|
|[People Opening Issues](activity-metrics/people-opening-issues.md) | How many people are opening issues.|
|Project Life Cycle|Community assigned label. Some communities have a project life cycle for example: proposal, incubaton, active, deprecated, end of life (Source: [Hyperledger](https://wiki.hyperledger.org/community/project-lifecycle)).|
|Percentile Distribution of First Maintainer Response to Code Merge Request|The proportional frequency of time it takes for a maintainer to make the first response to a code merge request.|
|Percentile Distribution of First Response Time|The proportional frequency of time it takes for the first response to an issue.|
|Percentile Distribution of Issue Resolution Time|Proportional frequency of closed issue time duration.|
|Percentile Distribution of Open Issue Time|Proportional frequency of open issue time duration.|
|Percentile Distribution of Time to Merge Code|Proportional frequency of code merge to upstream time duration.|
|Pony Factor|The minimum number of developers performing 50% of the commits. [The Math](https://ke4qqq.wordpress.com/2015/02/08/pony-factor-math/)|
|[Pull Request Comments](activity-metrics/pull-request-comments.md)|Number of comments per pull request.|
|[Pull Request Comment Duration](activity-metrics/pull-requests-comment-duration.md)|The difference between the timestamp of the pull request creation date and the most recent comment on the pull request.|
|[Pull Request Discussion Diversity](activity-metrics/pull-request-discussion-diversity.md)|Number of different people discussing each pull request.|
|[Pull Request made/closed](activity-metrics/pull-requests-made-closed.md)|Pull requests made vs. pull requests closed [Example](http://repocheck.com/#https%3A%2F%2Fgithub.com%2Ftwbs%2Fbootstrap). Encompasses number of pull requests rejected.|
|[Pull Requests Open](activity-metrics/pull-requests-open.md)|Number of open pull requests. Perhaps more telling than total pull requests.|
|[Pull Requests Over Time](activity-metrics/pull-requests-over-time.md)|How many pull requests have been submitted over a specified time period?|
|Qualified Committers|Contributions over time and what components they commit to over time.|
|Relative Activity| Sum up the activities (GH issues+comments, GH pull requests+comments and GH commits) for the project members and for the non-project members, then  create a ratio of the two. Compare the activity between committers-as-a-group and contributors-as-a-group. It easily shows when a project is not yet popular, or when a project is not paying attention to its users. I also feel that a balance between the two groups is essential; ie) a project with a lot more contributor than committer activity is one that is failing to recruit committers quickly enough.|
|Release Maturity|Ratio of major and minor releases.|
|Release Note Completeness|Number of functionality changes and bug fixes represented in release notes vs. release. Good for users, also shows diligence of community.|
|Release Velocity|Time between releases. Regular releases are a reliability metric.|
|[Reopened Issues](activity-metrics/reopened-issues.md)|Rate of issues closed but discussion continues or issues that were closed and re-opened.|
|[Repository Size](activity-metrics/repository-size.md)|Overall size of the repository or number of commits.|
|Retrospectives|Existence of after release meetings. Collect lessons learned, improve processes, recognize contributors.|
|Review Efficiency|Number of merged patches / number of abandoned patches over a set period of time.|
|Rewards|Rewards, shout-outs, recognition, and mentions in pull-requests or change logs - might improve contribution levels.|
|Roadmap|Existence and quality of roadmap. Best practice as community engagement and scalability (might not be automatically computable).|
|Role Definitions|Existence and quality of role definitions. Governance related. Relates to "Path to Leadership".|
|[Size of Code Base](activity-metrics/size-of-code-base.md)|Lines of code.|
|Software Downloads|Number of project software downloads. Beware: downloads might be skewed by builders. Used as measure for success (Grewal, Lilien, & Mallapragada, 2006).|
|Stack Overflow|Several metrics: # of questions asked, response rate, number of responding people that have verified solutions.|
|Stars|Number of stars (GitHub).|
|[Sub-Projects](activity-metrics/sub-projects.md) | What is the number of sub-projects?|
|Test Coverage|Percentage of codebase covered by developer tests.|
|Time to Contributor|Time to becoming a contributor.|
|[Total Contributing Organizations](activity-metrics/total-contributing-organizations.md)|The total number of organizations contributing over time.|
|[Total Contributors](activity-metrics/total-contributors.md)|The total number of contributors over time on any platform.|
|Total New Contributing Organizations|The total number of new organizations contributing over time.|
|Total New Contributors|The total number of new contributors over time on any platform.|
|Total (Sub-)Projects|The total number of (sub)projects over time.|
|[Transparency](activity-metrics/transparency.md)|Number of comments per issue. Discussion is occuring openly - could also indicate level of agreement.|
|Unity|Rivalry or unity of community (sentiment analysis).|
|Update Age|Time since last update.|
|Update Rate|Number of updates over period x.|
|Update Regularity|How consistently and frequently are updates provided.|
|Use of Acronym|Frequency of acronyms used. Specialized language can be a barrier for new contributors.|
|User Dependency|Number of users who are aware that they depend on the software over time.|
|User Groups|Number of user groups that perform a variety of crucial marketing, service support, and business-development functions at the grassroots level\\ (Bagozzi & Dholakia, 2006)|
|V-index|An index of project's first-order and second-order downstream dependencies. For example: if a project has 15 downstream dependencies and those downstream projects have 15 downstream dependencies of their own, the V-index is 15.|
|Velocity|A graph where bubbles’ area is proportional to the number of authors, the y-axis (height) is the total number of pull requests & issues, and the x-axis is the number of commits. [Example](https://www.cncf.io/blog/2017/06/05/30-highest-velocity-open-source-projects/)|
|[Watchers](activity-metrics/watchers.md)|Number of watchers (GitHub).|
|YouTube Videos|Number of Youtube videos that mention or specifically deal with the project (e.g. tutorials).

## How to Contribute and Participate to the CHAOSS Project

[Contribute and Participate](https://chaoss.community/participate/). If you would like to propose a new metric to this repository, open a new issue and provide a pull request to open the discussion about inclusion. If you would like to provide metric details, we have a __[metric-template](activity-metrics/metric-template.md)__ to be used. Follow the same approach regarding an issue/pull request to have your detail changes discussed and potentially merged. 

## Repository Maintainers

- [Georg Link](https://github.com/GeorgLink)
- [Matt Germonprez](https://github.com/germonprez)
- [Ben Lloyd Pearson](https://github.com/BenLloydPearson)

[How to become a maintainer](.github/CONTRIBUTING.md#how-to-become-a-repository-maintainer)

# License

All contributions to implementation-agnostic metrics and standards, including associated scripts, SQL statements, and documentation, will be received and made available under the MIT License (https://opensource.org/licenses/MIT).
