Here’s an updated version of your README file that aligns with the final code provided:

---

# Interactive Map of Survey Respondents

## Overview
This project generates an **interactive heatmap and circle marker map** to visualize the geographical distribution of survey participants based on their Canadian postal codes, specifically focusing on Brampton, Ontario.

## Use Case
The map provides insights into where survey respondents are concentrated within Brampton. This helps businesses, organizations, or analysts identify high-density areas, supporting better outreach strategies, resource allocation, and targeted decision-making.

---

## How It Works

### 1. **Data Cleaning**
   - The script cleans the postal codes from the survey data.
   - It removes invalid characters, standardizes the format (e.g., `A1A1A1` → `A1A 1A1`), and excludes invalid entries.

### 2. **Mapping Postal Codes**
   - Cleaned postal codes are mapped to their **latitude** and **longitude** using a reference file (`CanadianPostalCodes202403.csv`).
   - The script groups data by postal codes and calculates the count of respondents for each location.

### 3. **Interactive Map Generation**
   - Using **Folium**, the script generates an interactive map:
     - **Circle Markers**: Each marker represents a postal code.
       - The size of the circle is proportional to the number of respondents at that postal code.
       - Markers display detailed information on hover, such as postal code and count.

---

## Prerequisites

Before running the script, ensure you have the following installed:
- Python 3.x
- Required libraries:
   ```bash
   pip install pandas folium
   ```

---

## How to Run

1. **Clone the repository**:
   ```bash
   git clone https://github.com/MasegoM94/interactive_map_python.git
   cd interactive_map_python
   ```

2. **Prepare the Input Data**:
   - Place the following files in the same directory:
     - **`fake_postal_codes.csv`**: Input file containing survey data with a column named `postal_code`.
     - **`CanadianPostalCodes202403.csv`**: A reference file containing postal codes, latitude, and longitude. (This file was obtained from the following site (https://www.serviceobjects.com/blog/free-zip-code-and-postal-code-database-with-geocoordinates/) and will require you to disclose what the data will be used for)

3. **Run the Script**:
   Execute the Python script:
   ```bash
   python interactive_map.py
   ```

4. **View the Map**:
   - The generated interactive map will be saved as an HTML file (e.g., `brampton_map.html`).
   - Open the file in a web browser to explore the map.

---

## File Structure

```plaintext
interactive_map_python/
│-- fake_postal_codes.csv       # Input survey data
│-- CanadianPostalCodes202403.csv # Postal code reference file
│-- interactive_map.py          # Main Python script
│-- cleaned_postal_data.csv     # Cleaned postal code output (generated)
│-- brampton_map.html           # Interactive map output (generated)
```

---

## Example Output

- **Postal Code**: M5V 1A1  
- **Count**: 10  
- Circle markers on the map will grow in size based on the respondent count.

---

## Tools and Libraries Used
- **Python**: Data processing and cleaning.
- **Pandas**: For data manipulation and cleaning.
- **Folium**: To create interactive maps and visualize data.

---

## Acknowledgments
This project leverages open-source tools and libraries. Data is provided in CSV format and can be adjusted to suit other locations or use cases.

---

## Future Enhancements
- Add heatmap visualization for higher-level insights.
- Enable dynamic input file selection.
- Allow filtering based on custom regions.
