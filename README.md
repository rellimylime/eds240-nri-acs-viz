# Visualizing FEMA National Risk Index Data

## Purpose
This repository contains data visualization work for EDS 240 (Data Visualization & Communication) at UC Santa Barbara's Bren School. The project explores patterns in natural hazard risk across US counties, with analysis progressing from state-level comparisons to demographic disparities within California.

## Repository Contents
```
eds240-nri-acs-viz/
├── README.md
├── HW2.qmd                                      # California vs other states NRI comparison
├── HW2.pdf                                      # Rendered HW2
├── HW3.qmd                                      # NRI + ACS demographic analysis
├── HW3.pdf                                      # Rendered HW3
├── data/                                        # Raw data files (gitignored)
│   ├── National_Risk_Index_Counties_*.csv       # FEMA NRI data
│   └── ACS-1yr-2023-county-race-ethnicity.csv   # Census demographic data
└── .gitignore
```

## Projects

### HW #2: State-Level Risk Comparison
**Research Question:** How does California's natural hazard risk compare to other US states?

**Key Finding:** California has the highest median natural hazard risk score among all 50 US states, with a median NRI score of approximately 95. California counties show consistently high risk scores (85-100 range), substantially higher than other states whose median scores range from approximately 5 to 40.

**Visualization Approach:** Box plot with overlaid individual county points, ordered by state median risk score to highlight California's position as the highest-risk state while showing within-state variation.

### HW #3: Demographic Disparities in Climate Risk
**Research Question:** How does climate hazard risk exposure vary across racial and ethnic groups in California?

**Key Finding:** Asian, Black or African American, and Some Other Race populations show the highest proportions (75-80%) living in Very High risk counties, while Native Hawaiian and Other Pacific Islander populations show the lowest exposure (~50%) to Very High risk areas, though still face substantial hazard exposure.

**Visualization Approach:** Stacked bar chart showing proportional distribution of each racial/ethnic group across FEMA risk categories, ordered by Very High risk exposure to highlight disparities.

## Data Sources

### FEMA National Risk Index
Data from the [FEMA Resilience Analysis and Planning Tool (RAPT)](https://hazards.fema.gov/nri/map). 

To replicate:
1. Navigate to RAPT → click NRI button → find National Risk Index Counties layer
2. Click the three dots → Export to CSV
3. Place the downloaded file in the `data/` directory

Alternatively, access via [Google Drive](https://drive.google.com/file/d/1yoavLSBmJIMjVY9fQrT_rg8u6C-3v_v8/view?usp=sharing).

### American Community Survey (ACS)
Demographic data accessed via the `tidycensus` R package using the US Census Bureau API. Race and ethnicity population estimates from the 2023 ACS 1-year survey for California counties.

**Data Limitation:** ACS 1-year data only includes counties with populations of 65,000+, which excludes California's three Very Low risk counties (Alpine, Modoc, Sierra). This does not meaningfully affect the analysis as these counties contain less than 0.05% of California's population.

## Technical Implementation

**R Packages Used:**
- Data wrangling: `tidyverse`, `janitor`
- Visualization: `ggplot2`, `ggbeeswarm`, `paletteer`, `showtext`
- Census data: `tidycensus`
- File management: `here`

**Key Techniques:**
- Custom color palettes for emphasis and accessibility
- Embedded text labels for cleaner y-axes
- Statistical overlays (box plots + individual points)
- Ordered factors for meaningful visual hierarchies
- Custom fonts via Google Fonts integration

## Author
**Emily Miller** - [GitHub Profile](https://github.com/rellimylime)

Master of Environmental Data Science Candidate, Bren School of Environmental Science & Management, UC Santa Barbara

## References & Acknowledgements
- Course materials developed by Sam Csik for EDS 240
- Data sources: 
  - FEMA National Risk Index (2023 Release, 2025 Release)
  - US Census Bureau American Community Survey (2023)
- Course website: [EDS 240 - Data Visualization & Communication](https://eds-240-data-viz.github.io/)

## License
This project is part of academic coursework and is shared for educational purposes.
