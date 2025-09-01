# 🏢 Software Houses in Major Pakistani Cities — Data Analysis Report

## 📌 Overview
This repository presents a **comprehensive data-driven analysis of software houses in Pakistan**, focusing on the major urban centers: **Lahore, Karachi, Islamabad, and Gujranwala**.  

The dataset was collected using the **Instant Data Scraper Chrome extension** from **Google Maps and local business directories**, followed by **systematic data cleaning, transformation, and visualization** in Python.  
Our primary objective is to understand the **geographical distribution, digital presence, and reputation (ratings)** of software houses, while uncovering patterns that can inform **policy makers, IT professionals, and entrepreneurs**.

---

## 📊 Dataset Description
Each row in the dataset corresponds to a **single software house**. The fields are:

- **Name** → Business name as registered online.  
- **City** → One of {Lahore, Karachi, Islamabad, Gujranwala}.  
- **Address** → Physical address (if provided).  
- **Phone Number** → Contact number (where available).  
- **Website** → Official website link (if available).  
- **Rating** → Google rating (0.0–5.0) when provided.  

📂 The final dataset is stored at:  
[`data/cleaned/software_houses_cleaned.csv`](data/cleaned/software_houses_cleaned.csv)

---

## 🎯 Research Questions
This project investigates the following research questions:

1. **City Distribution** → Which city has the highest number of software houses?  
2. **Service Quality** → What is the average rating of software houses in each city?  
3. **Geographical Patterns** → Are there notable differences in the distribution of software houses between larger vs. smaller cities?  
4. **Digital Presence & Trust** → Is there a correlation between **having a website** and **receiving higher ratings**?  
5. **Data Completeness** → How does the **availability of contact details (phone, website, address)** vary across cities?  

---

## 🛠️ Tools & Technologies
- **Data Collection (Scraping):** Instant Data Scraper (Chrome Extension)  
- **Data Cleaning & Transformation:** Python (`pandas`, `numpy`)  
- **Visualization & Analysis:** `matplotlib`, `seaborn`, PowerBI  
- **Reproducibility:** Jupyter Notebook  

---

## 🔄 Data Processing & Transformations
To ensure **data quality and reliability**, we applied the following transformations:

- **Missing Values Handling**  
  - Text fields (`Name`, `WebsiteURL`, `Phone`, `Address`) → Replaced with `"Not-Available"`.  
  - Numeric fields (`Rating`, `Reviews`) → Filled with `0.0`.  

- **Deduplication**  
  - Removed duplicate records to prevent bias in city-wise analysis.  

- **Data Type Standardization**  
  - Converted `Rating` values to integers/floats where applicable.  

- **Feature Engineering**  
  - Added **binary flags** for presence of `Website` and `Phone`.  
  - Created a **completeness score** per company (0–3) based on availability of `Phone`, `Address`, `Website`.  

---

## 📈 Key Findings & Insights

### 1️⃣ City Distribution
- **Islamabad and Karachi** lead in number of software houses.  
- This highlights their role as **national IT hubs** with established ecosystems.  
- **Lahore** follows closely, while **Gujranwala** lags significantly.  

### 2️⃣ Ratings Analysis
- The **average rating** in Islamabad is slightly higher than Karachi and Lahore.  
- This suggests that competition in Islamabad may push companies to maintain a stronger reputation.  

### 3️⃣ Digital Presence
- Companies with a **website** consistently show **higher average ratings**.  
- This indicates a strong link between **professionalism**, **online visibility**, and **customer trust**.  

### 4️⃣ Data Completeness
- **Islamabad**: Most complete data (phone, address, websites available).  
- **Gujranwala**: Lowest completeness → Many companies missing websites and phone numbers.  
- This suggests a **digital maturity gap** between Tier-1 cities (Karachi, Lahore, Islamabad) and smaller urban centers.  

---

## 📊 Visualizations
The following plots (in `visuals/`) support the findings:

1. **Bar Chart:** Number of software houses per city (`city_distribution.png`).  
2. **Boxplot:** Average ratings across cities (`average_ratings.png`).  
3. **Heatmap:** Correlation between rating and website presence (`website_vs_rating.png`).  
4. **Stacked Bar Chart:** Completeness of contact info by city (`completeness_by_city.png`).  

---

## 📎 Appendix
This repository also includes:  

- **Python Notebook**: [`notebooks/01_data_cleaning_and_analysis.ipynb`](notebooks/01_data_cleaning_and_analysis.ipynb)  
- **Cleaned Dataset**: [`data/cleaned/software_houses_cleaned.csv`](data/cleaned/software_houses_cleaned.csv)  
- **Raw Dataset**: [`data/raw/software_houses_raw.csv`](data/raw/software_houses_raw.csv)  
- **Generated Visualizations**: [`visuals/`](visuals/)  

---

# 📂 Project Structure

Folders

Cleaned_SH/ → contains cleaned datasets

Combine_SH/ → contains merged/combined datasets

DATA_SH/ → contains raw/original datasets

## Files

DV_A_2.docx → report in Word format

dv-a2-f.ipynb → Jupyter Notebook with your analysis

SOFTWARE_HOUSEA_NALYSIS.pbix → Power BI dashboard

SOFTWARE_HOUSEA_NALYSIS.pdf → exported report from Power BI

## 🚀 Reproducibility Guide

### 1️⃣ Clone the Repository
### 2️⃣ Install Dependencies
pip install -r requirements.txt

### 3️⃣ Run the Jupyter Notebook
jupyter notebook notebooks/01_data_cleaning_and_analysis.ipynb

📜 License

This project is licensed under the MIT License — see LICENSE
 for details.

🙌 Acknowledgements

Google Maps & Business Directories for raw data availability.

Instant Data Scraper for assisting in semi-automated data collection.

Open-source Python community for libraries powering this research.
git clone https://github.com/kkfaraz/Software-Houses-Major-Pakistan-Cities-Data-Analysis.git
cd software-houses-pakistan
