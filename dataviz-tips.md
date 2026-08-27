# Dataviz tips, by chart type

A collection of articles and papers with practical guidance on chart design, organised by the chart type each one is most useful for. Sourced mainly from the [ONS Digital blog's dataviz category](https://digitalblog.ons.gov.uk/category/dataviz/), plus a few external references.

## General principles / chart selection

Not tied to one chart type — useful as a starting point before picking a chart.

- [Say what you see – the way we write chart titles is changing](https://digitalblog.ons.gov.uk/2019/01/28/say-what-you-see-the-way-we-write-chart-titles-is-changing/) (ONS, 2019) — write chart titles that state the takeaway in ≤10 words, with a statistical subtitle underneath; applies across chart types.
- [In a relationship – it's complicated](https://digitalblog.ons.gov.uk/2016/08/03/in-a-relationship-its-complicated/) (ONS, 2016) — a two-step method for chart selection: identify the statistical relationship in the data (magnitude, change, part-to-whole, distribution, difference, correlation, rank, spatial), then pick the chart that emphasises it. Compares bar, lollipop, and slope charts on the same dataset.
- [The Art of Charts](https://digitalblog.ons.gov.uk/2015/07/01/the-art-of-charts/) (ONS, 2015) — the origin of ONS's written Style.ONS charting guidance, grounded in Playfair, Tufte, and Gestalt principles.
- [An Economist's Guide to Visualizing Data](https://ovastgacct.blob.core.windows.net/ovamedia/course_materials/An_Economists_Guide_to_Visualizing_Data.pdf) — Jonathan A. Schwabish, *Journal of Economic Perspectives*, 28(1), 2014 — three core principles (show the data, reduce clutter, integrate text and graph) with worked examples of common graph faults.
- [The Science of Visual Data Communication: What Works](https://ovastgacct.blob.core.windows.net/ovamedia/course_materials/The_Science_of_Visual_Data_Communication_-_What_Works.pdf) — Franconeri, Padilla, Shah, Zacks & Hullman, *Psychological Science in the Public Interest*, 22(3), 2021 — research-backed guidelines on what the visual system extracts quickly vs. slowly, and how to design for it.
- [Sourcing and credibility](https://www.edwardtufte.com/notebook/sourcing-and-credibility/) (Tufte forum) — "if you don't say where [information comes from], you are saying 'trust me'"; documentation of sources is part of the basic quality-control mechanism for a chart's credibility, and cherry-picked or unsourced evidence is the single biggest threat to it.
- [Analytical design and human factors](https://www.edwardtufte.com/notebook/analytical-design-and-human-factors/) (Tufte forum, 2002) — argues that chart design should be driven by the cognitive task of reasoning about evidence and content expertise, not by generic human-factors/usability methodology.
- [Scientific visualization: evidence and/or fireworks](https://www.edwardtufte.com/notebook/scientific-visualization-evidence-and-or-fireworks/) (Tufte forum, 2006) — critiques a scientific-visualization award competition where flashy, decorative renderings beat entries that actually supported comparison and analysis; a case study in decoration crowding out evidence.
- [Block that metaphor: the NASA space exploration map](https://www.edwardtufte.com/notebook/block-that-metaphor-the-nasa-space-exploration-map/) (Tufte forum, 2003) — a NASA slide recast planned space missions as a subway map; critiques picking a familiar visual metaphor that doesn't actually fit the data's structure.
- [Graphic visualization of risks](https://www.edwardtufte.com/notebook/graphic-visualization-of-risks/) (Tufte forum, 2003) — discusses how to display multi-factor risk (probability, consequence, cost, timing) in one display, including 2×2 risk matrices, when a single chart can't hold every dimension.
- [Cleaning up Excel's poshlust graphics](https://www.edwardtufte.com/notebook/cleaning-up-excels-poshlust-graphics/) (Tufte forum, 2007) — practical workarounds (Clean Charts add-in, custom templates) for stripping Excel's default chartjunk — gridlines, gradients, 3D — back to a plain, honest chart.
- [Design review: improving a good news graphic](https://www.edwardtufte.com/notebook/design-review-improving-a-good-news-graphic/) (Tufte forum, 2014) — a worked critique of a *New York Times* sea-level-rise graphic, showing how combining rising oceans and sinking land into one map/statistical display can be tightened further.
- [Poor op/ed data graphic in New York Times](https://www.edwardtufte.com/notebook/poor-op-ed-data-graphic-in-new-york-times/) (Tufte forum, 2003) — a case study in a graphic gone wrong: confusing risk ordering, an ad hoc "Fear Index" scale, and a mostly-empty plot area that buries the shark-attack data point it was built around.
- [Megan Jaegerman's brilliant news graphics](https://www.edwardtufte.com/notebook/megan-jaegermans-brilliant-news-graphics/) (Tufte forum, 2007) — a gallery of Jaegerman's *New York Times* graphics (1990–98) as a positive counter-example: every design element is used to explain content, not decorate it.

## Axes & scales

General axis/scale choices, zero baselines (line and bar charts), and dual-axis charts.

- [Use your y-axis](https://digitalblog.ons.gov.uk/2016/06/07/use-your-y-axis/) (ONS, 2016) — how axis range/endpoint choices change the story, using a line chart then a stacked bar chart of women MPs as the running example.
- [Does the axis have to start at zero? (Part 1 – line charts)](https://digitalblog.ons.gov.uk/2016/06/27/does-the-axis-have-to-start-at-zero-part-1-line-charts/) (ONS, 2016) — unlike bars, line-chart axes don't always need to start at zero; truncation is an editorial decision that should be annotated when used.
- [Does the axis have to start at zero? (Part 2 – bar charts)](https://digitalblog.ons.gov.uk/2016/07/23/does-the-axis-have-to-start-at-zero-part-2-bar-charts/) (ONS, 2016) — bar charts should always include zero, since bar length itself is the encoded value; suggests dot plots for narrow-range data instead.
- [Rule 25: Always start your bar charts at zero](https://medium.com/@addtwo/rule-25-always-start-your-bar-charts-at-zero-11d7994ccd5b) (Medium) — same zero-baseline rule for bar charts, as one entry in a broader dataviz rules list.

**Dual-axis charts** (two independent axes on one chart — a separate failure mode from baseline truncation, but still an axis-scale issue):

- [Dueling with axis: the problems with dual-axis charts](https://digitalblog.ons.gov.uk/2019/07/03/dueling-with-axis-the-problems-with-dual-axis-charts/) (ONS, 2019) — dual-axis scales are arbitrary and can be tuned to imply a relationship that isn't there; recommends annotated single-axis charts or splitting into separate charts.
- [Why not to use two axes, and what to use instead](https://www.datawrapper.de/blog/dualaxis) (Datawrapper) — same critique of arbitrary dual-axis scaling, with alternative chart layouts.
- [What to consider when creating dual-axis charts](https://www.datawrapper.de/blog/dual-axis-charts-guide) (Datawrapper) — a more permissive companion piece: when dual axes are actually appropriate and how to design them to reduce misreading.
- [Tick marks in graphs](https://www.edwardtufte.com/notebook/tick-marks-in-graphs/) (Tufte forum, 2003) — whether tick marks should point in, out, or both; consensus (citing Tufte and William Cleveland) favours outward-pointing ticks so they don't obscure the data near the axis.
- [Taking logarithms in statistical data](https://www.edwardtufte.com/notebook/taking-logarithms-in-statistical-data/) (Tufte forum, 2012) — excerpt from *Data Analysis for Politics and Policy* on when and why to log-transform a scale, with a worked "remembering logarithms" example.
- [Auto safety – stopping distance chart](https://www.edwardtufte.com/notebook/auto-safety-stopping-distance-chart/) (Tufte forum, 2003) — a California Highway Patrol chart understates how non-linear stopping distance is with speed (reaction distance at 60 mph exceeds *total* stopping distance at 30 mph); the thread proposes properly scaled curves instead.
- [Dequantification in scientific images](https://www.edwardtufte.com/notebook/dequantification-in-scientific-images/) (Tufte forum, 2003) — "a scientific image isn't scientific unless it has a scale of measurement"; without scale bars or axes, an image (chart or photo) becomes indistinguishable from decoration.

## Stacked bar charts

- [Stacking the bars in your favour!](https://digitalblog.ons.gov.uk/2017/08/17/stacking-the-bars-in-your-favour/) (ONS, 2017) — limit to 3–4 segments, order categories deliberately, and know when to switch to line charts, slope charts, or small multiples instead.

## Pie & donut charts

- [The humble pie chart](https://digitalblog.ons.gov.uk/2017/01/26/the-humble-pie-chart/) (ONS, 2017) — history from Playfair (1801) plus best practices: cap at 5–6 categories, ensure the parts sum to 100%, avoid 3D, use HSL-based colour choices.
- [The humble pie chart: part 2](https://digitalblog.ons.gov.uk/2017/02/28/the-humble-pie-chart-part2/) (ONS, 2017) — reviews Skau & Kosara's research on how accurately people read pie vs. donut vs. exploded-pie vs. treemap; complete pie/donut charts perform best, angle-only encodings worst.
- [Pie charts](https://www.edwardtufte.com/notebook/pie-charts/) (Tufte forum, 2004) — debates whether pie charts are ever defensible; a proportional-circle map (circle size = total, pie segments = mix within it) is offered as a case where the format can work, against Tufte's default preference for tables or small multiples.
- [Florence Nightingale's statistical graphics](https://www.edwardtufte.com/notebook/florence-nightingales-statistical-graphics/) (Tufte forum, 2002) — discusses Nightingale's polar-area "coxcomb" diagrams of Crimean War mortality, and the counter-argument that the polar format conceals part of the data compared to a table.

## Radar charts & heat maps

- [Marriages – when two become one](https://digitalblog.ons.gov.uk/2016/08/26/marriages-when-two-become-one/) (ONS, 2016) — two different treatments of the same marriage-trends dataset: an interactive scrollytelling piece using radar charts and heat maps for data-literate readers, versus a narrative/photo-led piece with simple line graphs for a general audience.

## Tables, deviation charts & maps

- [Should tables be off the table?](https://digitalblog.ons.gov.uk/2016/09/01/should-tables-be-off-the-table/) (ONS, 2016) — the same Welsh house-price table redrawn as a horizontal bar chart, a deviation chart (bars centred on the average), and a choropleth map, each surfacing a different story the table hides.

## Maps

- [The Truthful Art, Chapter 10 – Mapping Data](https://ovastgacct.blob.core.windows.net/ovamedia/course_materials/The_Truthful_Art_Chapter_10_-_Mapping_Data.pdf) — Alberto Cairo — a chapter-length treatment of choropleth maps, projections, and common mapping pitfalls.
- [Detailing on choropleth maps](https://www.edwardtufte.com/notebook/detailing-on-choropleth-maps/) (Tufte forum, 2002) — how to add geographic detail (rivers, roads, elevation) to an epidemiological choropleth without obscuring the data layer; suggests transparent GIS overlays and citing Ian McHarg's *Design with Nature* for layering technique.
- [Data maps](https://www.edwardtufte.com/notebook/data-maps/) (Tufte forum, 2001) — critiques an experimental choropleth-with-histogram-key design, flagging the classic ecological-correlation trap of equating a county's visual area with its population.
- [Maps moving in time: a standard of excellence for data displays](https://www.edwardtufte.com/notebook/maps-moving-in-time-a-standard-of-excellence-for-data-displays/) (Tufte forum, 2013) — holds Swiss mountain maps up as a density/clarity standard, then explores how animating a map through time can add a third dimension without sacrificing that clarity.
- [Election data displays](https://www.edwardtufte.com/notebook/election-data-displays/) (Tufte forum, 2008) — praises 2008 US election-cycle graphics (pollster.com, RealClearPolitics) for combining overview and detail in one display, and fivethirtyeight.com's forecasting approach.
- [Mapping election results](https://www.edwardtufte.com/notebook/mapping-election-results/) (Tufte forum, 2004) — discusses cartograms and alternative colour/area schemes for election maps, where standard geographic area misrepresents a result dominated by population, not land.
- [Unusual maps](https://www.edwardtufte.com/notebook/unusual-maps/) (Tufte forum, 2007) — a gallery thread of unconventional cartography (river-height and elevation maps, animated wind-pattern maps, geotagged-photo density maps) as inspiration for non-standard spatial encodings.
- [Airport maps and runway incursions](https://www.edwardtufte.com/notebook/airport-maps-and-runway-incursions/) (Tufte forum, 2006) — argues that low-resolution, cluttered airport taxi diagrams (lacking cartographic hierarchy) are a contributing cause of runway incursions; pilots and aviation experts weigh in on fixes.
- [Mercator's projection](https://www.edwardtufte.com/notebook/mercators-projection/) (Tufte forum, 2003) — the classic area-distortion problem with Mercator maps, and alternatives (Peters projection, Fuller's Dymaxion map, or just using a globe) for when relative area matters.
- [Flowlines (as in Minard's work)](https://www.edwardtufte.com/notebook/flowlines-as-in-minards-work/) (Tufte forum, 2001) — flow maps that encode a quantity as line width over a geographic base, in the tradition of Minard's Napoleon and French-wine-export maps; a thread of tools and worked examples for building one.
- [Blackout graphic](https://www.edwardtufte.com/notebook/blackout-graphic/) (Tufte forum, 2003) — a NASA Earth Observatory before/after pair of the 2003 Northeast blackout is critiqued for not marking the same reference cities on both images, forcing readers to scroll and hunt for landmarks.

## Dashboards

- [Reinventing the Wheel](https://digitalblog.ons.gov.uk/2017/07/06/reinventing-the-wheel/) (ONS, 2017) — redesigning the static "Well-being Wheel" infographic into an accessible, filterable dashboard; covers colourblind-safe palettes and not relying on colour alone to signal change.
- [Executive dashboards](https://www.edwardtufte.com/notebook/executive-dashboards/) (Tufte forum, 2003) — a proposal to replace gauge-style KPI dashboards with sparklines sparks a broader critique of the dashboard-gauge metaphor itself, arguing for data-dense designs that support thinking rather than a decorative "cockpit" look.
- [Analog gauges and the user interface](https://www.edwardtufte.com/notebook/analog-gauges-and-the-user-interface/) (Tufte forum, 2004) — aircraft instruments are deliberately laid out so every needle points straight up in normal operation, letting an anomaly be spotted instantly; the same "normal = one orientation" trick shows up in racing and submarine dashboards.

## Uncertainty

- [Uncertainty and graphicacy](https://ovastgacct.blob.core.windows.net/ovamedia/course_materials/Uncertainty_and_graphicacy.pdf) — Alberto Cairo, *Outlook Report* — uses hurricane "cone of uncertainty" maps to show how readers misinterpret uncertainty bands, and proposes alternative encodings (e.g. gradient-shaded possible paths).
- [Displaying estimates +/- error, confidence bounds](https://www.edwardtufte.com/notebook/displaying-estimates-error-confidence-bounds/) (Tufte forum, 2017) — methods for typesetting an estimate with its error/confidence bound (stacked LaTeX notation), plus a reminder that the display should reflect real assumptions such as observation independence and p-hacking risk, not just decorate the number with ± error bars.
- [Odds ratios, graphing positive and negative associations together](https://www.edwardtufte.com/notebook/odds-ratios-graphing-positive-and-negative-associations-together/) (Tufte forum, 2004) — how to chart odds ratios that cross 1.0 (both positive and negative associations) on one axis; recommends a log scale and Hi-Lo plots so the confidence interval stays symmetric around the null value.

## Statistical graphics history / Tufte classics

Foundational Tufte pieces worth knowing even when brief — the canonical vocabulary the rest of this file assumes.

- [Chartjunk](https://www.edwardtufte.com/notebook/chartjunk/) (Tufte forum) — excerpts spanning Tufte's 1983–2006 books defining chartjunk: unnecessary decoration (moiré patterns, 3D, gratuitous ornament) that obscures rather than clarifies quantitative information.

## Sparklines

- [Sparklines history by Tufte: 1324 to now](https://www.edwardtufte.com/notebook/sparklines-history-by-tufte-1324-to-now/) (Tufte forum, 2016) — traces the sparkline concept from Tufte's own 1983 *Visual Display of Quantitative Information* back roughly 700 years through manuscripts, maps, and diagrams, and notes Microsoft's 2008 patent filing on "sparklines in the grid."
- [Making better inferences from statistical graphics](https://www.edwardtufte.com/notebook/making-better-inferences-from-statistical-graphics-edward-tufte/) (Tufte forum, 2013) — argues sparklines counter "recency bias" (over-weighting the latest data point) by showing it in the context of many past changes, and discusses the related "rage-to-conclude" bias of seeing patterns that aren't there.
- [Overlapping data graphics to make comparisons](https://www.edwardtufte.com/notebook/overlapping-data-graphics-to-make-comparisons/) (Tufte forum, 2015) — two techniques for direct comparison: a sparkline-table of mutual-fund performance, and an ER technique of folding an ECG tracing in half and holding it to light to align QRS complexes and spot an irregular rhythm.

## Connected scatterplots / XY trajectories

- [Time-series that move through XY space](https://www.edwardtufte.com/notebook/time-series-that-move-through-xy-space/) (Tufte forum, 2016) — plotting a time series as a path through an abstract 2D space (e.g. healthcare spend vs. life expectancy by country, inflation vs. unemployment) instead of against time alone, using small multiples to keep multiple trajectories legible.

## Slopegraphs

- [Slopegraphs for comparing gradients: slopegraph theory and practice](https://www.edwardtufte.com/notebook/slopegraphs-for-comparing-gradients/) (Tufte forum, 2011) — the canonical Tufte reference on slopegraphs (two-point-in-time line charts) for comparing rank and rate of change across many series at once.
- [Cancer survival rates: tables, slopegraphs, barcharts](https://www.edwardtufte.com/notebook/cancer-survival-rates-tables-slopegraphs-barcharts/) (Tufte forum, 2002) — a worked comparison of the same cancer-survival dataset as a table, a slopegraph, and a decorative PowerPoint-style bar chart (labelled chartjunk), showing what the plain formats preserve that the decorated one loses.
- [Sports graphics](https://www.edwardtufte.com/notebook/sports-graphics/) (Tufte forum, 2005) — "runnings" charts show a sports team's season as cumulative deviation from .500, and get folded into sparklines; also covers bumps charts for rowing standings — a rank-over-time cousin of the slopegraph.

## Boxplots & distributions

- [Boxplots data test](https://www.edwardtufte.com/notebook/boxplots-data-test/) (Tufte forum, 2014) — a challenge to construct scatterplots with wildly different underlying patterns that all reduce to the same boxplot, in the spirit of Anscombe's Quartet — a reminder that binning x and summarizing y can hide what's actually going on in the raw data.
- [Display of one dimensional distributions](https://www.edwardtufte.com/notebook/display-of-one-dimensional-distributions/) (Tufte forum, 2003) — "crow's feet" tick marks stacked at a line's endpoints to show multiple coincident data points, an alternative to jittering for showing density along a single axis.
- [Stem and leaf displays](https://www.edwardtufte.com/notebook/stem-and-leaf-displays/) (Tufte forum, 2003) — on a stem-and-leaf plot of volcano heights: Tukey's original plots were built by hand from unsorted almanac data, and Tufte notes a computer-generated version should sort the leaves within each stem for readability.

## Small multiples

- [Illustration of small multiples – Magic Knight Tours](https://www.edwardtufte.com/notebook/illustration-of-small-multiples-magic-knight-tours/) (Tufte forum, 2003) — all 140 solutions to the "magic knight's tour" chess puzzle shown as one grid of small multiples, illustrating the technique's power for comparing many instances of the same structure at once.
- [How can information in 4-dimensions be pictured using 2-dimensional diagrams?](https://www.edwardtufte.com/notebook/how-can-information-in-4-dimensions-be-pictured-using-2-dimensional-diagrams/) (Tufte forum, 2001) — visualizing a 4-variable economic relationship (two firms' quantities and two product characteristics) using linked small-multiple 2D plots and colour encoding rather than a single chart.

## Tables & timetables

- [Graphical timetables](https://www.edwardtufte.com/notebook/graphical-timetables/) (Tufte forum, 2014) — a bus-timetable design overlaying schedules and routes on aerial photographs, so hourly/daily/weekly service rhythms are visible and readers can orient themselves by familiar landmarks.
- [Table and timetable design and typography](https://www.edwardtufte.com/notebook/table-and-timetable-design-and-typography/) (Tufte forum, 2015) — excerpt from *Envisioning Information* on typographic choices (rules, spacing, alignment) that make tables and timetables scannable.
- [Zebra tables and lists](https://www.edwardtufte.com/notebook/zebra-tables-and-lists/) (Tufte forum, 2004) — Tufte calls alternating-row-colour "zebra striping" a form of chartjunk that can make the eye jump between same-coloured rows; recommends restrained typography or subtle rules instead.
- [Do zebra-striping practices in table UI design enhance readability or create visual noise?](https://medium.com/@designbyfgs/do-zebra-striping-practices-in-table-ui-design-enhance-readability-or-create-visual-noise-5d98cc59f4fd) (Medium) — a UI-design counterpoint weighing zebra striping's row-tracking benefit in dense tables against Tufte's chartjunk critique above.
- [Round to two digits](https://www.edwardtufte.com/notebook/round-to-two-digits/) (Tufte forum, 2004) — evidence (citing Washburne 1927 and Ehrenberg) that rounding to about two significant digits improves table readability, with the caveat that appropriate precision still depends on the content and measurement accuracy.
- [Table graphics](https://www.edwardtufte.com/notebook/table-graphics/) (Tufte forum, 2004) — a general discussion of table data density, when a table beats a chart, and how tables scale into small-multiple layouts.

## Financial & stock charts

- [Financial data displays](https://www.edwardtufte.com/notebook/financial-data-displays/) (Tufte forum, 2009) — highlights a 2002 *New York Times* graphic that combines a stock-price line, an annotated timeline, and a table to narrate Enron's collapse — a model for integrating price history with the events that explain it.
- [Plotting share (stock) volumes](https://www.edwardtufte.com/notebook/plotting-share-stock-volumes/) (Tufte forum, 2003) — trading volumes span orders of magnitude (hundreds of thousands to hundreds of millions of shares); debates linear vs. log vs. square-root scaling for keeping both normal variation and outlier spikes visible.
- [Graphic: stock performance](https://www.edwardtufte.com/notebook/graphic-stock-performance/) (Tufte forum, 2003) — a fund-performance graphic is critiqued for reversing the usual left-to-right time axis, which visually disguises recent losses; broader discussion of transparency norms in fund-performance reporting.
- [Formatting for financial scorecards and detailed reports](https://www.edwardtufte.com/notebook/formatting-for-financial-scorecards-and-detailed-reports/) (Tufte forum, 2003) — whether ruled lines/boxes are needed to organize a financial scorecard table, versus using whitespace and typography within Excel's constraints.

## Venn diagrams & area-proportional charts

Charts that use area or size to encode a quantity — the same failure mode (area misread as the encoded value) recurs across all three.

- [Venn diagrams](https://www.edwardtufte.com/notebook/venn-diagrams/) (Tufte forum, 2003) — a request for software that draws *proportional* Venn diagrams (set and overlap sizes scaled to the data) rather than the default uniform-circle version, which misrepresents relative set sizes.
- [Comparing weights of irregular shapes](https://www.edwardtufte.com/notebook/comparing-weights-of-irregular-shapes/) (Tufte forum, 2003) — should a fish outline be scaled 50% smaller to represent a 50% weight loss? Discusses why scaling a 2D silhouette by a linear factor misrepresents a mass/area change, and alternatives (dot charts, actual photos, length-weight formulas).
- [Map of the stock market](https://www.edwardtufte.com/notebook/map-of-the-stock-market/) (Tufte forum, 2002) — critiques the SmartMoney treemap ("Map of the Stock Market") for using 2D area to encode a 1D number and under-labelling; the designer's counter-argument is that it optimizes for trader "glanceability" over precise reading.

## Nomographs

- [Nomographs](https://www.edwardtufte.com/notebook/nomographs/) (Tufte forum, 2002) — nomograms (contour-line graphical calculators for multivariate relationships) have lost their computational role now that computing is cheap, but Tufte notes they remain a useful way to build intuition for how several variables interact.

## Tornado plots & sensitivity analysis

- [Tornado plots](https://www.edwardtufte.com/notebook/tornado-plots/) (Tufte forum, 2002) — what tornado plots are (horizontal bars ranking how much each input uncertainty moves an outcome, e.g. net present value), how to build them in Excel or dedicated tools, and pitfalls in their statistical setup.

## Legends & color encoding

- [Legends and colors](https://www.edwardtufte.com/notebook/legends-and-colors/) (Tufte forum, 2004) — how to keep 40+ categories distinguishable in a scatterplot legend across both screen and print; recommends ColorBrewer palettes plus secondary encodings (shape, border) once colour alone runs out of resolution.
- [Traffic light colors](https://www.edwardtufte.com/notebook/traffic-light-colors/) (Tufte forum, 2003) — red/green traffic signals are unreadable to the ~5% of men with red-green colour blindness; a long-running thread on shape- and position-based alternatives to a colour-only encoding, directly relevant to red/green status indicators in charts and dashboards.
- [Charting chess](https://www.edwardtufte.com/notebook/charting-chess/) (Tufte forum, 2003) — a *New York Times* human-vs-computer chess graphic is praised for text/image integration but critiqued for using an ad hoc chart legend to label players instead of standard chess-diagram conventions.

## Medical & statistical graphics

- [Survival vs. mortality results from cancer detection](https://www.edwardtufte.com/notebook/survival-vs-mortality-results-from-cancer-detection/) (Tufte forum, 2007) — a core statistical-graphics trap: early diagnosis lengthens *survival time* without necessarily changing the *mortality rate*, so screening-benefit charts built on survival statistics alone can be systematically misleading (lead-time bias).
- [Graphical summaries for medical patients](https://www.edwardtufte.com/notebook/graphical-summaries-for-medical-patients/) (Tufte forum, 2011) — sparkline-based patient timelines and clinical summaries, referencing Tufte's own co-authored papers in *The Lancet* (1994) and *Psychiatric Services* (1997) on visualizing patient status over time.

## Weather charts

- [New York City weather chart](https://www.edwardtufte.com/notebook/new-york-city-weather-chart/) (Tufte forum, 2004) — a *New York Times* daily high/low/normal/record temperature-plus-cumulative-precipitation chart; comments debate whether precipitation (an accumulating quantity) is better shown as discrete bars than as a continuous line.
- [Weather reporting on television](https://www.edwardtufte.com/notebook/weather-reporting-on-television/) (Tufte forum, 2003) — argues TV weather segments under-use their visual bandwidth, relying on a talking head instead of the rich, information-dense graphics the format could support.
