# Range of Motion Analysis Project

## Project overview

This project focuses on the cleaning, preparation, and exploratory analysis of a range-of-motion dataset collected at two timepoints (T0 and T1).

The Python workflow was used to:
- inspect the raw dataset,
- clean and standardize the variables,
- identify and handle implausible raw values,
- verify the longitudinal structure of the data,
- reshape the dataset into wide format,
- create the final analysis dataset,
- compute individual change scores,
- produce descriptive tables and exploratory figures,
- export the final dataset for statistical analyses in RStudio.

The statistical analyses and additional final figures will be performed in RStudio.

---

## Objective

The main objective is to describe and prepare the dataset for the comparison of wrist extension and forearm supination between T0 and T1.

At this stage, the Python notebook is used for:
-  data cleaning,
- descriptive analyses,
- exploratory visualizations,
- export of the final analysis dataset.

No formal statistical interpretation is made in Python.

---

## Dataset

The project is based on a range-of-motion dataset containing repeated measurements for each participant at two timepoints:
- **T0**: baseline
- **T1**: follow-up

The final analysis dataset includes one row per participant and complete paired measurements for both movement outcomes.

---

## Main variables

The main variables used in the final analysis dataset are:

- `participant_id`: unique participant identifier
- `wrist_extension_deg_T0`: wrist extension at baseline
- `wrist_extension_deg_T1`: wrist extension at follow-up
- `forearm_supination_deg_T0`: forearm supination at baseline
- `forearm_supination_deg_T1`: forearm supination at follow-up
- `delta_wrist_extension_deg`: change in wrist extension between T0 and T1
- `delta_forearm_supination_deg`: change in forearm supination between T0 and T1

The delta variables are computed as:

- `delta_wrist_extension_deg = wrist_extension_deg_T1 - wrist_extension_deg_T0`
- `delta_forearm_supination_deg = forearm_supination_deg_T1 - forearm_supination_deg_T0`