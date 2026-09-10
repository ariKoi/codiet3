# CODIET — Metabolite Biomarkers and Clinical Prediction for Metabolic Syndrome

Analysis documentation for a study of metabolic syndrome in a population-based
cohort, covering the construction of a continuous metabolic risk index and a
clinical prediction model built on it.

**Rendered site:** https://arikoi.github.io/codiet3/

---

Two connected pieces of work are documented here.

The **Composite Metabolic Desirability Index (CMDI)** is a continuous measure of
metabolic risk derived from body mass index, triglycerides, HDL cholesterol and
fasting glucose using multi-response optimisation and Derringer–Suich
desirability functions. It is intended as an alternative to the binary
International Diabetes Federation classification, which reduces a graded
phenomenon to a yes/no decision and treats all qualifying criteria as
interchangeable.

The **clinical prediction model** for that index is fitted with a priority-ordered
variable selection procedure (`bootPriorProc`) across data domains spanning
demographics, dietary indices, physical activity, medication, device-based body
composition, clinical biochemistry, targeted metabolomics, urinary metabolites
and untargeted lipidomics. Validation uses bootstrap resampling clustered by
participant to respect the repeated-measures structure.

The site currently documents the reconstruction of the index following a data
quality problem found in the triglyceride measurements. Further sections will be
added as analyses are completed. The work continues from and is connected to the 
previous version of the analysis, documented at 
https://arikoi.github.io/codiet2/
which is deprecated. 

## Data availability

**No participant data are included in this repository.** The cohort comprises
identifiable human participants, and the raw biochemical, anthropometric,
metabolomic and lipidomic measurements are held separately under the project's
data governance arrangements. Data folders and common data file extensions are
excluded via `.gitignore`.

### Software

Analyses use R with `desirability2` for index construction, `rms` for ordinal
regression modelling and validation, `miceRanger` for random-forest imputation,
and `tidyverse`, `ggplot2` and `patchwork` for data handling and figures. The
site is built with [Quarto](https://quarto.org).

## Status

Work in progress. Numerical results shown on the site are internal working
outputs and should not be cited or treated as final until the corresponding
model refits have been completed and checked.

## Funding and acknowledgements

<!-- To add grant number, funding programme and partner acknowledgements. -->

## License

<!--  MIT for code and CC BY 4.0 for documentation. -->