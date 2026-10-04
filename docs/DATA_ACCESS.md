# Data Access

## Dataset

This research uses data from the 2023–24 Nigeria Demographic and Health Survey (NDHS), obtained through The DHS Program.

## Access

Access to the DHS datasets used in this project was granted through an approved request to The DHS Program.

The original respondent-level datasets are not included in this public GitHub repository.

Researchers who wish to use the data must request access directly from The DHS Program and comply with its terms and conditions.

## Local Data Storage

For this project, authorized datasets are stored locally using the following structure:

- `data/raw/` — original downloaded DHS data
- `data/interim/` — intermediate datasets created during processing
- `data/processed/` — analysis-ready datasets

These respondent-level files are excluded from GitHub through `.gitignore`.

## Reproducibility

Where permitted, this repository will provide:

- Variable-selection documentation
- Data dictionary
- Data-cleaning code
- Preprocessing code
- Analysis notebooks
- Statistical-analysis code
- Machine-learning code
- Model evaluation code
- Instructions for reproducing the analysis after obtaining authorized access to the DHS data

## Data Protection

The DHS datasets will not be redistributed through this repository, and no attempt will be made to identify individual survey respondents.
