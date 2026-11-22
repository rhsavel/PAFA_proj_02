# PAFA Project 02

Python analysis of the PAFA postmortem study, examining associations between PAFA questionnaire responses and clinical and pathological parkinsonism diagnoses.

## Analysis notebook

- `PAFA_analysis_2026_11_21.ipynb` — data preparation, scoring checks, and correlation heatmap generation.

## Workflow

1. Load the source PAFA clinical dataset and remove a block of original raw clinical variables (dataset v04).
2. Recode primary pathological diagnosis categories 4 and 5 into category 9, labeled Lewy body disease (v05).
3. Compare alternative methods of combining three physicians' PAFA assessments.
4. Calculate the median response across three physician ratings for each of 36 binary PAFA questions, and the mean of physician total, motor, and nonmotor scores (v06).
5. Build a focused analysis dataset containing patient identifiers, PAFA question medians, scores, and clinical/pathological diagnosis categories (v07).
6. Generate correlation heatmaps comparing PAFA items, domains, and summary scores with clinical and pathological diagnoses. The latest heatmap revision (v09) displays 34 individual questions after excluding lower motor neuron signs and cortical sensory loss, and generates 10 PNG figures at 600 DPI.

## Python dependencies

- pandas
- numpy
- matplotlib
- seaborn
- scipy
- statsmodels

## Running the analysis

Open the notebook in Jupyter and execute its cells in sequence. The code references local CSV datasets named `AllPAFA_Clinical_OrigOnset_2026-11-18_wide_v03.csv` through `..._v07.csv`. These datasets are **not included** in this repository and must be made available in the working directory to reproduce the analysis. Some later visualization cells rely on functions and variables defined in earlier cells.

## Data privacy

The repository is intended for analysis code and shareable, reviewed outputs. Do not upload patient-level data, identifiers, or confidential research datasets to this public repository. Review figures and notebook outputs for potentially identifying information before publishing.

## Status

Analysis notebook dated November 21, 2026. Research work in progress; findings and figures should not be interpreted as peer-reviewed results.
