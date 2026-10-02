# Problem Statement

*As delivered 2026-09-25. Kept verbatim; don't edit. If the research question
changes, record the change in the notes rather than rewriting this.*

## Introduction

Searching a large video collection for a specific moment requires more than a single
query. Finding it may take a text description, a visual example, filters over metadata, or
several of these in sequence, so interactive multimedia retrieval systems offer users a
range of retrieval, visualization, and exploration features. How best to combine these
features to find a target quickly and reliably remains an active area of research.

Venues such as the Video Browser Showdown, Lifelog Search Challenge, and CASTLE
compare such systems through a series of live search tasks (Sauter et al., 2024),
solved by expert operators under time pressure. Participants are encouraged to log user
interactions and search results, but logging formats differ between systems, making the
data difficult to compare (Jäckl et al., 2026), so systems are compared mainly by their
final ranking. A ranking shows the outcome of a search, not how the participant reached
it. Replaying user interactions would make a single retrieval process available for study,
showing how a result was reached rather than only that it was.

To enable such analysis, Jäckl et al. (2026) proposed a fine-grained logging format,
applied to Exquisitor and PraK at the Video Browser Showdown 2026. Their analysis
showed that interaction logs can provide insights beyond final ranking performance.

Exquisitor is an experimental multimedia retrieval system combining conversational
search, relevance feedback, and metadata filtering over large collections (Khan et al.,
2026). It already implements fine-grained interaction logging, but its logs require
post-processing to conform to that format, and it is unclear whether they record enough
to reproduce an entire session.

**Research question:**

> To what extent can Exquisitor's current logging data support replay of an entire user
> session, and what additional information or system changes would replay require?

This project makes three contributions: (1) an assessment of Exquisitor's logging with
respect to session replay, (2) an analysis of what the logs would need to record, and (3)
a prototype demonstrating replay.

## Proposed approach

We distinguish two forms of replay. Re-execution reruns logged queries against the
system and compares the results with those recorded; session reconstruction rebuilds
what the user saw, without re-running the search. The two place different demands on
what a log must contain, and we assess Exquisitor's logging against both. Based on this
assessment, we prototype the changes needed to support one of them.

## Method and Deliverables

The research uses a prototype-driven case study. We will work with Exquisitor's
backend, the Live Services Engine, and its web interface, using the format of Jäckl et al.
as a reference for assessing the existing logging. Deliverables are a gap analysis, a
replay prototype, and the final report, with presentations in October and November and
hand-in in December.

## References

Jäckl, B., Khan, O. S., Verner, B. V., Vopalkova, Z., Schlegel, U., Keim, D. A., and Lokoč, J.
(2026). What drove success at the 15th Video Browser Showdown? A comprehensive
interaction-logging analysis. ICMR '26. https://doi.org/10.1145/3805622.3810635

Khan, O. S., Sharma, U., Marcelino, G., Rudinac, S., and Jónsson, B. Þ. (2026). Exquisitor at
the Video Browser Showdown 2026: Temporal queries revisited. MMM 2026, LNCS 16415,
245–251. https://doi.org/10.1007/978-981-95-6963-2_27

Sauter, L., Gasser, R., Schuldt, H., Bernstein, A., and Rossetto, L. (2024). Performance
evaluation in multimedia retrieval. ACM Transactions on Multimedia Computing,
Communications and Applications 21(1), Article 23.
