# Chart critique checklist

A working checklist for reviewing a chart/plot for statistical and presentational issues, distinct from general chart-design checklists (e.g. Evergreen & Emery's *Data Visualization Checklist*), which focus on formatting and clarity. This one focuses on ways a chart can misrepresent the underlying data even when it's well-designed.

Related frameworks worth knowing:
- **SCAM** (Source, Chart, Axes, Message) — a simple four-part framework for spotting misleading charts.
- **Kaiser Fung's "Trifecta Checkup"** ([junkcharts.typepad.com](https://junkcharts.typepad.com/junk_charts/trifecta-checkup/)) — evaluates whether the underlying question, the data, and the visual all tell the same story.
- **Alberto Cairo, *How Charts Lie*** (2019) — the most thorough taxonomy of how charts mislead.
- **Evergreen & Emery, "Data Visualization Checklist"** (2014/2018) — 24 criteria on formatting/clarity (Text, Arrangement, Color, Lines, Overall).
- **Derek Sonderegger, *STA 141 – Exploratory Data Analysis and Visualization*** ([bookdown.org](https://bookdown.org/dereksonderegger/141/index.html)) — course notes aimed at inoculating readers against misleading data and graphs by teaching the follow-up questions to ask.
- **Data Visualization Society, "Critique"** ([datavisualizationsociety.org](https://datavisualizationsociety.org/mentorship/critique/)) — the DVS #share-critique framework (goals, audience, project stage, feedback sought) plus links to example critiques.

This checklist leans on the statistical/methodological end of that spectrum, since that's where the gaps in the frameworks above tend to be.

## Axes & scale

1. Does any axis have a non-zero baseline? If so, is the truncation flagged, or does it visually exaggerate the change?
2. Are the axis tick intervals/ranges chosen in a way that happens to make the data "fit" a particular narrative (e.g., compressing a divergence, stretching a small change)?

## Dual axes / multiple series

3. If two series share a chart with independent axes, are the units commensurate (e.g., both rates, both counts)? Flag any pairing of a normalized measure (%, rate) with an unnormalized one (raw count, level) — there's no principled way to co-scale them, so the visual relationship is manufactured by axis-window choice.
4. Is the relative scaling between the two axes justified anywhere, or arbitrary/unstated?
5. Do the two series actually move together across the *whole* period shown, or only part of it? Check the divergent stretches, not just the endpoints.
6. If areas are shaded/filled, does the shaded region represent something meaningful, or is it decorative and implying false comparability between two different units?

## Extrapolation & projections

7. Is any part of the plotted line/bar actually a projection, model output, or extrapolation rather than observed data?
8. If so, is it visually distinguished (dotted line, shading, "projected" label) with prominence matching the disclosure it needs?
9. Is there an uncertainty band/interval on the projected portion, or is a single point estimate drawn with the same confidence as the historical data?
10. How much of the trend is the extrapolation based on — a long stable run, or a short/noisy recent segment being extended a long way forward?

## Sample size & precision

11. What's the underlying N for each bar/point? Are any built on small absolute counts (rare events, small subgroups) that would carry meaningful sampling noise?
12. Is the displayed precision (decimal places) appropriate to that N, or does it imply more confidence than the data supports?
13. Are error bars/confidence intervals present anywhere they'd matter? If never, is that a report-wide gap?

## Chart type fit

14. Does the chart type match the underlying data structure? (E.g. a boxplot/distribution used where a time trend is the actual claim being made; a bar chart implying a continuum across a categorical axis; a "gradient" claim over data that isn't monotonic.)
15. If a single axis groups multiple categories, are they actually points on one meaningful continuum, or is it splicing together unrelated classification systems?

## Labeling & annotation

16. Are individual data points labeled where identity matters (e.g., which country is which dot in a scatter)?
17. Is a trend/regression line drawn without stating the correlation strength (R², slope, n)? Is an obvious outlier driving the fit without acknowledgment?
18. Is the chart title's claim (e.g. "gradient", a named methodology) actually what's plotted, or does it overstate/mislabel the content?

## Color & accessibility

19. Are similarly-hued series used for more than ~3-4 categories, risking confusion for colorblind readers, especially with no secondary encoding (pattern, marker shape)?

## Source/text consistency

20. Does the chart's data source match the country/dataset the surrounding prose is describing?
21. Does the chart's y-axis or headline number match the number quoted in the body text for the same claim?

---

Most charts will only trip a handful of these. The point isn't to score every chart against all 21 — it's to have a consistent set of things to check instead of triaging toward whichever 3-4 issues look most interesting at a glance, which is the easiest way to miss something real in a chart-heavy report.
