# CSJ: Baby Bust

The Centre for Social Justice published two related reports on UK fertility decline:

- [*Baby Bust: Helping families realise their dreams of parenthood*](https://www.centreforsocialjustice.org.uk/library/baby-bust) (March 2026, 13 figures) — [PDF](https://www.centreforsocialjustice.org.uk/wp-content/uploads/2026/03/CSJ-Baby_Bust.pdf)
- [*Baby Bust: Update — The state of births in England and Wales*](https://www.centreforsocialjustice.org.uk/library/baby-bust-update) (July 2026, 10 figures) — [PDF](https://www.centreforsocialjustice.org.uk/wp-content/uploads/2026/06/Baby-Bust-Update.pdf)

Both were reviewed against the [checklist](checklist.md). Findings below, most consequential first per report. The Update report shows some genuine improvement in how it handles projections compared to the original — noted where relevant.

## Report 1: Baby Bust (March 2026)

### Figure 5 — cohort fertility with unlabeled forward extrapolation

The most consequential issue in the report. Figure 5 (proportion of women who've had a live birth by age 30/35/40/45, by birth cohort) uses "regressed forward trends" — linear extrapolations — for any cohort that hasn't yet reached the target age. Cohorts born in the 1980s/90s haven't reached 40 or 45 yet, so those segments are projections, not observed data. The only visual distinction is a dotted line style, with no legend entry explaining it, and no uncertainty band.

This matters because Figure 5 is the direct input to the report's headline claim of "600,000 missing mothers": it assumes no recuperation of delayed births, when cohort-fertility literature generally finds that women who delay childbearing partially catch up rather than simply not having the child at all. Checklist items: #7, #8, #9, #10.

### Figure 3 — boxplot masking the trend it's meant to disprove

"Children per Mother" shown as boxplots per country, pooling 1970–2020 for the UK/Japan/US but only 1970–2014 for Italy — inconsistent windows across the four boxes (#20). More importantly, the surrounding text claims CPM "has increased slightly" in the US over this period — i.e. there's a trend — but a boxplot collapses 50 years into a static distribution and can't show that. Wrong chart type for the claim being made (#14).

### Figure 8a/8b — truncated axis

Real earnings for non-college men, y-axis runs $45k–75k rather than from zero. The ~11% decline ($56.4k → $50k) is stretched across most of the visible chart height (#1).

### Figure 11 — chart/text source mismatch

The surrounding paragraph cites specific IVF success-rate figures from **Australian** data (VARTA), but the chart itself is sourced from a **Japanese** ART registry (2019). The numbers discussed in prose and the numbers plotted aren't from the same country (#20).

### Figure 12 — outlier-driven correlation claim, cluttered labels

Childcare cost vs. TFR across OECD countries includes Israel as an extreme outlier (TFR ~2.8) for reasons unrelated to childcare policy. A near-flat regression line is drawn through the cloud to support a "no correlation" claim, with no sensitivity check for removing the outlier and no R² reported (#17). Country labels are also badly crowded in the low-cost cluster, reducing readability (#16).

### Figure 7 — unlabeled scatter, no reported correlation statistic

Fertility gap (married vs. never-married) vs. share of nonmarital births — points are unlabeled countries, so there's no way to verify which point drives the "plateau past 30–40%" pattern asserted in the text (#16, #17).

### Figure 13 — mislabeled methodology

Captioned "Kaya identity: percentage change in the drivers of CO₂ emissions", but the Kaya identity has **four** multiplicative factors (population × GDP/capita × energy intensity × carbon intensity of energy). Only three series are plotted; the two terms that actually explain the CO₂ decline (energy and carbon intensity) are omitted (#18).

### Minor: color/accessibility

Figure 2 (stacked area, 5 pension-spending categories) and Figure 11 (4 lines) use similarly-hued reds/pinks/teals with no secondary encoding (#19).

## Report 2: Baby Bust: Update (July 2026)

### Figure 10 — splices two unrelated classifications onto one axis

The most serious issue in the update. "The stillbirth gradient from affluence to sole registration" puts six categories on one x-axis as if they're steps on a single continuum: Least deprived → National average → Most deprived → Within marriage → Outside marriage (different address) → Sole registration. Deprivation decile and registration type are two different, only partially overlapping dimensions, not points on one ladder (#15). This directly contradicts §7.4 of the same report, which explicitly says the two factors "are not independent phenomena" and need to be understood as separately compounding — the chart oversimplifies the more careful point the text is making.

### Figures 8–10 — small-N rates shown with false precision

Figure 8 is captioned "the poverty gradient: decile by decile" but isn't monotonic — Decile 4 (4.1) sits above Decile 3 (4.0), Decile 6 (3.7) spikes above both neighbours (#14). With ~2,292 stillbirths split across 10 deciles, each bar rests on a small enough count that sampling noise is plausible, but there are no confidence intervals anywhere in the chapter (#13).

The "sole registration" stillbirth rate (6.59 per 1,000) — which drives the headline "relational deprivation > material deprivation" claim — rests on 167 stillbirths nationally, then Figure 9 splits that further by year into even smaller slices, plotted to two decimal places (#11, #12).

### Figures 1, 3, 4 — recurring dual-axis / unit-mismatch problem

Three charts pair series on independent axes and shade the area between them:

- **Figure 4** is the clearest instance: it shades the gap between marriage rate (per 1,000 unmarried adults, axis 0–90) and TFR (per woman, axis 0.5–3.5). The units are incommensurate; the shaded "gap" has no real meaning (#3, #6).
- **Figure 3** overlays "% births within marriage" (falling monotonically since 1973) against "total live births" (which rose through the 1990s to a 2012 peak before falling) — dual axes, both shaded. Pairing a normalized measure with a raw count on independent axes has no principled co-scaling; the visual similarity between the two curves is largely an artifact of the chosen axis windows, and for roughly 20 years (1990s–2012) the two series actually move in opposite directions to what the shared framing implies (#3, #5, #6). It's also the wrong variable for the argument being made — the report's own citation (Lyman Stone) is about marriage predicting *fertility rate*, not aggregate birth counts, which are confounded by population size and migration (addressed at length in the report's own Chapter 6).
- **Figure 1** (dual-axis, births 0–800k / TFR 0–2.5) is scaled so the bars and line track closely, reinforcing the narrative, with the relative axis scaling unexplained (#4).

### What's improved from Report 1

- **Figure 2** (births vs. deaths, projected to 2035) explicitly separates "Actual" from "Projected" with shading and a vertical divider — exactly what Report 1's Figure 1 (pension age extrapolated to 2122) lacked.
- **Figure 5** (permanent childlessness by cohort) shows an explicit **uncertainty fan** (27–36% range) on the projected portion, and the text hedges appropriately: *"Whether this modest reversal represents a sustained trend or a temporary plateau remains to be seen."* This directly fixes the criticism of Report 1's equivalent chart.
- **Figures 6 and 7** show two different trend-extrapolation slopes side by side (recent vs. long-run) rather than presenting one as fact, and only project 3 years forward rather than decades.
