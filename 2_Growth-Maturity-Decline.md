# Metric: Growth-Maturity-Decline


 Activity Metric | Description
 --- | ---
 Tickets Closed | Total number of tickets closed
 Bug Time to Close | Time from bug opened to bug closed
 Time to Merge | Time from submission to merge or abandon
 Review Efficiency | Number of merged patches / Number of abandoned patches
 Number of New Contributors | Number of first time contributors over time
 Community Growth | Number of new developers over time

**Disclaimer:**
The activity metrics listed are not meant to represent a fully comprehensive list. It is fully expected that this list will evolve as people have insights and thoughts about the activity metrics that comprise Growth-Maturity-Decline. 

**Tooling:**
The activity metrics are intended to be a starting point for community health related tooling. It is expected that the activity metrics will evolve based on the ability (or inability) of tooling to successfully implement the activity metrics. 

**Background:**
The activity metics have been identified based on workshops at the Open Source Leadership and the Open Source Summit North America. In addition, the activity metrics are based on active CHAOSS mailing list conversations. The activity metrics listed here are the result of compiling the discussions to data. We thank everyone who participated.

**How to contribute:**
- To advance the document, fork the repo, make your changes, create a pull request see CONTRIBUTING.md
- To ask questions or make comments, post to our [mailing list][ml], join our weekly [Hangout call][ho], or open an [issue on GitHub][issue].

[ml]: https://wiki.linuxfoundation.org/chaoss/metrics#mail-list
[ho]: https://wiki.linuxfoundation.org/chaoss/metrics#weekly-hangout
[issue]: https://github.com/chaoss/metrics/issues

## Growth-Maturity-Decline: Metric -> Signal -> Action

### Value Accumulation
- Patch speed: There can be two different data.  One is "review efficiency", which is the number of merged/abandoned changes out of all submitted patches over a given period.  The other is "time-to-merge", which is the time since a patch is submitted until this is merged/abandoned.
- Bug resolution: Somewhat similar to the patch speed above.  We could look at the total number of tickets closed out of all the tickets opened over a given time period.  We can also look at the "time-to-close", which is time since a bug is opened until it is closed.
- *Why:*
    - We want to know how active a project is and whether new contributions are being accepted in a timely fashion.
- *Signals:*
    - Higher velocity signals regular/on-going activities in the community 
- *Informs activity:*
    - (not discussed at OSSNA)
- *Potential positive or negative outcomes:*
    - (not discussed at OSSNA)

### Community Growth
- Number of new developers: Number of new contributors (using appropriate userid) over a period (e.g. monthly, quarterly, etc.)
- *Why:*
    - Growth can be measured in new developers.
- *Signals:*
    - More newcomers signal on-going interest/awareness in the project and the community.  
- *Informs activity:*
    - (not discussed at OSSNA)
- *Potential positive or negative outcomes:*
    - (not discussed at OSSNA)

### Usage
- Trajectory of usage (e.g. OpenSSL high usage was not indicative) - time over time activity.
- Project dependency - ecosystem position: where is the project on the continuum between mostly used downstream or mostly dependent on upstream? - that determines how the other metrics are interpreted.
- *Why:*
    - We have to understand contextual factors to understand the other metrics and signals.
    - Let's us compare a project over time.
- *Signals:*
    - Transparency
    - More usage (upstream and downstream) might be good
    - Upstream contribution may be good
    - Downstream usage may be good
    - Transparency may be positive - possibly signaled by
        - Where communication occurs
        - # of people
- *Informs activity:*
    - (not discussed at OSSNA)
- *Potential positive or negative outcomes:*
    - (not discussed at OSSNA)

## Images from workshop
We thank everyone who participated in the workshop at the Open Source Summit North America. The below picture is the flip chart figure that came out of the Growth-Maturity-Decline group.

![Flip Chart Figure](img/OSSNA2017.GMD.jpg "Flip Chart Figure")
