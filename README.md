# 🔍 Crime Rate Analysis — Los Angeles (2020–2024)

> An end-to-end exploratory data analysis of LAPD crime incidents using Python and Power BI.

---

## 📌 Project Overview

This project analyzes **57,691 crime incidents** recorded by the Los Angeles Police Department (LAPD) between **2020 and 2024**. Using Python for data processing and Power BI for visualization, the project uncovers patterns in crime types, geographic hotspots, victim demographics, weapon usage, and temporal trends.

---

## 📁 Repository Structure

```
crime-rate-analysis/
│
├── Copy_of_crime_rate_analysis.ipynb   # Main Jupyter/Colab notebook (EDA pipeline)
├── CRIME_RATE_ANALYSIS.pbix            # Power BI interactive dashboard
├── Crime_Rate_Analysis_Report.pdf      # Full project report (PDF)
├── clean_data.csv                      # Preprocessed dataset (output)
├── .gitignore                          # Git exclusion rules
└── README.md                           # This file
```

> **Note:** The raw dataset (`Crime_Data_from_2020_to_2024.csv`) is excluded via `.gitignore` due to file size. See [Data Source](#-data-source) below.

---

## 📊 Dataset

| Attribute        | Details                                      |
|------------------|----------------------------------------------|
| **Source**       | LAPD Open Data Portal                        |
| **File**         | `Crime_Data_from_2020_to_2024.csv`           |
| **Raw Records**  | 65,849                                       |
| **After Dedup**  | 57,691                                       |
| **Features**     | 28 original + 4 engineered                   |
| **Period**       | January 2020 – December 2024                 |

---

## 🛠️ Tech Stack

| Tool        | Purpose                                      |
|-------------|----------------------------------------------|
| Python 3    | Data processing and analysis                 |
| Pandas      | Data manipulation                            |
| NumPy       | Numerical operations                         |
| Matplotlib  | Static data visualization                    |
| Seaborn     | Statistical visualization                    |
| Power BI    | Interactive dashboard                        |
| Google Colab| Notebook runtime environment                 |

---

## ⚙️ How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/<your-username>/crime-rate-analysis.git
cd crime-rate-analysis
```

### 2. Install Dependencies

```bash
pip install pandas numpy matplotlib seaborn
```

### 3. Download the Dataset

Download the dataset from the LAPD Open Data Portal and place it in the project root:

```
Crime_Data_from_2020_to_2024.csv
```

> Direct link: [LAPD Crime Data on Data.gov / LA Open Data](https://data.lacity.org/Public-Safety/Crime-Data-from-2020-to-Present/2nrs-mtv8)

### 4. Run the Notebook

Open the notebook in **Google Colab** or **Jupyter**:

```bash
jupyter notebook Copy_of_crime_rate_analysis.ipynb
```

Or upload directly to [Google Colab](https://colab.research.google.com/).

### 5. View the Dashboard

Open `CRIME_RATE_ANALYSIS.pbix` in **[Power BI Desktop](https://powerbi.microsoft.com/desktop/)** (free download).

---

## 🔬 Analysis Highlights

### Data Preprocessing
- Removed 8,158 duplicate records based on `DR_NO`
- Parsed `DATE OCC` and `Date Rptd` to datetime objects
- Converted `TIME OCC` from HHMM integer to time format
- Imputed missing `Vict Age` (zero values) with median age
- Filled missing `Weapon Desc` with `"Unknown"`, missing `Vict Sex` with `"U"`

### Feature Engineering
- **Year**, **Month**, **Day** extracted from `DATE OCC`
- **Hour** extracted from `TIME OCC`

### EDA Visualizations

| Analysis | Insight |
|---|---|
| Year-wise Crime Trend | Multi-year crime volume comparison |
| Top 10 Crime Types | Theft of Identity, Vehicle Theft dominate |
| Top 10 Crime Areas | 77th Street, Southwest, Central are hotspots |
| Crimes by Hour | Peak window: 12 PM – 8 PM |
| Crimes by Day | Elevated on Fridays & Saturdays |
| Victim Age Distribution | Peak: 25–45 years |
| Victim Gender | Male victims in majority |
| Weapon Analysis | Strong-arm & Unknown most frequent |
| Premises Analysis | Street-level & residential dominate |
| Geographic Map | Scatter plot of LAT/LON coordinates |

---

## 📈 Power BI Dashboard

The `.pbix` dashboard provides:
- 📅 Year/Month/Area slicers
- 📊 Crime type and area bar charts
- 🗺️ Geographic crime map
- 👤 Victim demographic breakdowns
- 🔫 Weapon and premises analysis

---

## 📄 Report

A full formal report is available at:
```
Crime_Rate_Analysis_Report.pdf
```

---

## 🔭 Future Work

- [ ] Machine learning models for crime category prediction
- [ ] Integration with socioeconomic/census data
- [ ] Interactive Folium/Plotly geographic heatmap
- [ ] Time-series forecasting with Prophet/ARIMA
- [ ] Streamlit web app for live exploration

---

## 📜 License

This project is for educational and analytical purposes. Crime data is sourced from the LAPD Open Data Portal and is publicly available under its respective terms of use.

---

## 🙋 Author

> Developed as part of a Data Science & Analytics project.  
> Dataset: LAPD Open Data | Tools: Python · Power BI | Year: 2025

---

*If you found this project useful, give it a ⭐ on GitHub!*
