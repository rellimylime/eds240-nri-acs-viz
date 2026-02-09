# Visualizing FEMA National Risk Index Data

## Purpose
This repository contains data visualization work for EDS 240 (Data Visualization & Communication) at UC Santa Barbara's Bren School. The project explores patterns in natural hazard risk across US counties and examines how climate risk exposure varies across racial and ethnic groups in California.

## Repository Contents
```
eds240-nri-acs-viz/
├── README.md
├── HW2.qmd                                      # Initial NRI exploration
├── HW2.pdf                                      # Rendered HW2
├── HW3.qmd                                      # NRI + ACS demographic analysis
├── HW3.pdf                                      # Rendered HW3
├── data/                                        # Raw data files (gitignored)
│   ├── National_Risk_Index_Counties_*.csv       # FEMA NRI data
│   └── ACS-1yr-2023-county-race-ethnicity.csv   # Census demographic data
└── .gitignore
```

**HW #2**: Visualizations analyzing FEMA National Risk Index scores across all US states

**HW #3**: Integration of American Community Survey (ACS) demographic data to examine climate risk exposure disparities across racial and ethnic groups in California

## Data Sources

### FEMA National Risk Index
Data comes from the [FEMA Resilience Analysis and Planning Tool (RAPT)](https://hazards.fema.gov/nri/map). 

To replicate:
1. Navigate to RAPT → click NRI button → find National Risk Index Counties layer
2. Click the three dots → Export to CSV
3. Place the downloaded file in the `data/` directory

Alternatively, access via [Google Drive](https://drive.google.com/file/d/1yoavLSBmJIMjVY9fQrT_rg8u6C-3v_v8/view?usp=sharing).

### American Community Survey (ACS)
Demographic data accessed via the `tidycensus` R package using the US Census Bureau API. Race and ethnicity population estimates come from the 2023 ACS 1-year survey for California counties.

**Note:** ACS 1-year data only includes counties with populations of 65,000+, which excludes California's three Very Low risk counties (Alpine, Modoc, Sierra).

## Key Findings
Analysis reveals substantial disparities in climate hazard risk exposure across racial and ethnic groups in California. Asian, Black or African American, and Some Other Race populations show the highest proportions (75-80%) living in Very High risk counties, while Native Hawaiian and Other Pacific Islander populations show the lowest exposure (~50%) to Very High risk areas.

## Author
**Emily Miller** - [GitHub Profile](https://github.com/rellimylime)

Master of Environmental Data Science Candidate, Bren School of Environmental Science & Management, UC Santa Barbara

## References & Acknowledgements
- Course materials developed by Sam Csik for EDS 240
- Data sources: 
  - FEMA National Risk Index (2023 Release)
  - US Census Bureau American Community Survey (2023)
- Course website: [EDS 240 - Data Visualization & Communication](https://eds-240-data-viz.github.io/)

## License
This project is part of academic coursework and is shared for educational purposes.