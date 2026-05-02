# NYC Airbnb Market Analysis — Exploratory Data Analysis & Interactive Dashboard

A data analytics project on the New York City Airbnb market. The project covers data ingestion from multiple sources, cleaning, merging, exploratory analysis, outlier detection, and an interactive Excel dashboard for visual exploration of key market insights.

---

## Overview

The dataset covers thousands of Airbnb listings across New York City's five boroughs, sourced from DataCamp. Three separate data files, pricing, room type, and review history, are merged and cleaned into a single unified dataset, which is then analyzed and visualized both in Python and through an interactive Excel dashboard.

This is an independent project. The dataset originates from a DataCamp course, but the analysis, pipeline, and dashboard were designed and implemented independently, going beyond the scope of the guided material.

---

## Pipeline

1. Load three data sources: pricing (CSV), room type (Excel), review history (TSV)
2. Inspect and sample each dataset independently
3. Merge all three on `listing_id`
4. Parse and clean price column (remove "dollars" string, convert to numeric)
5. Standardize room type labels to lowercase
6. Parse and convert review dates to datetime format
7. Split neighborhood into district and neighborhood columns
8. Detect and flag pricing outliers using IQR method
9. Export cleaned dataset to Excel
10. Build interactive pivot-based dashboard in Excel

---

## Key Findings

- **Manhattan** dominates listings count and commands the highest average prices
- **Entire home/apt** is the most common room type across all boroughs
- **Private rooms** offer the most competitive pricing relative to location
- Outlier listings (flagged via IQR) are concentrated in Manhattan and represent luxury or event-space rentals
- Review activity peaks suggest strong seasonal demand patterns in mid-2019

---

## Deliverables

| File | Description |
|---|---|
| `NY_AirBnB_Data.ipynb` | Full analysis notebook including data loading, cleaning, EDA, outlier detection |
| `NY_AirBnb_Data.xlsx` | Three-sheet workbook: cleaned data, pivot tables, and interactive dashboard |

---

## Project Structure

```
data-analytics-nyc-airbnb/
│
├── NY_AirBnB_Data.ipynb      # Analysis notebook
├── NY_AirBnb_Data.xlsx       # Cleaned data + pivot tables + dashboard
├── requirements.txt
├── .gitignore
└── README.md
```

---

## Data Sources

The project uses three input files from the DataCamp NYC Airbnb dataset:

- `airbnb_price.csv` — listing ID, price, and full neighborhood name
- `airbnb_room_type.xlsx` — listing ID, description, and room type
- `airbnb_last_review.tsv` — listing ID, host name, and last review date

These files are not included in the repository as they originate from DataCamp. They can be accessed through the DataCamp platform.

---

## How to Run

1. Clone the repository:
```bash
git clone https://github.com/MostafaJahanian/data-analytics-nyc-airbnb.git
cd data-analytics-nyc-airbnb
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Place the three data files in the same directory as the notebook.

4. Run the notebook top to bottom.

5. The cleaned dataset will be exported as `NY_AirBnb_Data.xlsx` — open it and navigate to the **Dashboard** sheet for the interactive view.

---

## Tech Stack

`Python` `Pandas` `NumPy` `Matplotlib` `Seaborn` `Microsoft Excel`

---

## Author

**Mostafa Jahanian**
[LinkedIn](https://linkedin.com/in/mostafa-jahanian)
