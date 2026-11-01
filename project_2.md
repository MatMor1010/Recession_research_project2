# Does the Excess Bond Premium Still Forecast Recessions? A Recent-Sample Null/Boundary Test

- Student: Moreau, Matthieu
- Assignment: Project 2
- Proposal ID: A05-21
- Official area: A05 — Credit & fixed income
- Official category: C3 — Rates, credit, derivatives & macro
- Data not ready: 33.3%
- Estimated data not available locally: 16.7%

## Main research question

Built from library spreads, does an excess-bond-premium proxy retain out-of-sample recession / industrial-production forecasting power in the recent sample?

## Testable hypothesis

H0 (boundary): the EBP proxy's OOS recession-forecasting edge is weaker/less robust in the 2015-2025 sample than in the original Gilchrist-Zakrajsek window.

## Why this project was selected

The project offers recent or out-of-sample evidence, economic implementability, strong inference discipline. Its hypothesis is falsifiable and the required market data can be assembled without asking the student to acquire high-frequency data.

## Study design

- Primary assets: US IG/HY spreads; USREC; industrial production.
- Traditional method: Construct an index-level EBP proxy (spread minus predicted-default component); probit/OOS forecasts of recession/IP; Clark-West vs benchmark; HAC SEs; FDR.
- ML or robustness method: Penalized/RF recession classifier from EBP + controls under purged+embargoed CV vs a spread-level baseline; DSR/PBO. Robustness only.
- Sample or event window: 1999-2025 monthly; OOS from 2015.
- Expected result type: honest-null / boundary-condition.
- Proposal feasibility: GO-after-pull (🔌 issuer-level EBP; index proxy ✅ now)

## Data plan

### Bloomberg acquisition by the student

Issuer-level corporate-bond OAS/yield, duration, maturity, rating, liquidity and macro controls.

The Bloomberg extraction must be end-of-day, daily, weekly, monthly, quarterly, annual, document, or event/reference data only. Record terminal function, security or series identifier, field, frequency, date range, currency, adjustment convention and extraction date in a source log.

### Data already available in RiskLab

1. IG / HY spreads -> CF-07 / CF-08 / CF-11 [local] (index EBP proxy)
2. Mixed local/external: issuer-level inputs for a true GZ EBP -> 02_market/fixed_income [not local BBG/WRDS panel]
3. recession / IP -> 04_macro/USREC, US_IndustrialProduction_YOY_Monthly [local]

### Local data needing preparation

None identified.

### Data not currently available locally

1. Mixed local/external: issuer-level inputs for a true GZ EBP -> 02_market/fixed_income [not local BBG/WRDS panel]

### High-frequency data rule

No high-frequency Bloomberg extraction is authorized. If high-frequency data becomes useful later, check `C:\risklab\data\intraday_data` first and use only the local archive.

## Minimum outputs

1. A source and field dictionary for every Bloomberg series and every local file used.
2. A reproducible cleaning and merge script with point-in-time and adjustment conventions stated explicitly.
3. Descriptive coverage, missingness and identifier-join diagnostics before estimation.
4. The traditional specification, the stated robustness method and economically interpretable effect sizes.
5. A concise paper draft that preserves null or failed results and distinguishes exploratory from confirmatory analysis.
