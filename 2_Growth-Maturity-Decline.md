# Metric: Growth-Maturity-Decline


 Activity Metric | Description
 --- | ---
 Tickets Closed | Total number of tickets closed
 Time to Close | Time from bug opened to bug closed
 Time to Merge | Time from submission to merge or abandon
 Review Efficiency | Number of merged patches / Number of abandoned patches
 # of New Contributors | Number of first time contributors over time
 Community Growth | Number of new developers over time


**Background:**
At the Open Source Summit North America, a group of around 8-12 people each agreed on the metrics important in the following scenarios.
For now, we will focus our conversation around these outcomes to further the conversation.
The two-hour session sparked great conversations but could not address all aspects.
We thank everyone who participated.

Below is the metric->signal->action chain for *Growth-Maturity-Decline*.

**How to contribute:**
- To advance the document, fork the rep, make your changes, create a pull request see CONTRIBUTING.md
- To ask questions or make comments, post to our [mailing list][ml], join our weekly [Hangout call][ho], or open an [issue on GitHub][issue].

[ml]: https://wiki.linuxfoundation.org/chaoss/metrics#mail-list
[ho]: https://wiki.linuxfoundation.org/chaoss/metrics#weekly-hangout
[issue]: https://github.com/chaoss/metrics/issues

## Growth-Maturity-Decline: Metric -> Signal -> Action

### Value Accumulation
- Bug resolution: Somewhat similar to the patch speed above.  We could look at the total number of tickets closed out of all the tickets opened over a given time period.  We can also look at the "time-to-close", which is time since a bug is opened until it is closed.
- Patch speed: There can be two different data.  One is "review efficiency", which is the number of merged/abandoned changes out of all submitted patches over a given period.  The other is "time-to-merge", which is the time since a patch is submitted until this is merged/abandoned.
- *Why:*
    - We want to know how active a project is and whether new contributions are being accepted in a timely fashion.
- *Signals:*
    - Value Accumulation: higher velocity signals more value accumulated
- *Informs activity:*
    - (not discussed at OSSNA)
- *Potential positive or negative outcomes:*
    - (not discussed at OSSNA)

### Community Growth
- Number of new developers: Number of new contributors (using appropriate userid) over a period (e.g. monthly, quarterly, etc.)
- *Why:*
    - Growth can be measured in new developers.
- *Signals:*
    - More people on the project might signal more transparency.
    - More transparency might be positive.
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
