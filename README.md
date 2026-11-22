# NHS Community Pharmacy Flu Vaccinations: December 2025 Report (Sep–Dec 2025)

An exploratory data analysis (EDA) of the NHS Community Pharmacy Adult Seasonal Influenza Vaccination Service, using the NHSBSA report for December 2025, which covers vaccinations given from September to December 2025.

## Data

The data is the NHSBSA Community Pharmacy Adult Seasonal Influenza Vaccination Service report for December 2025, for pharmacy contractors. It has about 25,000 rows, each showing one pharmacy's use of one vaccine product, with the number of vaccines given and their cost.

- Dataset: [December 2025 report](https://opendata.nhsbsa.net/dataset/community-pharmacy-adult-seasonal-influenza-vaccination-service-report-pharmacy-contractors/resource/792613ac-7561-4757-8c05-71e850445f04)
- Info page: [NHSBSA open data portal](https://opendata.nhsbsa.net/dataset/community-pharmacy-adult-seasonal-influenza-vaccination-service-report-pharmacy-contractors)

The service runs from September to March each year and aims to reduce unplanned hospital admissions and pressure on A&E. I chose the dataset as a real-world public dataset of manageable size for practising exploratory data analysis.

## Analysis approach

- Workflow: ingestion, validation, cleaning, calculation and visualisation.
- Validation established that each row is one pharmacy's use of one vaccine product, before any totals were calculated.

## Findings

- £80 million was spent on vaccine products through the service from September to December 2025.
- Spend is concentrated: three of the seven vaccine products (identified by BNF presentation code) account for 97%.
- One manufacturer, Seqirus UK Ltd, receives 83% of total spend.

## Limitations

- One report covering September to December only, so the flu season (which runs to March) is incomplete.
- No population or eligibility figures, so uptake can't be compared between areas.
- Products are identified by BNF code rather than vaccine name in the source data.
- Pharmacy-level data only: no patient-level detail, and vaccinations given by GPs are not included.

## Power BI version

The two main charts were rebuilt in Power BI (`flu_vaccinations_dec2025.pbix`), with a comparison of the two versions in my [Power BI training log](https://github.com/TomSCarter/powerbi_training_log/tree/main/01_flu_vaccination_visual).

## Project structure

```text
├── data/                                # Raw CSV goes here (git-ignored)
├── notebooks/
│   └── flu_vaccinations_dec2025.ipynb   # Main analysis notebook
├── flu_vaccinations_dec2025.pbix        # Power BI version of the main charts
├── .gitignore
└── README.md
```

## Setup and running

1. Install the requirements: pandas, NumPy, Matplotlib and seaborn.
2. Download the December 2025 CSV from the dataset link above and place it in `data/`.
3. Run the notebook from top to bottom.