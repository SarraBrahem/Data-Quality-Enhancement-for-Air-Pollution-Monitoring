# Data-Quality-Enhancement-for-Air-Pollution-Monitoring

## Description
This project addresses the evaluation and improvement of data quality in the context of air pollution monitoring. Using the **Talend** ETL tool, we implemented workflows to process, clean, and integrate data from multiple heterogeneous sources. The resulting dataset supports accurate environmental analysis and informed decision-making.

---

## Features
### **Key Objectives**
- **Data Integration**: Combining data from fixed stations and mobile sensors.
- **Quality Evaluation**: Identifying and addressing issues such as:
  - Missing values
  - Data duplication
  - Non-standard formats
  - Granularity discrepancies
- **Data Quality Improvement**: Implementing transformations to:
  - Normalize data
  - Eliminate duplicates
  - Harmonize scales
  - Ensure completeness and consistency

### **ETL Workflow**
1. **Data Sources**:
   - Fixed station measurements (e.g., pollutant levels, station details).
   - Mobile sensor data (e.g., geolocation, pollutant levels).
   - Pollutant metadata (e.g., descriptions, tolerance thresholds).

2. **ETL Steps**:
   - **Extraction**: Loading data from multiple sources.
   - **Transformation**:
     - Cleaning missing values by interpolation or default metrics.
     - Merging duplicate records and normalizing formats.
     - Calculating daily averages and pollutant statuses.
   - **Load**: Consolidating results into unified tables for analysis.

3. **Outputs**:
   - Consolidated tables for cities like Paris, Hauts-de-Seine, and Yvelines, including:
     - Daily pollution averages
     - Station and sensor counts
     - Pollution status (e.g., "Normal" or "Alert")

---

## Project Structure
- **Schema**: Target schema includes:
  - **Pollutants**: Type, average concentration, and tolerance.
  - **Stations**: Details on fixed stations (location, contact).
  - **Sensors**: Mobile data linked with geolocation.
- **Workflow Implementation**:
  - Talend jobs for transformation, grouping, and aggregation.
  - Intermediate and final tables for reporting.

---

## Installation and Setup
1. **Requirements**:
   - Talend Open Studio (latest version recommended).
   - Access to data sources in CSV or database format.

2. **Steps**:
   - Import the Talend job files into Talend Studio.
   - Update the paths to point to your local or remote data sources.
   - Run the ETL workflow jobs (`Transformation Job`, `Grouping Job`) in sequence.

3. **Output Tables**:
   - `Stations`
   - `Measurements`
   - `Pollutant Status`

---

## Example Scenarios
- **Complete Workflow**:
  1. Start with raw data files for fixed stations, mobile sensors, and pollutants.
  2. Execute Talend jobs for cleaning and integration.
  3. Review consolidated tables with pollutant status per city.

- **Handling Missing Data**:
  - Replace missing pollution levels with calculated averages for the same pollutant type.

- **Duplicate Elimination**:
  - Identify and retain the most reliable records by comparing data completeness.

---

## Challenges Addressed
- **Completeness**: Ensuring no critical values are missing for analysis.
- **Duplication**: Removing redundant entries during data merging.
- **Granularity**: Harmonizing data from fixed stations and mobile sensors.
- **Conformity**: Standardizing formats, especially for attributes like email.

