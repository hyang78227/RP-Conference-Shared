# Special Admit Dashboard Project

## Overview
This project contains multiple Python scripts for processing and analyzing student enrollment data related to special admit programs. The scripts are designed to clean, transform, and merge data from various sources to facilitate reporting and visualization in a dashboard.

## Table of Contents
- [Overview](#overview)
- [File Descriptions](#file-descriptions)
  - [RP_SpecialAdmit_Headcount_by_HighSchool.ipynb](Notebook/RP_SpecialAdmit_Headcount_by_HighSchool.ipynb)
  - [RP_SpecialAdmit_Headcount_combined.ipynb](Notebook/RP_SpecialAdmit_Headcount_combined.ipynb)
  - [RP_SpecialAdmit_Headcount_combined_call.ipynb](Notebook/RP_SpecialAdmit_Headcount_combined_Call.ipynb)
  - [RP_Make_SpecialAdmit_Demos.ipynb](Notebook/RP_Make_SpecialAdmit_Demos.ipynb)
- [Data Flow](#data-flow)
- [Raw Data](#raw-data)
- [Processing](#processing)
- [Output](#output)
- [Installation](#installation)
- [Usage](#usage)
- [Requirements](requirements.txt)
- [License](LICENSE)

## Folder Structure

```plaintext
RP-Conference-Share/
│
├── Example/
│   ├── Input Data/
│   │   └── Special Admit Foundation_sample.csv
│   │
│   ├── Notebook/
│   │   ├── Sample_SpecialAdmit_Headcount_by_Highschool.ipynb
│   │   ├── Sample_SpecialAdmit_Headcount_combined.ipynb
│   │   └── Sample_SpecialAdmit_Headcount_combined_Call.ipynb
│   │
│   └── Output Data/
│       ├── Special Admit Heaadcount_by_HighSchool.xlsx
│       └── Special Admit Heaadcount_combined.xlsx
│
├── Notebook/
│   ├── RP_Make_SpecialAdmit_Demos.ipynb
│   ├── RP_SpecialAdmit_Headcount_by_HighSchool.ipynb
│   ├── RP_SpecialAdmit_Headcount_combined.ipynb
│   └── RP_SpecialAdmit_Headcount_combined_Call.ipynb
│
├── .gitignore
├── Code Of Conduct.md
├── Contributing.md
├── LICENSE
├── README.md
└── requirements.txt
```
## File Descriptions

### RP_SpecialAdmit_Headcount_by_HighSchool.ipynb
- [RP_SpecialAdmit_Headcount_by_HighSchool.ipynb](Notebook/RP_SpecialAdmit_Headcount_by_HighSchool.ipynb)
 
This notebook processes data related to special admit headcounts by high school. It includes data cleaning, filtering, and generating headcount statistics for each high school.  
**Processes special admit headcount data by high school, including:**
- **Input:** Raw enrollment data by high school.
- **Steps:** Data cleaning, filtering, and generating headcount statistics.
- **Output:** A cleaned dataset summarizing headcounts for each high school.

### RPSpecialAdmit_Headcount_combined.ipynb
- [RP_SpecialAdmit_Headcount_combined.ipynb](Notebook/RP_SpecialAdmit_Headcount_combined.ipynb)
  
This script aggregates and combines headcount data from multiple sources and prepares it for further analysis and reporting.  
**Aggregates and combines headcount data from multiple sources to:**
- **Input:** Processed datasets from the high school-level analysis.
- **Steps:** Merging, aggregation, and transformation.
- **Output:** A consolidated dataset ready for reporting.

### RP_SpecialAdmit_Headcount_combined_call.ipynb
- [RP_SpecialAdmit_Headcount_combined_Call.ipynb](Notebook/RP_SpecialAdmit_Headcount_combined_Call.ipynb)
 
This Python script automates the execution of the other two notebooks. It runs both the RP_SpecialAdmit_Headcount_by_HighSchool.ipynb and RPSpecialAdmit_Headcount_combined.ipynb scripts in sequence to automate the data processing pipeline.  
**Automates the data processing pipeline by:**
- Executing RP_SpecialAdmit_Headcount_by_HighSchool.ipynb and RPSpecialAdmit_Headcount_combined.ipynb sequentially.
- Ensures all data is processed in the correct order.

### CDE_Data_Processing_Script.ipynb
- [RP_Make_SpecialAdmit_Demos.ipynb](Notebook/RP_Make_SpecialAdmit_Demos.ipynb)
 
This script processes the California Department of Education (CDE) data, filters, and reshapes it for use in the dashboard. It includes steps for filtering by reporting categories and school names, as well as pivoting the data from long to wide format for easier analysis.  
**Processes California Department of Education (CDE) data:**
- **Input:** Raw CDE datasets.
- **Steps:** Filtering by reporting categories, cleaning school names, and reshaping the data from long to wide format.
- **Output:** A pivoted dataset ready for dashboard visualization.

## Data Flow

### Raw Data
Input data is sourced from multiple files, including:
- High school enrollment data (special admit programs and associated headcounts).
- California Department of Education (CDE) data for educational reporting and student demographics.

### Processing
The data is processed through the following steps:
1. **Data Cleaning:** The data is cleaned to handle missing values, remove outliers, and ensure consistency across datasets.
2. **Filtering:** Data is filtered based on relevant categories such as academic year, school names, and program types.
3. **Reshaping:** Data is reshaped (pivoted from long to wide format) for easier analysis and reporting.
4. **Aggregation:** Aggregated datasets are created by combining headcount data, ethnicities, and academic year data.

### Output
The consolidated and processed datasets are exported as Excel files, which are used for the dashboard's reporting and visualization.

## Installation
To set up this project on your local machine, follow the steps below:

1. Clone the repository to your local machine:
    ```bash
    git clone <repository-url>
    ```

2. Navigate to the project directory:
    ```bash
    cd <project-directory>
    ```

3. Install the required Python packages:
    ```bash
    pip install -r requirements.txt
    ```

## Usage
To run the notebooks and execute the data processing steps:

1. Run the RP_SpecialAdmit_Headcount_combined_call.ipynb script. This will automatically execute both the RP_SpecialAdmit_Headcount_by_HighSchool.ipynb and RPSpecialAdmit_Headcount_combined.ipynb notebooks sequentially.
   
2. For the CDE data processing, run the CDE_Data_Processing_Script.ipynb to filter, reshape, and clean the CDE data. This step will prepare the data for reporting.

### How to Run Jupyter Notebooks
1. **Install Jupyter:** If you don't have Jupyter installed, you can install it using pip:
    ```bash
    pip install jupyter
    ```

2. **Start Jupyter:** Once Jupyter is installed, start it by running:
    ```bash
    jupyter notebook
    ```
    This will open a web interface in your default browser.

3. **Navigate to the Project Folder:** In the web interface, navigate to the folder where the project is located. You should see all the notebooks listed.

4. **Run the Notebooks:** Start with RP_SpecialAdmit_Headcount_combined_call.ipynb and run it. This will automatically execute the RP_SpecialAdmit_Headcount_by_HighSchool.ipynb and RPSpecialAdmit_Headcount_combined.ipynb scripts in sequence. Afterward, run the CDE_Data_Processing_Script.ipynb to process and reshape the CDE data for visualization.


## License
This project is licensed under the MIT License. See the  [License](LICENSE)vfor more details.


## Requirements
This project requires the following Python libraries:
- pandas
- openpyxl
- nbformat
- nbconvert
- os
- matplotlib (if you plan on visualizing the data)

All dependencies are listed in the requirements.txt file. You can install them by running:
```bash
pip install -r requirements.txt

