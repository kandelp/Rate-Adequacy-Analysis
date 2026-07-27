# Rate Adequacy & Loss Development Analysis

A chain-ladder rate adequacy study of five major U.S. property-casualty insurers, built from public Schedule P annual statement filings.

## Companies Studied
Allstate · Farmers Insurance · Travelers · Zurich · Liberty Mutual

## Lines of Business
- Combined (All Lines)
- Homeowners / Farmowners
- Private Passenger Auto Liability/Medical
- Commercial Auto/Truck Liability/Medical
- Workers' Compensation
- Commercial Multiple Peril

## Methodology

1. **Loss triangles** — Cumulative net loss triangles for accident years 2016–2025 were built from each insurer's Schedule P disclosures, split into the six lines of business above.
2. **Development factors** — Volume-weighted age-to-age loss development factors (LDFs) were calculated for each triangle and chained into age-to-ultimate factors (the chain-ladder method).
3. **Ultimate losses & loss ratio** — Latest-diagonal losses were multiplied by the age-to-ultimate factor to estimate ultimate losses (and the implied reserve) for each accident year, then divided by earned premium to get the indicated loss ratio.
4. **Rate adequacy verdict** — Each company-line's own 10-year average indicated loss ratio was used as its benchmark. A given year is scored:
   - **Roughly Adequate** — within ±5 points of the average
   - **Undercharged** — more than 5 points above average (losses running hotter than premium supports)
   - **Overcharged** — more than 5 points below average (premium exceeds the loss trend)

**Note:** the benchmark is each line's own historical average, not a regulator-approved target or a competitor's pricing — verdicts describe deviation from a company's own long-run norm, not an absolute profitability judgment.



Each workbook contains four sheets:
1. Loss development triangles (by line of business)
2. Year-to-ultimate loss development factors
3. Loss reserve and loss ratio (chain-ladder ultimate)
4. Rate adequacy verdict (vs. 10-year average)

## Key Findings

- All five companies trace the same underwriting cycle: a 2020 pandemic-driven dip (overcharged), a 2022–23 inflation shock (undercharged), and a 2025 hard-market correction (overcharged again, the most one-sided year in the dataset).
- Commercial Auto/Truck Liability/Medical is a clear outlier for Allstate and Zurich, averaging 85%+ indicated loss ratios.
- Workers' Compensation is the most stable line across all companies that report it.
- Travelers shows the lowest volatility and the highest share of "roughly adequate" years of the five.

Full write-up with charts, company-by-company breakdowns, limitations, and suggested next steps is in `Rate_Adequacy_Analysis_Report.pdf`.

## Data Source

All figures are derived from publicly filed Schedule P annual statement exhibits. No proprietary or non-public data is used.

## Known Gaps

Three company-line combinations had insufficient Schedule P detail to support a triangle and were excluded rather than estimated:
- Allstate — Workers' Compensation
- Farmers — Combined All Lines
- Zurich — Private Passenger Auto Liability/Medical

## Possible Extensions

- Layer in a Bornhuetter-Ferguson estimate alongside the pure chain ladder for the least-mature accident years
- Benchmark against industry-wide loss ratios (e.g., NAIC/A.M. Best) instead of each company's own average
- Automate the workbook-to-verdict pipeline in Python (pandas + a chain-ladder function)
