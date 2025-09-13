# london-weather-analysis

# Weather Data Resampling and Visualization

This project analyzes weather data from **London (Kaggle - modified version)** using resampling techniques in Pandas.  
The assignment is divided into two main parts: preparing the dataset and answering two research questions through visualizations.

---

## Dataset
- **Source**: [Google Sheets CSV](https://docs.google.com/spreadsheets/d/e/2PACX-1vT_jChgNsQbHbg4TGepzIqk8XC9DTIKmyyxb1upo5cfZCgbfIUQc2ZC0YMzuU5uApP140Ob49KBjdqh/pub?gid=1198589591&single=true&output=csv)  
- **Features used**:
  - Precipitation  
  - Mean Temperature  
  - Min Temperature  
  - Max Temperature  
  - Snow Depth  
- **Time Range**: Data from year 2000 onwards.

---

## Part 1: Data Preparation
1. Converted the `date` column to `datetime` dtype.  
2. Set `date` as the index.  
3. Filtered data:
   - Only years ≥ 2000  
   - Only selected features listed above  
4. Imputed missing values with context-appropriate methods:
   - Forward/backward fill for continuous data  
   - Mean/median replacement where suitable  

---

## Part 2: Research Questions

### Q1: What month had the most precipitation (2000–2010)?
- **Method**:
  - Resampled precipitation to **monthly frequency** using `.sum()`.  
  - Identified the month with maximum precipitation.  
  - Added a vertical line to highlight this point.  
- **Visualization**:
  - Title: *"Precipitation for 2000-2010"*  
 <img width="1993" height="347" alt="image" src="https://github.com/user-attachments/assets/621e57e5-5903-4445-8f1f-a9572bc1367a" />
  
## Results
- **2000-10-01**: Found the month with the highest precipitation between 2000–2010.  
---

### Q2: Which year (2000–2020) had the coolest average temperature?
- **Method**:
  - Resampled mean temperature to **yearly frequency** using `.mean()`.  
  - Identified the year with the lowest average temperature.  
  - Added a vertical line to highlight this point.  
- **Visualization**:
  - Title: *"Average Temperature"*  
<img width="1998" height="347" alt="image" src="https://github.com/user-attachments/assets/f53c5aee-856c-4e04-a589-a4e4f9d35744" />
## Results
- **2010-12-31**: Identified the coolest year (lowest mean temperature) between 2000–2020.
- 
---

