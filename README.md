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
│   │   ├── Special Admit Foundation_sample.csv
│   │   └── Census Day Enrollment(CDE) Data.md
│   │
│   ├── Notebook/
│   │   ├── Produce college headcount data (Generate Sample Numerator)
│   │   │   ├── Sample_SpecialAdmit_Headcount_by_Highschool.ipynb
│   │   │   ├── Sample_SpecialAdmit_Headcount_combined.ipynb
│   │   │   └── Sample_SpecialAdmit_Headcount_combined_Call.ipynb
│   │
│   └── Output Data/
│       ├── Special Admit Headcount_by_HighSchool.xlsx
│       ├── Special Admit Headcount_combined.xlsx
│       └── SpecialAdmit_Demos.xlsx
│
├── Notebook/
│   ├── Produce college headcount data (Generate Actual Data)
│   │   ├── RP_Make_SpecialAdmit_Demos.ipynb (denominator)
│   │   ├── RP_SpecialAdmit_Headcount_by_HighSchool.ipynb
│   │   ├── RP_SpecialAdmit_Headcount_combined.ipynb
│   │   └── RP_SpecialAdmit_Headcount_combined_Call.ipynb (numerator)
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
  - **Input:** Raw Special Admit Foundation data in CSV format.
  - **Steps:** Data cleaning, filtering, and aggregating headcount statistics.
  - **Output:** A processed dataset in Excel format, summarizing headcounts for each high school.

### RPSpecialAdmit_Headcount_combined.ipynb
- [RP_SpecialAdmit_Headcount_combined.ipynb](Notebook/RP_SpecialAdmit_Headcount_combined.ipynb)

  This script aggregates and combines headcount data from multiple sources and prepares it for further analysis and reporting.

  **Processes special admit headcount data across all high school, including:**
  - **Input:**  
    - Raw Special Admit Foundation data in CSV format  
    - Processed headcount data from [RP_SpecialAdmit_Headcount_by_HighSchool.ipynb](Notebook/RP_SpecialAdmit_Headcount_by_HighSchool.ipynb)  

  - **Steps:**  
   - Aggregation, join, and transformation  

  - **Output:**  A processed headcount dataset in Excel format, summarizing
    - Headcounts for each high school  
    - Overall headcount across all high schools 

### RP_SpecialAdmit_Headcount_combined_call.ipynb
- [RP_SpecialAdmit_Headcount_combined_Call.ipynb](Notebook/RP_SpecialAdmit_Headcount_combined_Call.ipynb)
 
  This Python script automates the execution of the other two notebooks.
  
  **=====!!! THIS IS THE ONLY PYTHON FILE YOU NEED TO RUN !!!=====**  

  It automates the data processing pipeline by executingruns both:  
  - [RP_SpecialAdmit_Headcount_combined.ipynb](Notebook/RP_SpecialAdmit_Headcount_combined.ipynb)  
  - [RP_SpecialAdmit_Headcount_by_HighSchool.ipynb](Notebook/RP_SpecialAdmit_Headcount_by_HighSchool.ipynb)  

  in sequence to automate the data processing pipeline and to ensures all data is processed in the correct order.

### CDE_Data_Processing_Script.ipynb
- [RP_Make_SpecialAdmit_Demos.ipynb](Notebook/RP_Make_SpecialAdmit_Demos.ipynb)
 
  This script processes the California Department of Education (CDE) data, filters, and reshapes it for use in the dashboard. It includes steps for filtering by reporting categories and school 
  names, as well as pivoting the data from long to wide format for easier analysis.
   
  **Processes California Department of Education (CDE) data:**
  - **Input:** Raw CDE datasets.
  - **Steps:** Filtering by reporting categories and interested high schools, cleaning school names, and reshaping the data from long to wide format.
  - **Output:** A pivoted dataset in Excel format, ready for dashboard visualization.

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
- A processed headcount dataset in Excel format, summarizing both
    - Headcounts for each high school  
    - Overall headcount across all high schools 
- A processed CDE datasets in Excel format, summarizing high school enrollment inforamtion.

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

1. Run [RP_SpecialAdmit_Headcount_combined_call.ipynb](Notebook/RP_SpecialAdmit_Headcount_combined_Call.ipynb). This will automatically execute [RP_SpecialAdmit_Headcount_combined.ipynb](Notebook/RP_SpecialAdmit_Headcount_combined.ipynb) and [RP_SpecialAdmit_Headcount_by_HighSchool.ipynb](Notebook/RP_SpecialAdmit_Headcount_by_HighSchool.ipynb) notebooks sequentially.
   
2. For the CDE data processing, run [RP_Make_SpecialAdmit_Demos.ipynb](Notebook/RP_Make_SpecialAdmit_Demos.ipynb) to filter, reshape, and clean the CDE data. This step will prepare the data for reporting.

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

4. **Run the Notebooks:**
   - Start with [RP_SpecialAdmit_Headcount_combined_call.ipynb](Notebook/RP_SpecialAdmit_Headcount_combined_Call.ipynb) and run it. This will automatically execute [RP_SpecialAdmit_Headcount_combined.ipynb](Notebook/RP_SpecialAdmit_Headcount_combined.ipynb) and [RP_SpecialAdmit_Headcount_by_HighSchool.ipynb](Notebook/RP_SpecialAdmit_Headcount_by_HighSchool.ipynb)  
 scripts in sequence.
   - Afterward, run [RP_Make_SpecialAdmit_Demos.ipynb](Notebook/RP_Make_SpecialAdmit_Demos.ipynb) to process and reshape the CDE data for visualization.


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

