# Community Activity

## 1. Description
Community activity in an open source project takes place across a number of different forms of contribution, including code, issue identification. This metric provides a summary level view of specific types of contributions that are operationalized to get a general sense of the level of community engagement.

Unlike most metrics, defined at a raw level, this metric is necessarily aggregated by a minimum unit of time, the week, in order to express contribution rates.

### The following specific data points are indcluded in this metric
  - date: The Sunday that begins a particular week.
  - issues_opened	: How many issues were opened this week?
  - issues_closed	: How many issues were closed this week?
  - pull_requests_opened	: How many pull requests were opened this week?
  - pull_requests_merged	: How many pull requests were merged this week?
  - pull_requests_closed	: How many pull requests were closed this week?
  - issues_opened_total	: How many total issues were opened on this project to date?
  - issues_closed_total	: How many total issues were closed on this project to date?
  - issues_closed_rate_this_week	: issues_opened/issues_closed
  - issues_closed_rate_total	: issues_opened_total/issues_closed_total
  - issues_delta	: Net change in total issues for the week (issues_opened - issues_closed)
  - issues_open	: How many total issues remained open at the conclusion of this week?
  - pull_requests_opened_total	: How many pull requests have been opened on this project to date?
  - pull_requests_closed_total	: How many pull requests have been closed on this project to date?
  - pull_requests_merged_total	: How many pull requests have been merged on this project to date?
  - pull_requests_closed_rate_this_week	: pull_requests_closed/pull_requests_opened
  - pull_requests_merged_rate_this_week	: pull_requests_merged/pull_requests_opened
  - pull_requests_closed_rate_total	: pull_requests_closed/pull_requests_opened
  - pull_requests_merged_rate_total	: pull_requests_merged/pull_requests_opened
  - pull_requests_delta	: Net change in total pull requests for the week (pull_requests_opened-pull_requests_closed)
  - pull_requests_open	: Total number of pull requests remaining open at the end of this week

## 2. Use Cases
A community manager wants to get an overview of their project that helps them understand the aggregate level of engagement in the project.

## 3. Sample Filter and Visualization


## 4. Sample Implementations
### Augur
[API Example](http://twitter.augurlabs.io/api/unstable/rails/rails/timeseries/community_engagement)
[API Docs](https://osshealth.github.io/augur/api/index.html#api-Experimental-CommunityEngagement)
[Source Code](https://github.com/OSSHealth/augur)


## 5. Known Implementations

[Augur](https://github.com/OSSHealth/augur)

## 6. External References (Literature)
