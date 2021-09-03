This issue is created to collect comments about the rolling release of "______"

This metric can be found here: https://github.com/chaoss/xxxxxxx/xxxxxxx/xxxxxxx.md

See all release candidates: https://chaoss.community/metrics/

## CHAOSS Metric Quality Checklist
This checklist is used for new and updated metrics to ensure we follow CHAOSS quality standards and processes. Below checklist items don’t have to be completed all at once: create the metric release candidate issue first and then start working on the checklist.

### Process

- [ ] Create the “review issue” in the authoring WG’s repo for comments during review period and paste this template in
- [ ] Create pull request to edit or add metric to WG’s repo (after checking Content Quality and Technical Requirements below)
- [ ] Add the new metric or metric edit to release notes issue in working group repo
- [ ] Update the [Metrics Spreadsheet](https://docs.google.com/spreadsheets/d/1tAGzUiZ9jdORKCnoDQJkOU8tQsZDCZVjcWqXYOSAFmE/edit)
- [ ] Create issue in [CHAOSS/Translations repository](https://github.com/chaoss/translations) to kick-off translation to other languages (please use the the translation issue template)
- [ ] "Metric Candidate Release" label added to the metric release candidate issue.
- [ ] Metric was added to website

**When above steps are completed:**

- [ ] Announce new/updated metric on mailing list, newsletter, community Zoom call, and Twitter. This can be coordinated with the community manager.

### Content Quality

- [ ] Required headings are filled in, including Questions.
- [ ] Description provides context to metric
- [ ] Objectives list sample uses for the metric and desired outcomes
- [ ] If any, DEI uses of the metric are included in Objectives
- [ ] Optional headings that have no content were removed
- [ ] Contributors section lists those contributors that want to be named
- [ ] The name of the metric is the same in (1) metric heading, (2) metric file name, (3) focus area, (4) metrics spreadsheet, (5) “review issue”, (6) translation issue, and (7) website

### Technical Requirements

- [ ] Message in the metric markdown file that the metric will be part of the next regular release is at top of page and the links are correct (this is in the [metric template](https://github.com/chaoss/metrics/blob/master/resources/metrics-template.md))
- [ ] Metric file name is the full metric name and only contains lower case letters and hyphens (“-”) for spaces
- [ ] Images are included using markdown and relative links (as described in the metrics template)
- [ ] Images have at least one empty line above and below them
- [ ] Ensure images are placed in image folder and followed [naming convention](https://github.com/chaoss/metrics/blob/master/resources/metrics-template.md)
- [ ] If new focus area is created, ensure focus area is added to wg repo readme and focus area folder readme
- [ ] Within the focus area, add the metric in the table and provide the link to the metric and metric question
- [ ] Ensure tables within metric are converted as image and placed in the image folder (both original MD and screenshotted PNG format) and follow the naming convention
- [ ] No HTML code in the metrics markdown file




