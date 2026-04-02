# Movement analysis project

## Project aim
This project investigates the effect of a prevention program on two distal upper-limb range of motion variables in leather workers:
- wrist extension
- forearm supination

The main objective is to analyse the change between baseline (T0) and follow-up (T1).

## Data
The input dataset is stored in the `data/` folder.

Main file:
- `TMinstitute_prevention_base_2025.xlsx`

Sheet used for the analyses:
- `range_of_motion`

Main variables:
- `participant_id`
- `timepoint`
- `wrist_extension_deg`
- `forearm_supination_deg`

## Project structure
- `data/` : input data
- `results/` : cleaned datasets, tables, and figures
- `main.ipynb` : entry point for Python analyses
- `main.Rmd` : entry point for R analyses

## Python analyses
Python is used to:
- import the raw data
- clean the dataset
- standardize labels
- handle missing values and duplicates
- create derived variables
- to produce exploratory figures
- export a cleaned dataset

## R analyses
R is used to:
- describe the variables at T0 and T1
- analyse the change between T0 and T1
- perform paired statistical tests
- produce final tables and figures

## Outputs
The main outputs are stored in the `results/` folder:
- cleaned datasets
- descriptive tables
- statistical results
- boxplots and other figures