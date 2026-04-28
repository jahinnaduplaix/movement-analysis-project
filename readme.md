# Range of Motion Analysis Project

**Student:** DUPLAIX JAHINNA

## Project overview

This project analyses the effect of a prevention program on two range-of-motion outcomes in leather workers:
- wrist extension
- forearm supination

The workflow is divided into two complementary parts:
- **Python** is used for data cleaning, data validation, outcome preparation, and exploratory outputs
- **RStudio** is used for the final statistical analyses and the final report

---

## Objective

The main objective of the project is to prepare and analyse repeated range-of-motion measurements collected at two timepoints:
- **T0**: baseline
- **T1**: follow-up

The project aims to:
- clean and validate the dataset
- verify the longitudinal structure of the data
- create a complete-case analysis dataset
- compute change scores between `T0` and `T1`
- produce descriptive and exploratory outputs
- perform the final statistical analyses in RStudio

---

## Project structure

```text
DUPLAIX.JAHINNA/
│── readme.md
│── requirements.txt
│── main.ipynb
│── main.Rmd
│── main.Rproj
├── data/
│   ├── raw/
│   │   └── TMinstitute_prevention_base_2025.xlsx
│   └── processed/
│       └── analysis_dataset.csv
└── results/
    ├── figures_exploratory/
    └── tables_exploratory/
```

## Dataset

The project is based on a range-of-motion dataset containing repeated measurements for each participant at two timepoints:
- **T0**: baseline
- **T1**: follow-up

The cleaned long-format dataset is used to verify the structure of the repeated measurements before reshaping the data into wide format.

The final analysis dataset contains one row per participant and complete paired measurements for both movement outcomes.

---

## Python workflow

The Python notebook is used to:

1. read and inspect the raw dataset
2. clean and standardize the variables
3. identify implausible raw values
4. remove exact duplicate rows
5. inspect incomplete observations
6. verify the longitudinal structure of the dataset
7. exclude participants with an invalid longitudinal structure
8. reshape the valid dataset into wide format
9. create the final complete-case analysis dataset
10. compute the primary outcome variables
11. inspect extreme change scores
12. produce descriptive tables and exploratory figures
13. export the final dataset for the statistical analyses in RStudio

---

## Main variables

The final analysis dataset includes the following variables:

- `participant_id`: participant identifier
- `wrist_extension_deg_T0`: wrist extension at baseline
- `wrist_extension_deg_T1`: wrist extension at follow-up
- `forearm_supination_deg_T0`: forearm supination at baseline
- `forearm_supination_deg_T1`: forearm supination at follow-up
- `delta_wrist_extension_deg`: wrist extension change between `T0` and `T1`
- `delta_forearm_supination_deg`: forearm supination change between `T0` and `T1`

The delta variables are computed as:
- `delta_wrist_extension_deg = wrist_extension_deg_T1 - wrist_extension_deg_T0`
- `delta_forearm_supination_deg = forearm_supination_deg_T1 - forearm_supination_deg_T0`

---

## Data cleaning and preparation

The Python workflow includes the following cleaning and preparation steps:
- standardization of participant identifiers
- harmonization of timepoint labels
- conversion of movement variables to numeric format
- identification of implausible raw values
- removal of exact duplicate rows
- inspection of incomplete rows
- validation of the longitudinal structure
- exclusion of participants with invalid repeated-measure structure
- creation of a complete-case analysis dataset

Participants with:
- an invalid longitudinal structure
- or incomplete movement data

are excluded before the final statistical analyses.

---

## Exploratory outputs

Python produces:
- a descriptive summary table of the main movement variables
- global histograms of the primary outcome variables
- central-range histograms of the primary outcome variables

These outputs are saved in:
- `results/tables_exploratory/`
- `results/figures_exploratory/`

---

## Final analysis dataset

The processed dataset exported by Python is:
- `data/processed/analysis_dataset.csv`

This file is used as the input dataset for the statistical analyses performed in RStudio.

---

## Statistical analyses

The final statistical analyses are performed in **RStudio** from the processed dataset exported by Python.

These analyses are implemented in:
- `main.Rmd`

The final HTML report will also be generated from `main.Rmd`.

---

## Software and libraries

### Python

The Python part uses:
- `pandas`
- `matplotlib`
- `numpy`
- `pathlib`

### R / RStudio

The R part is developed in:
- `R`
- `RStudio`

Additional R packages will be listed in `main.Rmd`.

---

## Reproducibility

The project is designed to be reproducible.

The recommended order is:

1. run `main.ipynb` to clean and prepare the dataset
2. use the exported processed dataset in `main.Rmd`
3. knit `main.Rmd` to generate the final HTML report

---

## Current status

At this stage:
- the Python data cleaning and preparation workflow has been completed
- the final analysis dataset has been exported
- the next step is to perform the final statistical analyses in RStudio