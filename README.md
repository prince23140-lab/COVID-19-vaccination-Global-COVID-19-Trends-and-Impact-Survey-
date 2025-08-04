# 🦠 COVID-19 Vaccination & Mortality Analysis using Python & Power BI
👥 Student Information  

| 👤 Name        | 🆔 Student ID | 🧑‍💻 Role        |
|---------------|--------------|-----------------|
| 🧑‍🔬 Nziza Prince | 26651        | 💻 Data Analyst |

This project explores global COVID-19 case trends, death rates, and fatality ratios disaggregated by age and sex. Using real-world WHO surveillance data, we apply data cleaning, exploratory data analysis (EDA), clustering modeling, and interactive visualizations in Power BI.

---

🎯 Objective  
To analyze the COVID-19 surveillance dataset and derive insights related to:

- Global case, death, and fatality rate distributions
- Demographic disparities (age and sex)
- High-risk cluster identification using ML
- Weekly patterns and trends from 2019–2023
- Design of an interactive Power BI dashboard
- Data-driven insights to inform health strategies

---

🧰 Tools Used  

- 🐍 **Python (Jupyter Notebook)** – Data cleaning, transformation, EDA, clustering  
- 📊 **Power BI** – Data visualization, mapping, and dashboard development  
- 📁 **CSV** – Processed datasets  
- 🌐 **GitHub** – Documentation and version control  

---

📥 Dataset  
**Title:** COVID-19 Cases and Deaths (WHO COVID-19 Surveillance Data)  
**Source:** [WHO Health Inequality Repository](https://www.who.int/data/inequality-monitor/data)  
**Format:** Structured CSV  
**Period:** December 2019 – August 2023  
**Coverage:** 110 countries  
**Indicators:**  
- Cases per 100,000 people  
- Deaths per 100,000 people  
- Case fatality ratios  
- Dimensions: Age (5 groups) & Sex (Male/Female)  

---

🧼 1. Data Understanding & Preparation  

✅ Steps Taken:
- Loaded data using Pandas  
- Explored structure (hundreds of thousands of rows × 15+ columns)  
- Visualized and removed missing entries using `missingno`  
- Cleaned dates, renamed columns, and handled format inconsistencies  
- Standardized age groups & sex entries  
- Exported cleaned file as `vaccination_cleaned.csv`  

📸 Missing Data Matrix  
![Missing Data](images/missing_data_heatmap.png)

---

📊 2. Exploratory Data Analysis (EDA)

📌 Summary Statistics:
- Calculated mean, median, variance, percentiles for all indicators  
- Assessed sex and age-based patterns in case & death distribution  

📊 Key Visualizations:

**Case Distribution by Age & Sex**  
![Distribution](images/case_distribution_age_sex.png)

**Correlation Matrix of Indicators**  
![Correlation](images/correlation_heatmap.png)

**Weekly Case & Death Trends (Global)**  
![Weekly Trends](images/weekly_trends.png)

---

🧠 3. Clustering Analysis  

Used **KMeans clustering** to segment countries based on pandemic severity using:
- Case rate
- Death rate
- Case fatality ratio

✅ Steps:
- Normalized features using `StandardScaler`  
- Determined optimal clusters using **Elbow Method**  
- Applied PCA for 2D visualization  

📊 Cluster Segmentation (3 clusters)  
- Cluster 0: High-fatality countries  
- Cluster 1: Moderate impact  
- Cluster 2: Low impact  

📸 Clustering Output  
![KMeans Clustering](images/kmeans_clusters.png)

📏 Evaluation Metrics:  
- Silhouette Score: *Good separation*
- Inertia: Minimized within-cluster variance

---

🔧 4. Feature Engineering  

Created new features:
- Week number & year from date
- Region code mapping (for visuals)
- Scaled case/death rates for comparative analysis

Exported final dataset for Power BI as: `enhanced_covid_data.csv`

---

📉 5. Power BI Analysis  

🚦 Visualizations Built:
- Global Map: Deaths per 100,000
- Line Charts: Weekly case trends
- Bar Graphs: Age and sex-based distributions
- Case fatality by country & year
- Cluster comparison by indicator averages

🔍 Filters and Drill-downs:
- Year, Week, Country, Age Group, Sex
- Slicers enabled for deep exploration

📸 Power BI Dashboard  
![Dashboard Overview](images/powerbi_dashboard.png)

---

📑 6. Analytical Report  

🧾 Introduction  
This project uncovers critical patterns in global COVID-19 data to support public health responses and planning.

📍 Methodology  
- Cleaned and processed real-world WHO data  
- Performed EDA and visual diagnostics  
- Built unsupervised ML model (clustering)  
- Created an interactive dashboard using Power BI  

📊 Analysis & Results  
- Males and elderly (65+) experienced the highest mortality  
- Low-vaccinated or low-income countries show higher fatality ratios  
- Case fatality ratio varies significantly between age groups  
- Consistent peaks in early 2021 and mid-2022 globally  

🧠 Recommendations  
- Prioritize vaccination in countries with high fatality risk  
- Tailor messaging for age-specific risk management  
- Improve case and death reporting transparency in underrepresented regions

---

📂 Deliverables  

| File                          | Description                               |
|-------------------------------|-------------------------------------------|
| 📓 `Covid_19_vaccination_Capstone.ipynb` | Python code & analysis |
| 📄 `vaccination_cleaned.csv`           | Cleaned dataset              |
| 📄 `enhanced_covid_data.csv`           | Dataset with clustering features |
| 📊 `dashboard.pbix`                    | Power BI Dashboard           |
| 🖼️ `/images/`                          | Charts & dashboard screenshots |
| 📘 `README.md`                         | This documentation file      |

---

✅ Final Notes  
This project meets all academic capstone requirements:
- Real dataset from WHO  
- Data science lifecycle applied  
- ML model used  
- Interactive Power BI dashboard delivered  
- Clean documentation in GitHub

---

✨ Thank you for exploring this project!  
💡 Wishing you data-driven insights & health-conscious futures ahead.
