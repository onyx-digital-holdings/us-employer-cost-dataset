# US Employer Cost Dataset 2026-2027 (Hiring Cost Atlas)

What does an employee really cost a US employer, on top of pay? This dataset collects, for all 50 states, the District
of Columbia, 12 cities with their own rules and the federal level, every official input needed to answer that:

- Federal payroll taxes: Social Security (rate and wage base, 2026 and 2027), Medicare, FUTA and credit-reduction states.
- State unemployment insurance (SUTA): new-employer rate and taxable wage base.
- State employer-paid programs: paid family and medical leave, temporary disability (employer shares and size thresholds).
- State unemployment insurance by industry: new-employer rates by sector (NAICS) where the state sets them.
- Workers' compensation: state premium index per $100 of payroll.
- Employer health coverage: average premiums and employee contributions by state (single and family).
- Paid sick leave mandates: accrual rate and yearly caps by employer size.
- Minimum wage: state and city rates for 2026 and the 2027 rates already announced.
- City rules: local payroll taxes and charges (e.g. NYC MCTMT, Denver OPT, Jersey City payroll tax, Portland TriMet).

**825 values, 64 jurisdictions. Every value has its official source URL, the publishing agency, the effective date and
the date it was last verified.**

Interactive version, calculator and methodology: **[Hiring Cost Atlas by LeadChange Group](https://leadchangegroup.com/research/hiring-cost-atlas/)**
· Employee cost calculator: https://leadchangegroup.com/tools/employee-cost-calculator/

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23587547.svg)](https://doi.org/10.5281/zenodo.23587547)

Also on [Kaggle](https://www.kaggle.com/datasets/leadchangegroup/us-employer-cost-2026-2027-hiring-cost-atlas) and [Zenodo](https://doi.org/10.5281/zenodo.23587547).

Years covered: 2024–2027 · version 2026.10.30

## Files

| File | Content |
|---|---|
| `CHANGELOG.md` | What changed in each version |
| `us-employer-cost-2026-2027.csv` | One row per value (long format) |
| `us-employer-cost-2026-2027.json` | Same data with column descriptions, license and citation |
| `datapackage.json` | Frictionless Data descriptor |

## Columns

| Column | Description |
|---|---|
| `jurisdiction` | State (two-letter code), city or `US` |
| `jurisdiction_type` | `federal`, `state` or `city` |
| `year` | Calendar year the value applies to |
| `measure` | What the value is (e.g. `sui_new_employer_rate`, `minimum_wage`, `social_security_wage_base`) |
| `value` | The number |
| `unit` | `percent`, `usd`, `usd_per_100_payroll`, `usd_per_hour`, `usd_per_month`, `hours`, `employees` |
| `effective` | Date the value applies from (or the survey or study edition) |
| `carried_from_2026` | `1` when the 2027 value is not published yet and the 2026 value is shown |
| `source_url` | Official page the value comes from |
| `publisher` | Agency that publishes it |
| `verified_at` | Day the value was last checked against its source |

## Updates

Values are re-checked against their official sources on a schedule and the live version updates when an agency
changes a figure (2027 rates are added as states announce them). The most current data is always at
https://leadchangegroup.com/research/hiring-cost-atlas/data.csv and through the free read-only API at
https://leadchangegroup.com/api/hiring-cost-atlas/v1/states/.

## License and citation

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/): free to use, share and adapt, including commercially, with
attribution. Please cite as:

> LeadChange Research Team, "Hiring Cost Atlas", LeadChange Group, 2026, https://leadchangegroup.com/research/hiring-cost-atlas/ (DOI: 10.5281/zenodo.23587547)

Estimates for planning only; not tax or legal advice. Found an error? Tell us through the correction link on the
atlas page.
