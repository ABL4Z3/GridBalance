# Public source and license

## Source

U.S. Energy Information Administration (EIA), EIA-930 hourly balancing
authority data, six-month files:

- https://www.eia.gov/electricity/gridmonitor/sixMonthFiles/EIA930_BALANCE_2022_Jan_Jun.csv
- https://www.eia.gov/electricity/gridmonitor/sixMonthFiles/EIA930_INTERCHANGE_2022_Jan_Jun.csv
- https://www.eia.gov/electricity/gridmonitor/sixMonthFiles/EIA930_BALANCE_2023_Jan_Jun.csv
- https://www.eia.gov/electricity/gridmonitor/sixMonthFiles/EIA930_INTERCHANGE_2023_Jan_Jun.csv
- https://www.eia.gov/electricity/gridmonitor/sixMonthFiles/EIA930_BALANCE_2024_Jan_Jun.csv
- https://www.eia.gov/electricity/gridmonitor/sixMonthFiles/EIA930_INTERCHANGE_2024_Jan_Jun.csv

Accessed 2026-09-19; all URLs verified HTTP 200 at build time. No API key
or registration required.

## License

EIA information products are works of the U.S. federal government and are
in the public domain in the United States (17 U.S.C. §105). EIA requests
citation: "Source: U.S. Energy Information Administration, EIA-930 Hourly
Electric Grid Monitor."

## Derivation

From the interchange files, dual-reported balancing-authority (BA) pairs
are averaged into canonical signed tie flows. From the balance files,
hourly demand and net generation by fuel group are taken as covariates.
Cases aggregate case-local random groups of 1-2 BAs into zones, so zone
quantities are sums of real reported values; zone net interchange is
defined as the exact sum of shipped incident tie flows (observed plus
hidden gold). All values are divided by a per-case scale factor. BA
identities, dates, regions, and absolute magnitudes are not shipped;
aliases are randomized per case.
