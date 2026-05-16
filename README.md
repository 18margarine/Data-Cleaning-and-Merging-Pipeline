## **Data Cleaning & Merging Pipeline**
This is a simple project from my academic training in DataCamp.
A simple data engineering project that cleans, standardizes, and merges multiple pet-related datasets into a single unified dataset using Python and Pandas.
This project simulates a real-world ETL (Extract, Transform, Load) workflow where raw CSV files from different sources are processed into a clean and analysis-ready dataset.

### **Project Overview**
**Input Files**
| File Name |	Description |
|-----------|-------------|
| pet_activities.csv |	Daily activities of pets |
| pet_health.csv |	Vet visits and health records |
| users.csv |	Pet owner information |

**The goal of this project is to:**
- Clean inconsistent data
- Standardize column values
- Merge multiple datasets
- Produce a single comprehensive dataset for downstream analytics or application use

**The final dataset contains a unified view of:**
- Pet activities
- Health visits
- Owner information

**Features**
- Reads multiple CSV datasets using Pandas
- Cleans inconsistent activity labels
- Converts date columns into proper datetime format
- Handles missing and invalid values
- Standardizes activity names
- Adds health visit records into the same activity structure
- Merges owner information into pet records
- Exports a cleaned dataset automatically

**Technologies Used**
- Python
- Pandas
- OS module

### **Data Cleaning Performed**
**Activity Dataset**
- Converted date column to datetime format
- Replaced invalid duration values (-) with 0
- Converted duration_minutes to integer type
- Standardized activity names:
  - Play → Playing
  - Walk → Walking
  - Rest → Resting

**Health Dataset**
- Renamed visit_date to date
- Converted dates to datetime format
- Added:
  - activity_type = 'Health'
  - duration_minutes = 0

**Merging Process**
- Combined activity and health datasets using concat()
- Merged owner information using merge()
- Exported final cleaned dataset to:
  - cleaned_data/clean_data.csv
 
### **Final Output Columns**
| Column Name	| Description |
|-------------|-------------|
| pet_id	| Unique identifier for each pet |
| date	| Activity or health visit date |
| activity_type |	Pet activity type or Health |
| duration_minutes |	Activity duration in minutes |
| issue	| Health issue or vet notes |
| resolution |	Advice or treatment outcome |
| owner_id	| Pet owner identifier |
| owner_age_group |	Age group of owner |
pet_type	| Type of pet |
