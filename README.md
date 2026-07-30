# Product Manager Fit Profiler

A structured self-assessment for working out **which kind** of product management fits you — which archetype of the role, which organisational environment, and which problem domain.

60 items, about 10–12 minutes. One self-contained HTML file. No build step, no dependencies, no network calls, no analytics. Everything stays in the browser tab.

**[▶ Take the assessment](https://boshu9-ux.github.io/pm-fit-profiler/)**

---

## Why this exists

Most PM career advice treats "product manager" as one job. It isn't. The daily work of a pre-product-market-fit founding PM and a platform PM at a large infrastructure company share a title and almost nothing else — different traits load, different motivations sustain you, different environments reward you.

Person–environment fit theory holds that satisfaction and performance come less from ability alone than from the match between a person's dispositions and needs and what a given environment supplies and demands. This tool samples four layers of that match and reports where they point.

## What it measures

| Layer | Items | Constructs |
|---|---|---|
| **Disposition** | 20 | Five trait dimensions drawn from the Five-Factor tradition, narrowed to facets that load on PM work: ambiguity tolerance, execution discipline, assertive influence, consensus orientation, emotional steadiness |
| **Work values** | 16 | What the role must supply to sustain motivation: autonomy, mission, technical craft, commercial drive |
| **Context preference** | 12 | Structural fit: low-process comfort, pace and risk appetite, stakeholder density tolerance |
| **Domain interest** | 12 | Vocational interest across six problem families, mapped to industry shortlists |

Twelve dispositional/value/context scales at four items each, plus six domain scales at two items each. Thirteen items are reverse-keyed to control acquiescence bias.

## What the report produces

- A radar profile of the five dispositional dimensions, plus scored bars for values and context preferences
- **Fit ranking across seven PM archetypes** — 0→1 Explorer, Growth, Platform/Technical, Enterprise B2B, Consumer Experience, Data/AI, Internal Operations — each with where the role lives, what it will cost you, and what to get stronger at
- **Organisational environment ranking** across five stages, from pre-PMF startup to regulated incumbent
- **A top-three industry shortlist** derived from domain interest
- **Tensions to manage** — conditionally generated from combinations in your profile that pull against each other
- **Questions to ask before accepting a role**, derived from your highest-loading needs
- Print/save-to-PDF

## Scoring

Each scale is the mean of its items (reverse-keyed items inverted), rescaled to 0–100. Archetype and environment fit are weighted linear combinations of those scales, with weights summing to 1.0; a `!` prefix in the weight map inverts a scale. Domain scores map directly to industry shortlists.

Verified by running synthetic respondents — constructed to match each archetype's intended profile — through the scoring functions headlessly. All nine recover their intended archetype and environment at rank 1, and a deliberately conflicted profile triggers the expected tension flags.

## Limitations — read these

**Scoring is ipsative.** Scales are compared against each other, not against other people. There is no normative sample, so a score of 70 means "high for you," not "higher than most people." Read the ordering, not the absolute numbers.

**It is short.** Four items per dispositional scale and two per domain gives a directional read, not a precise one. Reliability at this length is adequate for reflection and insufficient for measurement.

**It is self-report.** This measures self-concept, which is correlated with but not identical to behaviour.

**It is not validated.** No criterion validity study has been run against PM performance or tenure outcomes. Treat the output as a structured mirror and a good input to a career conversation, not as a finding.

The tool detects and flags straight-lining, midpoint overuse, and acquiescence bias in the report when they appear.

## Intended use, and what not to use it for

Built for **self-assessment** — a PM or aspiring PM figuring out their own direction — and it's reasonable for a manager and report to work through together in a career conversation.

**Do not use it for hiring or selection.** It has no criterion validity evidence and no adverse-impact analysis. Using an unvalidated instrument to make employment decisions is professionally indefensible under the *Standards for Educational and Psychological Testing* and, in several jurisdictions, legally exposed. Selection use requires a different build.

It is also not a clinical instrument and says nothing about wellbeing or pathology.

## On the frameworks

Every item here is original, and every underlying framework is public domain: the Five-Factor structure (via IPIP-style item writing), vocational interest theory, work-values research, and the Competing Values Framework.

It deliberately contains **no** content from MBTI, DISC, Hogan, StrengthsFinder, or any other proprietary instrument. That's partly a licensing matter — those are trademarked and licensed products — and partly a substantive one: MBTI's type dichotomies have poor test–retest reliability and weak predictive validity for job performance, whereas the Five-Factor structure this borrows from is the better-evidenced base.

## Running it locally

```bash
git clone https://github.com/boshu9-ux/pm-fit-profiler.git
cd pm-fit-profiler
open index.html    # or just double-click it
```

No server required. The file is self-contained.

## Contributing

Useful directions, roughly in order of value:

- **Normative data.** The single biggest upgrade. Anonymous aggregate responses would let scores be reported as percentiles rather than ipsative positions.
- **Reliability estimates.** Cronbach's α or ω per scale, from real response data.
- **Criterion validity.** Correlating profiles against actual PM tenure and satisfaction outcomes.
- **Item refinement.** Items that are double-barrelled, ambiguous, or culturally narrow — open an issue with the item number.
- **Archetype weights.** The weight maps encode judgement about what each role loads on. Disagreement here is welcome and easy to argue with concretely: the weights are all in one place at the top of the script.

## License

MIT — see [LICENSE](LICENSE).
