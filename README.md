# Haverhill, MA Property Tax and Cost of Living Analysis

A data-driven analysis of property tax increases and cost of living changes in Haverhill, Massachusetts from 2017 to 2025.

## Overview

This analysis examines how property taxes have increased for the average single-family homeowner in Haverhill, MA over an 8-year period and compares those increases to the general cost of living.

## Key Findings

- **Property taxes increased 31.0% from 2017-2025** ($1,425 cumulative increase)
- **Cost of living increased ~17.2%** over the same period
- **Property taxes grew 1.8x faster than cost of living**
- The highest single-year increase was **$263 in 2025**
- Recent trends (2024-2025) show property taxes increasing **2.4x faster** than cost of living

### Income Required to Keep Up

To maintain the same standard of living in Haverhill from 2024-2025, residents would need:

- **Single person**: ~$1,239/year in additional pre-tax income (annual average)
- **Family of four**: ~$2,374/year in additional pre-tax income (annual average)

## Data Sources

### Property Tax Data
- City of Haverhill official property tax records
- City of Haverhill Budget and Finance Department

### Specific Sources by Year
- **2017-2023**: Eagle Tribune article (November 17, 2022)
- **2024**: Eagle Tribune article (November 29, 2023)
- **2025**: WHAV News article (November 18, 2025) - City Council vote

### Cost of Living Data
- [Salary.com Cost of Living Calculator](https://www.salary.com/research/cost-of-living/haverhill-ma)
- Assumes consistent 2% annual increase based on reported data

### Current Tax Information (FY 2025)
- Residential Tax Rate: $10.71 per $1,000 assessed value
- Average Single-Family Home Value: $561,903
- Source: City of Haverhill official website

## Usage

### Running the Analysis

```bash
python3 haverhill_tax_analysis.py
```

### Exporting Data

The script will prompt you to export the raw data to CSV format:

```bash
Export data to CSV? (y/n): y
```

This creates `haverhill_tax_data.csv` with year-by-year increases.

## Methodology

### Property Tax Calculations
- Uses actual year-over-year increases in average single-family home tax bills
- Baseline 2017 tax bill estimated by working backwards from current data
- Percentage increases calculated against the 2017 baseline

### Cost of Living Calculations
- Assumes 2% annual increase (conservative estimate based on available data)
- Compounds annually using formula: `(1 + rate)^years`
- 2025 baseline: $36,456/year (single), $80,280/year (family of four)

### Income Calculations
- Effective tax rate: 25% (federal + state combined estimate)
- Pre-tax income needed calculated as: `after-tax expense / (1 - tax_rate)`
- Accounts for both property tax increases and general cost of living increases

## File Structure

```
.
├── haverhill_tax_analysis.py    # Main analysis script
├── README.md                     # This file
└── haverhill_tax_data.csv       # Generated CSV (if exported)
```

## Requirements

- Python 3.6 or higher
- No external dependencies required (uses only standard library)

## Important Notes

1. **Property values vary**: This analysis uses the average single-family home value. Individual experiences will vary based on actual home value.

2. **Tax rate vs. tax bill**: The analysis focuses on actual tax bill increases, not just rate changes. Property value reassessments significantly impact individual bills.

3. **Cost of living assumptions**: The 2% annual COL increase is an estimate. Actual COL increases may vary by household spending patterns.

4. **Compounding effect**: Each year's tax increase is permanent and compounds. A $263 increase in 2025 means $263 more every subsequent year, plus additional increases.

5. **Effective tax rates**: The 25% effective tax rate is an estimate. Individual tax situations vary based on deductions, filing status, etc.

## Context and Background

### Why Property Taxes Are Rising

According to City Council records and mayor's budget statements, the increases are driven by:
- Employee health insurance premium increases (12.5% in FY 2025)
- Collective bargaining agreements
- School funding needs (35% of revenue increase from state Chapter 70 aid)
- Debt service for capital projects (including the Consentino Middle School)
- Decreased federal ARPA funds
- Infrastructure and maintenance needs

### Tax Classification

Haverhill uses a split tax rate system:
- Residential properties pay at one rate
- Commercial/industrial properties pay at a higher rate (65% more)
- The City Council votes annually on this classification split

## License

This analysis is provided for informational purposes. Data sources are publicly available and credited appropriately.

## Contributing

If you have additional data sources or corrections, please feel free to submit issues or pull requests.

## Disclaimer

This analysis is based on publicly available data and news reports. For official tax information, please consult:
- City of Haverhill Assessor's Office: (978) 374-2300
- City of Haverhill website: https://www.haverhillma.gov/

---

*Last Updated: November 19, 2025*
