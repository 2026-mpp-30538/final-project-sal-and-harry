# Chicago Crime, Social Vulnerability and Welfare Metrics Analysis

This project anaysis looks at the intersection between Social Vulnerability Index (SVI) data, Health Atlas measures, and violent crime in Chicago. 

## Data Sources 
1) Chicago Health Atlas: https://chicagohealthatlas.org/indicators — 
Provides ZIP-code-level social and health indicators including: Poor mental health prevalence, lack of social/emotional support, Childhood Opportunity Index, Hardship Index, Behavioral health hospitalization rates. Analyzed to assess violence predictivity of self-reported and professionally aggregated metrics. These variables are used in the Streamlit dashboard.
2) Chicago Police Department CLEAR: https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-Present/ijzp-q8t2/about_data —
Filtered to 2021-2025 and only violent crime: Sexual Assault, Assault, Battery, and Homicide. Includes and sorted by date/time, geography (latitute and logitude), and offense type and details.
3) CDC SVI: https://www.atsdr.cdc.gov/place-health/php/svi/index.html —
2022 Illinois dataset; measures the vulnerability of communities based on: socioeconomic status, demographic information, household composition, housing characteristics, and access to transportation. We use census-tract and ZIP-code-level SVI scores to group neighborhoods into vulnerability categories.

### Important: Required Large Files *not* in Github Repo that Must be Installed: 
https://drive.google.com/drive/folders/1AgjG-eKVSHtqHBCz1qplsBwrZigxKWy6?usp=sharing. \n
Both Required files 'crimes_with_tracts.csv' and 'crime_svi_merge_no_na.csv' must be added to BASE_PATH/data/derived_data. They have been added to .gitignore to prevent issues in git function. 

## Setup
Install the required Python environment:

```bash
conda activate DAP
pip install -r requirements.txt
```

## Project Structure
(Note: Tree format not compatible; brew not functioning properly. Description in its stead.)
Data is split between derived_data and raw_data within the data folder. Exploratory code files, which include extra visualizations and scripts, are predominantly found in the code_work folder. The final project .qmd, .pdf, and .html are in the final_project folder. Our streamlist app, 'testapp.py', is in our main directory, along with svi_plots.qmd, which is needed due to relative pathing error-fix requirement. 

Importantly, you should **not** need to run any preprocessing file for final_project.qmd or the dashboard (see below) to run properly. Other visualizations and our code progress can be seen and analyzed in the non-final_project qmd files in the repository (e.g. svi_plots.qmd, etc.). 

## Dashboard Link: https://apprepository-s2kxjajnqkzwyg8ys7j2hm.streamlit.app/
Note: Streamlit apps need to be “woken up” if they have not been run in the last 24 hours.
