# Extreme heat and cause-specific risk of hospital admission in the adult population in England: a case time series analysis

[![DOI](https://doi.org/10.5281/zenodo.19865006)](https://doi.org/10.5281/zenodo.19865006)

Partially reproducible code performing the analysis reported in the paper:

> Flower G, Cole R, Libardi ADLC, *et al*. Extreme heat and cause-specific risk of hospital admission in the adult population in England: a case time series analysis. *BMJ Open* (2026). [10.1136/bmjopen-2025-105321](https://doi.org/10.1136/bmjopen-2025-105321)

## Scripts

The scripts are run in order. Script 01 should be run first to set up the
packages and parameters. Scripts 02 and 03 prepare the data and run the first stage
analysis, these require the HES data and cannot be reproduced here. Scripts 04 to 05 
can be run by loading results of the first stage saved beforehand. This reproduced
the main results from the study. Scripts 06 and 07 contain the sensitivity analyses
and can be reproduced from the second stage (line 166).

| Script | Descriptions |
| :--- | :--- |
| `01.pkg_param.R` | Load the necessary R libraries and defines all the analysis parameters. |
| `02.prepmain.R` | Load and prepare the environmental and hospital admissions data |
| `03.firststage.R` | Centrepiece of the analysis. Loops through the causes and age groups to perform the case time series and produce the LAD level ERF.| 
|`04.secondstage.R` | Runs the meta analysis pooling the results to obtain a single national ERF.|
| `05.plots.R` | Produces plots featured in the main text of the article and supplementary plots related to the main analyses.|
| `05b.plothosp.R` | Produces plots using the HES data and cannot be reproduced here.|
| `06.sensitivity_knot.R` | Reproduces the stages in scripts 03-05 for the sensitivity analysis on knot placement.|
| `07.sensitivity_lag.R` | Reproduces the stages in scripts 03-05 for the sensitivity analysis on lag length.|
