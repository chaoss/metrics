# CHAOSS Metrics

Welcome to the CHAOSS Metrics repository. CHAOSS Metrics repository captures metrics for assessing open source community health and sustainability. Such metrics are aimed at understanding project diversity & inclusion, growth-maturity-decline, risk, and value. For more information about the CHAOSS project go to our website at: https://chaoss.community/

## Goals of CHAOSS Metrics 

(1) Capturing metrics based on the work of community members who have participated at CHAOSS events, worked in the repo, and discussed through on email. We capture the metrics that people find meaningful to their particular contexts when understanding project health and sustainability. In this, we work to represent metrics through concise definitions, known uses cases, sample visualizations, and sample implementations. The CHAOSS Metrics repository captures all potential metrics. It is the WGs that make these metrics meaningful, leading to our second goal. 

(2) Participating with the CHAOSS workgroups. Through these workgroups, we consolidate metrics in meaningful ways and inform the metrics by questioning how to capture and deploy (or not) them:

[CHAOSS Common Metrics Working Group](https://github.com/chaoss/wg-common)

[CHAOSS Diversity & Inclusion Working Group](https://github.com/chaoss/wg_diversity_inclusion)

[CHAOSS Evolution Working Group](https://github.com/chaoss/wg-evolution)

[CHAOSS Value Working Group](https://github.com/chaoss/wg-value)

[CHAOSS Risk Working Group](https://github.com/chaoss/wg-risk)

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

## Some Contexts to Consider When Evaluating Health

  * Value Derivation
  * Style of Project
  * Project Comparison
  * Maturity of Project
  * Programming Language
  * Quality of Ecosystem
  * Community Composition

# Full List of Activity Metrics

The following is a full list of identified metrics. How the metrics live in practice is work that happens in the workgroups. 

**Please note that there is a folder called "metrics_scratchpad" underneath the activity-metrics folder. This directory is for metrics that are nascent ideas but have not been through our metric naming and classification process yet. We are trying to name all the metrics according to the types of data they characterize. For example, metrics related to "code" are prefixed with "code-", etc.**

|Name|Question/Description|Deployment in CHAOSS Workgroup|
|---|---|---|
|Accepted Code Contributions|Percentage of new contributor code versus total code over time.|
|Age of Community|Time since repository/organization was registered; or time since first release (Chengalur-Smith et al., 2010; Grewal, Lilien, & Mallapragada, 2006).|
|All Licenses|List of licenses.|
|[Alternatives](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/communication/communication-inclusivity-alternatives.md)|Are there a variety of communication channels?|D&I|
|Apache Maturity Model| The [Apache Project Maturity Model](https://community.apache.org/apache-way/apache-project-maturity-model.html) guidelines for assessing the maturity of a project.|
|[Attendees Demographics](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/events/attendee-demographics.md)|How diverse are the attendees?|D&I|
|Availability of Add-on Products|Availability of 3rd party plug-ins, modules, utilities, etc. that provide additional functionality for the project's software.|
|Average Issue Resolution Time|The average amount of time it takes for issues to be closed.|
|Average Time of First Maintainer Response to Code Merge Request|The average amount of time it takes for a maintainer to make the first response to a code merge request.|
|Average Time of First Response to Issue|The average amount of time it takes for the first response to an issue.|
|Average Time of Open Issues|The average amount of time open issues have remained open.|
|[Board/Council Diversity](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/governance/board-council-diversity.md)|What is the diversity within our governing board or council?|D&I|
|Blog posts|Number of blog posts that mention the project.|
|Bug Age|Age of known bugs in issue tracker.|
|Bugs after Release|Number of bugs reported after a release.|
|[Bus Factor](activity-metrics/bus-factor.md)|The number of developers/organizations it would need to lose to destroy its progress.|Risk|
|[Captioning](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/communication/communication-inclusivity-captioning.md)|Do we provide text captioning for spoken communication?|D&I|
|Change in Maintainer Number|Number of maintainers added/removed over time.|
|[CII Best Practices](https://github.com/chaoss/wg-risk/blob/master/metrics/CII_Best_Practices.md)|The [CII Best Practices Badge Program](https://bestpractices.coreinfrastructure.org/) provides maturity self-certification: passing, silver, and gold.|Risk|
|[Closed Issues](https://github.com/chaoss/wg-evolution/blob/master/metrics/Issues_Closed.md) | What is the number of closed issues? |Evolution|
|[Closed Issues New Contributors](https://github.com/chaoss/wg-evolution/blob/master/metrics/issues-first-time-closed.md)|What is the number of persons closing an issue for the first time?|Evolution|
|[Closed Issue Resolution Duration](https://github.com/chaoss/wg-evolution/blob/master/metrics/issues-closed-resolution-duration.md) | What is the duration of time for issues to be resolved?|Evolution|
|[Code Commits](activity-metrics/code-commits.md)| What is the number of code commits?|
|[Code of Conduct at Event](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/events/event-code-of-conduct.md)|How does the Code of Conduct for events support diversity and inclusion?|D&I|
|[Code of Conduct Enforcement](https://github.com/chaoss/wg-diversity-inclusion/tree/master/focus-areas/governance)|Is enforcement process running at scale (volume, responsiveness, accuracy, fairness)?|D&I|
|[Code Merge Duration](activity-metrics/code-merge-duration.md) | What is the duration of time between code merge request and code commit?|
|Code Modularity|Modular code allowing for parallel development (Baldwin & Clark, 2006).|
|[Code Review Efficiency](https://github.com/chaoss/wg-evolution/blob/master/metrics/pull-requests-code-reviews-efficiency.md) | What is the number of merged code changes/number of abandoned code change requests?|Evolution|
|[Code Review Iteration](https://github.com/chaoss/wg-evolution/blob/master/metrics/pull-requests-code-reviews-iteration.md) | What is the number of iterations that occur before a merge request is accepted or declined?|Evolution|
|[Collaboration Style](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/contribution/collaboration-style.md)|How inclusive is community collaboration?|D&I|
|Commercial Offerings|Availability of commercial products or services based on the project.|
|Commit Bias|Acceptance rate and time to acceptance differences per gender, ethnicity, and relevant diversity characteristics.|
|Commit Hours|Does a contributor commit during or outside of regular business hours? Triangulate UTC commit times from a contributor with locale of contributor and employer to determine regular business hours.|
|[Committers](https://github.com/chaoss/wg-risk/blob/master/metrics/Committers.md)|The number of individuals who have committed code to a project.|Risk|
|[Communication Channels](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/project-and-community/channels.md)|How welcoming, responsive, respectful are interactions even on hot topics of debate? What is the diversity of voices speaking/being heard?|D&I|
|[Community Activity](activity-metrics/community-activity.md)|Contribution Frequency. Contribution = commit, issue, comment, etc).|
|[Contributing Organizations](https://github.com/chaoss/wg-evolution/blob/master/metrics/organizations.md) | What is the number of contributing organizations?|Evolution|
|Contribution Age|Time since last contribution. Contribution = commit, issue, comment, etc.).|
|[Contribution Diversity](activity-metrics/contribution-diversity.md)|Ratio of code committed by contributors other than original project initiator. Contributions going up beyond the core team.|
|[Contribution Sentiment](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/contribution/contribution-sentiment.md)|What are the stars, thumbs up, sentiment in comments?|D&I|
|[Contribution-Type](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/contribution/contribution-type.md)|Coding, Quality Assurance/Testing, Localization/L10N, Diversity & Inclusion, Event Organization, Documenting, Community Building/Management, Teaching, Trouble-shooting/Support, Creative/Design, Social Media, Writing Articles, Bug Triaging, UI/UX, Security/Campaign Advocacy|D&I|
|[Contribution Type](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/recognition/contribution-type.md)|Does recognition skew to a particular kind of contribution?|D&I|
|[Contribution Volume](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/recognition/contribution-volume.md)|Do we have a bias towards small contributions or multiple contributions?|D&I|
|[Contributor Activity](activity-metrics/contributor-activity-level.md)|Activity level of individual contributors.|
|[Contributor Breadth](activity-metrics/contributor-breadth.md)|Ratio of non-core committers (drive-by and peripheral committers).|
|Contributor Country|Primary residence of the contributor.|
|[Contributor Demographics](activity-metrics/contributor-demographics.md)| Gender, age, location, education, and skills.|
|[Contributor Diversity](activity-metrics/contributor-diversity.md)| Ratio of contributors from a single company over all contributors. Also described as: Maintainers from different companies. Diversity of contributor affiliation.|
|Contributor Employer Country|Headquarters location of the organization employing the contributor if they are contributing on behalf of their employer.|
|Contributor Importance|Percentage of commits by individual contributors from identified organizations.|
|Contributor Seniority|For each active contributor, time since first contribution. Experienced contributors providing value to the community, since they carry with them (in part) the history of the project.|
|[Contributors](https://github.com/chaoss/wg-evolution/blob/master/metrics/contributors.md)| What is the number of contributors?|Evolution|
|Copyright Declaration|The degree to which the project properly declares copyright ownership, including the copyright symbol or 'copyright' word, the year of the creation, the name of the author, and a rights statement.|
|Country|Country location of contributor.|
|Decision Distribution|Central vs. distributed decision making. Governance model, scalability of community.|
|Dependency Depth|Number of projects included in code base + number of projects relying on focal project. Indicator about centrality in open source dependency network.|
|Distribution of Work|How much is recent activity distributed?|
|[Diversity Access Tickets](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/events/diversity-tickets.md)|Are Diversity Access Tickets offered for an event?|D&I|
|[Documentation](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/project-and-community/documentation.md)|What is the thoroughness, and accessibility of documentation according to a set of criteria?|D&I|
|Downloads of Non-software Artifacts|Number of downloads of non-software artifacts (e.g. documentation, sample apps, test suites, etc).|
|[Elephant Factor](https://github.com/chaoss/wg-risk/blob/master/metrics/Elephant_Factor.md)|The minimum number of companies whose employees perform 50% of the commits|Risk|
|[Family Friendliness](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/events/family-friendly.md)|Does the event empower those who care for children to attend?|D&I|
|File License Declarations|A list of license declarations on the software package files.|
|[First Response to Issue Duration](https://github.com/chaoss/wg-evolution/blob/master/metrics/issues-maintainer-response-duration.md)|Time between a new issue is opened and a maintainer responds Also called: bug response rate. The maintainer is believed to not “pile on” but try to solve an issue|Evolution|
|[Followers](activity-metrics/followers.md)|Number of followers.|
|[Forks](activity-metrics/forks.md)|Number of forks.|Evolution|
|[Foundation Staff Diversity](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/governance/foundation-staff-diversity.md)|What is the diversity of foundation staff?|D&I|
|Gatherings|Number of face-to-face/in-person meetings per year.|
|Installs|Number of software installations of the project.|
|[Issue Comments](activity-metrics/issue-comments.md)|Number of comments per issue.|
[Issue Resolution Efficiency](https://github.com/chaoss/wg-evolution/blob/master/metrics/issues-closed-resolution-efficiency.md) | What is the number of closed issues/number of abandoned issues?|Evolution|
|[Issues Submitted/Closed](activity-metrics/issues-submitted-closed.md)|Issues submitted vs. issues closed. [Example](http://repocheck.com/#https%3A%2F%2Fgithub.com%2Ftwbs%2Fbootstrap).|
|[Issue Tracker](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/project-and-community/issue-tracker.md)|How well is a project issue tracker setup to invite new contributors, skilled contributors, non-technical contributors?|D&I|
|Job Postings|Number of job postings that mention the project as a preferred or required skill.|
|Known Vulnerabilities|Number of reported vulnerabilities. Could be limited to issue-tracker or extended vulnerability databases (e.g. CVE).|
|Language Bias|Bias against gender and ethnicity in use of language.|
|[Language Makeup](activity-metrics/language-makeup.md)|Makeup of a project in terms of whitespace, code, and comments.|
|Leadership Demographics|Demographics of project's leadership (e.g. Board, Technical Steering Committee, Maintainers, etc.) over time.|
|License Conflicts|Project containing incompatible licenses.|
|[License Count](https://github.com/chaoss/wg-risk/blob/master/metrics/License_Count.md)|Number of licenses.|Risk|
|[License Coverage](https://github.com/chaoss/wg-risk/blob/master/metrics/License_Coverage.md)|Number of files with a file notice (copyright notice + license notice).|Risk|
|[License Declared](https://github.com/chaoss/wg-risk/blob/master/metrics/License_Declared.md)|What license does the project declare?|Risk|
|License Identification Methods|A list of methods or tools used for identifying licenses in files.|
|[Lines of Code Changed](activity-metrics/lines-of-code-changed.md) | What is the number of lines of code changed?|
|[Listening](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/communication/communication-inclusivity-listening.md)|How well do our mechanisms for listening accommodate community?|D&I|
|Maintainer Promotion|Last time a maintainer was added.|
|[Maintainer Response to Merge Request Duration](https://github.com/chaoss/wg-evolution/blob/master/metrics/pull-requests-maintainer-response-duration.md) | What is the duration of time for a maintainer to make a first response to a code merge request?|Evolution|
|[Mode Alternatives](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/communication/communication-inclusivity-mode-alternatives.md)|What alternative communication modes do we offer?|D&I|
|[New Contributing Organizations](https://github.com/chaoss/wg-evolution/blob/master/metrics/organizations-new.md)|What is the number of new contributing organizations?|Evolution|
|New Contributions|Percentage of contributions (patches, pull requests, etc.) from new contributors vs all accepted contributions over time.|
|[New Contributors](https://github.com/chaoss/wg-evolution/blob/master/metrics/contributors-new.md)|What is the number of new contributors?|Evolution|
|[New Contributors Closing Issues](https://github.com/chaoss/wg-evolution/blob/master/metrics/issues-first-time-closed.md)|What is the number of persons closing an issue for the first time?|Evolution|
|[New Contributors of Code Reviews](https://github.com/chaoss/wg-evolution/blob/master/metrics/pull-requests-code-reviews-contributors-new.md)|What is the number of persons contributing with reviews of code for the first time?|Evolution|
|[New Contributors of Commits](https://github.com/chaoss/wg-evolution/blob/master/metrics/pull-requests-merge-contributor-new.md)|What is the number of persons contributing with an accepted commit for the first time?|Evolution|
|[New Contributors of Initiated Code Reviews](https://github.com/chaoss/wg-evolution/blob/master/focus_areas/community_growth.md)|What is the number of persons initiating a code review for the first time?|Evolution|
|[New Contributors of Code Reviews](https://github.com/chaoss/wg-evolution/blob/master/metrics/pull-requests-code-reviews-contributors-new.md)|What is the number of persons contributing with reviews of code for the first time?|Evolution|
|[New Contributors on the Email List](https://github.com/chaoss/wg-evolution/blob/master/metrics/mailing-lists-messages-contributors-new.md)|What is the number of persons posting messages in mailing lists for the first time?|Evolution|
|New Contributors* vs Maintainers**|Ratio of new contributors to maintainers over time.|
|Non-source Contributions|Track contributions like running tests in test environment, writing blog posts, producing videos, giving talks, etc.|
|Number of Active Users|Number of active users of the project.|
|Number of Contributing Organizations|Number of organizations participating in the project over time.|
|Onion Layers|Distance between onion model layers (users, contributors, committers, and steering committee). Rule of thumb: factor of 10x between layers. (OSLS'17 Node.js keynote).|
|[Open Issues New Contributors](https://github.com/chaoss/wg-evolution/blob/master/metrics/issues-first-time-opened.md)|What is the number of persons opening an issue for the first time?|Evolution|
|[Open Issue Age](https://github.com/chaoss/wg-evolution/blob/master/metrics/issues-open-age.md) | What is the the age of open issues?|Evolution|
|Package License Declaration|A list of license declarations on the software package.|
|Paid Developers|Number of paid developers in community over time.|
|[Path to Influence](https://github.com/chaoss/wg-diversity-inclusion/tree/master/focus-areas/governance)|What opportunities are there to move into governance?|D&I|
|Path to Leadership|A communicated path from lurker to contributor to maintainer.|
|Path to Maintainership|Path to maintainership published.|
|[People Opening Issues](activity-metrics/people-opening-issues.md) | How many people are opening issues?|
|Project Life Cycle|Community assigned label. For example: proposal, incubaton, active, deprecated, end of life (Source: [Hyperledger](https://wiki.hyperledger.org/community/project-lifecycle)).|
|[Perceived Value](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/contribution/perceived-value.md)|How are we valuing contributions and contribution types?|D&I|
|Percentile Distribution of First Maintainer Response to Code Merge Request|The proportional frequency of time it takes for a maintainer to make the first response to a code merge request.|
|Percentile Distribution of First Response Time|The proportional frequency of time it takes for the first response to an issue.|
|Percentile Distribution of Issue Resolution Time|Proportional frequency of closed issue time duration.|
|Percentile Distribution of Open Issue Time|Proportional frequency of open issue time duration.|
|Percentile Distribution of Time to Merge Code|Proportional frequency of code merge to upstream time duration.|
|Pony Factor|The minimum number of developers performing 50% of the commits. [The Math](https://ke4qqq.wordpress.com/2015/02/08/pony-factor-math/)|
|[Pull Request Comments](https://github.com/chaoss/wg-evolution/blob/master/metrics/pull-requests-comments.md)|Number of comments per pull request.|Evolution|
|[Pull Request Comment Duration](https://github.com/chaoss/wg-evolution/blob/master/metrics/pull-requests-comment-duration.md)|The difference between the timestamp of the pull request creation date and the most recent comment on the pull request.|Evolution|
|[Pull Request Discussion Diversity](activity-metrics/pull-request-discussion-diversity.md)|Number of different people discussing each pull request.|
|[Pull Request Made vs. Closed](activity-metrics/pull-requests-made-closed.md)|Pull requests made vs. pull requests closed [Example](http://repocheck.com/#https%3A%2F%2Fgithub.com%2Ftwbs%2Fbootstrap). Encompasses number of pull requests rejected.|
|Pull Requests Merged|Number of Code Commits|
|[Pull Requests Merged/Closed (Contribution Acceptance)](https://github.com/chaoss/wg-evolution/blob/master/metrics/pull-requests-merged-vs-closed.md)|Ratio of contributions accepted vs. closed without acceptance.|Evolution|
|[Pull Requests Open](https://github.com/chaoss/wg-evolution/blob/master/metrics/pull-requests-open.md)|Number of open pull requests. |Evolution|
|[Pull Requests Over Time](activity-metrics/pull-requests-over-time.md)|How many pull requests have been submitted over a specified time period?|
|Qualified Committers|Contributions over time and what components they commit to over time.|
|[Quick Links](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/events/quick-links.md)|No Question/Definition|D&I|
|[Recognition Type](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/recognition/recognition-type.md)|No Question/Definition|D&I|
|[Recognition Value](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/recognition/recognition-value.md)| Do different demographics value different types of recognition?|D&I|
|Relative Activity| Ratio of GH issues+comments, GH pull requests+comments, and GH commits for the project members and for the non-project members. Compare the activity between committers-as-a-group and contributors-as-a-group. It shows when a project is not yet popular or when a project is not paying attention to its users.|
|Release Maturity|Ratio of major and minor releases.|
|Release Note Completeness|Number of functionality changes and bug fixes represented in release notes vs. release. Good for users, also shows diligence of community.|
|Release Velocity|Time between releases. Regular releases are a reliability indicator.|
|[Reopened Issues](activity-metrics/reopened-issues.md)|Rate of issues closed but discussion continues or issues that were closed and re-opened.|
|[Repository Size](activity-metrics/repository-size.md)|Overall size of the repository.|
|[Response Times & Quality](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/project-and-community/response-time-quality.md)|How quickly and well do we respond to suggestions, PRs, questions?|D&I|
|Retrospectives|Existence of after release meetings. Collect lessons learned, improve processes, recognize contributors.|
|[Reviews](https://github.com/chaoss/wg-evolution/blob/master/metrics/Reviews.md) | What is new review requests for changes to the source code, during a certain period.?|Evolution|
|Review Efficiency|Number of merged patches / number of abandoned patches over time.|
|Rewards|Rewards, shout-outs, recognition, and mentions in pull-requests or change logs.|
|Roadmap|Existence and quality of roadmap. Best practice as community engagement and scalability (might not be automatically computable).|
|Role Definitions|Existence and quality of role definitions. Relates to "Path to Leadership".|
|[Sentiment](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/project-and-community/sentiment.md)|What is the sentiment within external communication channels regarding our own press releases and within our internal communication channels, e.g., mail lists or IRC?|D&I|
|[Size of Code Base](activity-metrics/size-of-code-base.md)|Lines of code.|
|Software Downloads|Number of project software downloads. Beware: downloads might be skewed by builders. Used as measure for success (Grewal, Lilien, & Mallapragada, 2006).|
|[Software Bill of Materials](https://github.com/chaoss/wg-risk/blob/master/metrics/Software_Bill_of_Materials.md)|Provides a single source document that provides this information both for internal use and downstream distribution of software packages. |Risk|
|[Speaker Demographics](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/events/speaker-demographics.md)|How well does the speaker lineup for the event represent a diverse set of demographics?|D&I|
|[Speaking](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/communication/communication-inclusivity-speaking.md)|Are we speaking to our communities in an accessible range?|D&I|
|Stack Overflow|Number of questions asked, response rate, number of responding people that have verified solutions.|
|Stars|Number of stars.|
|[Sub-Projects](https://github.com/chaoss/wg-evolution/blob/master/metrics/sub-projects.md) | What is the number of sub-projects?|Evolution|
|[Team/Module Ownership Diversity](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/governance/team-module-ownership-diversity.md)|What is the diversity of other bureaucratic and administrative foundation teams, e.g. working groups, committees, or ambassador groups?|D&I|
|[Test Coverage](https://github.com/chaoss/wg-risk/blob/master/metrics/Test_Coverage.md)|Percentage of codebase covered by developer tests.|Risk|
|Time to Contributor|Time to becoming a contributor.|
|Timezone|Timezone of contributor.|
|[Technical Jargon](https://github.com/chaoss/wg-diversity-inclusion/blob/master/focus-areas/communication/communication-inclusivity-technical-jargon.md)|Does the language skew to technical-confidence vs. technical ability?|D&I|
|[Total Contributing Organizations](activity-metrics/total-contributing-organizations.md)|The total number of organizations contributing over time.|
|[Total Contributors](activity-metrics/total-contributors.md)|The total number of contributors over time.|
|Total New Contributing Organizations|The total number of new organizations contributing over time.|
|Total New Contributors|The total number of new contributors over time.|
|Total Sub-projects|The total number of sub-projects over time.|
|[Transparency](activity-metrics/transparency.md)|Number of comments per issue. Discussion is occuring openly.|
|Unity|Rivalry or unity of community.|
|Update Age|Time since last update.|
|Update Rate|Number of updates over time.|
|Update Regularity|How consistently and frequently are updates provided.|
|Use of Acronym|Frequency of acronyms used as a barrier for new contributors.|
|User Dependency|Number of users who are aware that they depend on the software over time.|
|User Groups|Number of user groups that perform a variety of crucial marketing, service support, and business-development functions at the grassroots level\\ (Bagozzi & Dholakia, 2006)|
|V-index|An index of project's first-order and second-order downstream dependencies. [Example](https://www.cncf.io/blog/2017/06/05/30-highest-velocity-open-source-projects/)|
|[Watchers](activity-metrics/watchers.md)|Number of watchers.|
|YouTube Videos|Number of Youtube videos that mention or specifically deal with the project (e.g. tutorials).

## How to Contribute and Participate to the CHAOSS Project

[Contribute and Participate](https://chaoss.community/participate/). If you would like to propose a new metric to this repository, open a new issue and provide a pull request to open the discussion about inclusion. If you would like to provide metric details, we have a __[metric-template](activity-metrics/metric-template.md)__ to be used. Follow the same approach regarding an issue/pull request to have your detail changes discussed and potentially merged. 

## Repository Maintainers

- [Dawn Foster](https://github.com/geekygirldawn)
- [Georg Link](https://github.com/GeorgLink)
- [Matt Germonprez](https://github.com/germonprez)
- [Ben Lloyd Pearson](https://github.com/BenLloydPearson)

[How to become a maintainer](.github/CONTRIBUTING.md#how-to-become-a-repository-maintainer)

# License

All contributions to implementation-agnostic metrics and standards, including associated scripts, SQL statements, and documentation, will be received and made available under the MIT License (https://opensource.org/licenses/MIT).
