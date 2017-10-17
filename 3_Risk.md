# Metric: Risk

Activity Metric | Description
--- | ---
Contributor Importance | Percentage of commits by individual contributors
Qualified Committers | contributions over time and what components they commit to
User Dependency | Number of users who are aware that they depend on the software
Paid developers | Number of paid developers in community



**Background:**
At the Open Source Summit North America, a group of around 8-12 people each agreed on the metrics important in the following scenarios.
For now, we will focus our conversation around these outcomes to further the conversation.
The two-hour session sparked great conversations but could not address all aspects.
We thank everyone who participated.

Below is the metric->signal->action chain for *Risk*.

**How to contribute:**
- To advance the document, fork the rep, make your changes, create a pull request see CONTRIBUTING.md
- To ask questions or make comments, post to our [mailing list][ml], join our weekly [Hangout call][ho], or open an [issue on GitHub][issue].

[ml]: https://wiki.linuxfoundation.org/chaoss/metrics#mail-list
[ho]: https://wiki.linuxfoundation.org/chaoss/metrics#weekly-hangout
[issue]: https://github.com/chaoss/metrics/issues

## Risk: Metric -> Signal -> Action

### Case Characteristics
- *Heartbleed:* common and widespread adoption of software, not actively maintained, not enough developers, expertise required to do audits is high.

### Activity
- Different measures, e.g. number of commits combined with number of committers, possibly focus on qualified committers (determined by contributions over time and what components they commit to)
- *Why:* Determine whether project is actively maintained by developers with sufficient expertise.
- *Signals:*
    - We cannot make assumptions, what activity signals because many factors play into this. Someone has to look at the metrics and make a judgement call. Examples are below:
    - Low activity in code segments can signal 'orphaned code' that may be outdated or not been looked at
    - Low activity may also signal maturity and stable code
    - High activity in code may signal risk due to untested code
    - High developer turn-over may signal risky behavior because contributors don't know code well
- *Informs activity:*
    - (not discussed at OSSNA)
- *Potential positive or negative outcomes:*
    - (not discussed at OSSNA)

### User Awareness
- Number of users who are aware that they depend on the software
- *Why:* Determine whether people would know to update or care to report bugs.
- *Signals:*
    - Low user awareness signals that they have no interest in the health of the community
    - Low user awareness signals low interest in the role of the infrastructure
    - Low user awareness signals that users don't know that they should care
- *Informs activity:*
    - High user awareness leads to users staying up to date on software releases
    - In case of Heartbleed, a campaign was launched to educate the public
        - Something highly technical was communicated in a way that the layperson understood
        - The only way to get into public consciousness is to not talk in technical terms
- *Potential positive or negative outcomes:*
    - Education about risks may lead to 'disaster fatigue'

### Funding
- Money available for paid developers
- *Why:* Determine level of obligation of maintainers.
- *Signals*
    - Low funding signals that most development is done by volunteers or subsidized by companies
    - Decreasing funding signals risk because fewer developers can be paid to maintain the code
    - Increasing funding signals risk if it lags behind the overall project growth
- *Informs activity:*
    - Core Infrastructure Initiative is the response that came out of Heartbleed
- *Potential positive or negative outcomes:*
    - (not discussed at OSSNA)
