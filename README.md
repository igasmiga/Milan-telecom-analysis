# 📊 Milan Telecommunications Data Analysis
### Spatiotemporal patterns, Clustering, and Anomaly Detection
## 📌 Project Overview
This project provides a comprehensive analysis of telecommunications data from the city of Milan (November 2013). By analyzing mobile internet usage patterns across 10,000 grid squares, we identify functional city zones and detect unusual network behavior.

## 🛠️ Tech Stack & Libraries
* **Language:** Python 3.12.7
* **Data Processing:** `Pandas`, `NumPy`, `glob` (standard library)
* **Visualization:** `Matplotlib`, `Seaborn`
* **Machine Learning:** `Scikit-learn` (StandardScaler, K-Means)
* **Data Format:** `json` (for GeoJSON grid handling)
## 📊 Data Acquisition

The dataset used in this project is part of the **Telecom Italia Big Data Challenge**. To run the analysis, you need to obtain the following files:

### 1. Telecommunications Data (Activity Logs)
The core dataset contains mobile phone activity (SMS, Calls, Internet) for the city of Milan.
* **Source:** [Harvard Dataverse - Open Population Repository](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/EGZDWV) or the official **Nature Scientific Data** portal.
* **Required Files:** All `.txt` files covering November 2013 (e.g., `sms-call-internet-mi-2013-11-01.txt` through `2013-11-30.txt`).
* **Placement:** Download and extract these files into the `Data/` folder in the project root.

### 2. Grid Geometry (GeoJSON)
To visualize the 10,000 squares on a map (Task V), the grid geometry file is required.
* **Source:** Included in the same dataset link above or via the [Milan Grid GeoJSON](https://github.com/marcodena/mi-phone-data/blob/master/data/milano-grid.geojson) repository.
* **Required File:** `milano-grid.geojson`.
* **Placement:** Place this file in the root directory or the `Data/` folder (ensure the path in `main.ipynb` matches).

### 3. About the Data
The dataset is provided in a tab-separated format with the following structure:
`SquareID | TimeInterval | CountryCode | SMS-in | SMS-out | Call-in | Call-out | Internet`
*Note: This project specifically handles the field alignment issue where "Country Code" and "Internet" activity may be shifted in certain source versions.*


## ⚙️ How to Run
Follow these steps to replicate the analysis on your local machine:
### 1. Prerequisites
Ensure you have **Python 3.12** installed. You will also need the following external libraries:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
