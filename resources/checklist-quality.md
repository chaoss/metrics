To simplify project management on new or updated metrics, you can create tracking tickets using the markdown below as a template. This helps ensure that teams follow CHAOSS quality standards and processes. You can have one large ticket, or break it up into two or three. The checklist items don’t have to be completed all at once - you will probably want to create individual issues for some. 

# Get feedback and prepare release

## Process

- [ ] WG decided to release the metric (Create “review issue” in the authoring WG’s repo for comments during review period)
- [ ] Add metric to WG’s repo (after checking Content Quality and Technical Requirements)
- [ ] Add entry to release notes issue in working group repo and provide the link to the metric
- [ ] Update Spreadsheet of metrics 
- [ ] Create issue in CHAOSS/Translation repository  to kick-off translation to other languages
- [ ] Create issue to request adding metric to [website](https://chaoss.community/metrics/) with link to “review issue”
- [ ] Metric was added to website
- [ ] When above steps are completed, announce new/updated metric on mailing list

# Add Metric to Repo
## Content Quality

- [ ] Required headings are filled in, including Questions.
- [ ] Description provides context to metric
- [ ] Objectives list sample uses for the metric and desired outcomes
- [ ] If any, DEI uses of the metric are included Objectives
- [ ] Optional headings that have no content were removed
- [ ] Contributors section lists those contributors that want to be named
- [ ] The name of the metric is the same in (1) metric heading, (2) metric file name, (3) focus area, (4) metrics spreadsheet, (5) “review issue”, (6) translation issue, and (7) website

## Technical Requirements

- [ ] Message in the metric markdown file that the metric will be part of the next regular release (this is in the metric template)
- [ ] Metric (file name)[https://github.com/chaoss/metrics/blob/master/resources/metrics-template.md] is the full metric name and only contains lower case letters and hyphens (“-”) for spaces
- [ ] Images are included using markdown and relative links (as described in the metrics template)
- [ ] Images have at least one empty line above and below them
- [ ] Ensure images are placed in image folder and followed [naming convention](https://github.com/chaoss/metrics/blob/master/resources/metrics-template.md)
- [ ] If new focus area is created, ensure focus area is added to wg repo readme and focus area folder readme
- [ ] Within the focus area, add the metric in the table and provide the link to the metric and metric question
- [ ] Ensure tables within metric are converted as image and placed in the image folder (both original MD and screenshotted PNG format) and follow the naming convention
- [ ] No HTML code in the metrics markdown file


