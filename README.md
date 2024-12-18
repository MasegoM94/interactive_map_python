# Interactive Map of Survey Respondents

## Overview
This project generates an interactive map to visualize the geographical distribution of survey participants based on their Canadian postal codes (more specifically in Brampton, Ontario).

## Use Case
The map helps the user to understand where survey respondents are concentrated in Brampton, Ontario. It provides insights into respondent density, allowing for better outreach strategies and resource allocation.

## How It Works
1. **Data Cleaning and Preparation**: 
   - Survey data (postal codes) is cleaned and matched with latitude/longitude.
2. **Interactive Map**:
   - The map uses circle markers to represent response density. The size of the marker reflects the number of responses for a postal code.
3. **Tools Used**:
   - Python libraries: `pandas`, `folium`

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/MasegoM94/interactive_map_python.git
