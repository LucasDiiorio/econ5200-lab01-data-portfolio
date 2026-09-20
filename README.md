# econ5200-lab01-data-portfolio
[README_entry.md](https://github.com/user-attachments/files/32441340/README_entry.md)
## Data Quality Profiling — Big Mac Index

**Objective:** This project audits and corrects a flawed Purchasing Power Parity (PPP) pipeline, quantifying how survivorship bias in panel selection distorts cross-country price comparisons.

**Methodology:**
- Diagnosed and corrected a PPP computation error caused by a transposed numerator/denominator in the exchange-rate ratio
- Identified a survivorship bias risk introduced by discarding countries with incomplete reporting histories ("complete-panel" filtering)
- Quantified the bias by comparing the complete-panel average Big Mac price against the all-available average across all periods
- Developed `profile_dataframe()`, a reusable diagnostic utility that reports panel structure (unit count, period count), completeness (fully-observed units, panel balance), and per-column missingness

**Key Findings:**
- The complete-panel average Big Mac price is **$X.XX (X.X%)** higher than the all-available average, indicating that restricting the sample to countries with complete data systematically skews the average upward
- This divergence held in **XX of 45** periods, suggesting the bias is persistent rather than a one-off artifact of a particular time window
- [Add 1–2 lines here summarizing what `profile_dataframe()` reported on your actual data: e.g. total units, total periods, number of complete units, overall balance %, and any columns with notably high missingness]

---
*Replace all bracketed/bolded placeholder values above with the actual figures from your Part 2 output before publishing.*
