# 📊 Analysis Plan

This document outlines how each **primary and secondary research question** was addressed using the available datasets from Dataful, along with additional research and logic. The goal is to support AirPure Innovations in identifying the **product-market fit** for launching a smart air purifier in India.

---

## ✅ Primary Analysis Plan

### 1. **Top 5 and Bottom 5 Areas with Highest Average AQI (Dec 2024 – May 2025)**
- 📂 Dataset: `aqi.csv`
- 🔍 Method:
  - Filter date range from Dec 2024 to May 2025
  - Ensure area has data for all 6 months
  - Group by `area` → calculate average AQI
  - Sort to get top 5 and bottom 5 areas
- 📈 Output: Bar chart, table

---

### 2. **Top 2 and Bottom 2 Prominent Pollutants per Southern State (2022 Onwards)**
- 📂 Dataset: `aqi.csv`
- 🔍 Method:
  - Filter `state` for southern states (KA, TN, KL, TS, AP)
  - Filter records from Jan 2022
  - Extract individual pollutants from `prominent_pollutants` field
  - Count frequency per pollutant by state
  - Rank and display top 2 and bottom 2 per state
- 📈 Output: Matrix table or pollutant heatmap

---

### 3. **Does AQI Improve on Weekends vs Weekdays in Metro Cities?**
- 📂 Dataset: `aqi.csv`
- 🔍 Method:
  - Filter for 8 metro cities
  - Convert `date` to day of week
  - Group into `Weekday` vs `Weekend`
  - Compare average AQI
- 📈 Output: Line chart, clustered bar

---

### 4. **Worst AQI Months Across Indian States**
- 📂 Dataset: `aqi.csv`
- 🔍 Method:
  - Identify top 10 states with the most unique `area` entries
  - Group by `state` and `month` to calculate average AQI
  - Highlight months with highest AQI per state
- 📈 Output: Monthly heatmap

---

### 5. **Bengaluru AQI Category Distribution (Mar–May 2025)**
- 📂 Dataset: `aqi.csv`
- 🔍 Method:
  - Filter `area = Bengaluru` and dates Mar–May 2025
  - Group by `air_quality_status`
  - Count number of days in each category
- 📈 Output: Pie chart or bar chart

---

### 6. **Top 2 Disease Illnesses per State + AQI Link**
- 📂 Datasets: `idsp.csv` + `aqi.csv`
- 🔍 Method:
  - Aggregate `idsp.csv` by `state` and `disease_illness_name` (2022–2025)
  - Join with `aqi.csv` based on `state` and `year`
  - Calculate average AQI for disease period per state
  - Rank top 2 diseases per state
- 📈 Output: Table with KPIs, bar chart

---

### 7. **EV Adoption vs AQI Comparison**
- 📂 Datasets: `vahan.csv` + `aqi.csv`
- 🔍 Method:
  - Filter for `fuel = ELECTRIC` or `PURE EV`
  - Aggregate EV count per state
  - Join with average AQI per state
  - Compare AQI of top 5 EV states vs bottom 5
- 📈 Output: Scatter plot or grouped bar

---

## ✅ Secondary Analysis Plan

### S1. **Most Affected Age Group by City**
- 🔍 Method:
  - External health studies and government reports used to infer age vulnerability
  - Age group overlays added via tooltips or assumptions
- 📁 Notes in: `external_sources_notes.md`

---

### S2. **Competitor Analysis**
- 🔍 Method:
  - Manual research of top brands (e.g., Dyson, Philips, Xiaomi)
  - Compare features: HEPA filters, PM2.5 support, VOC sensors, smart features, pricing
  - Identify gaps to guide product R&D
- 📈 Output: Feature gap matrix

---

### S3. **Population vs AQI**
- 📂 Datasets: `population_projection.csv` + `aqi.csv`
- 🔍 Method:
  - Join population and AQI per state (2024)
  - Calculate average AQI exposure per 100K people
  - Identify high-population, high-pollution areas
- 📈 Output: Bubble chart

---

### S4. **AQI Awareness in Public**
- 🔍 Method:
  - Use Google Trends to track searches like "AQI meaning", "AQI Delhi", etc.
  - Analyze search spikes during pollution emergencies
- 📁 Summary in: `external_sources_notes.md`

---

### S5. **Impactful Pollution Control Policies**
- 🔍 Method:
  - Research major policies (e.g., GRAP, BS-VI, NCAP)
  - Correlate post-policy AQI trends in regions like Delhi, Pune
  - Timeline overlay analysis
- 📈 Output: Before/after AQI comparison

---

## 🧠 Tools Used

- **Power BI** – Dashboard creation
- **Python / Excel** – Preprocessing & EDA
- **Google Trends** – For behavior/demand proxies
- **Web Research** – For secondary insights

---
# Requirements-to-Dashboard Mapping

This document maps the core expectations from the business case and evaluation criteria to the respective report pages in the Power BI dashboard for the **AirPure Innovations - Market Fit & Product Strategy** challenge.

| **Core Expectations from Business Case**                                                                                                                    | **Mapped Dashboard Page & Key Insights**                                                                                                                                                                                                                          |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Understand India’s air pollution problem**<br>– Where is it worst?<br>– What are the causes?<br>– Who is most impacted?                                | **Page 2: AQI & Health Impact**<br>🔹 Trend of AQI by state and city<br>🔹 Top polluted cities (YOY growth)<br>🔹 Impact by tier and season<br>🔹 Correlation with disease incidence (e.g. respiratory illnesses)                                                 |
| **2. Evaluate the growth and acceptance of EVs**<br>– Is EV adoption helping improve air quality?<br>– Where is the shift happening?                        | **Page 3: EV Adoption & AQI**<br>🔹 State-wise EV registrations over time<br>🔹 Comparison of AQI vs. EV density<br>🔹 Tier-wise trend analysis of adoption<br>🔹 Policy or regional drivers                                                                      |
| **3. Estimate the risk hotspots**<br>– Where is the pollution × population risk highest?<br>– What’s the demand potential?                                  | **Page 4: Risk Potential & Demand**<br>🔹 AQI × Population weighted score<br>🔹 Cities with highest health vulnerability<br>🔹 Tier-based market prioritization<br>🔹 High-risk zone map overlays                                                                 |
| **4. Define product opportunity**<br>– What type of consumers would buy air purifiers?<br>– What features do they value?<br>– What is their ability to pay? | **Page 5: Product Market Fit**<br>🔹 Willingness to pay (from external/secondary research)<br>🔹 Popular feature preference<br>🔹 Pain points from health surveys<br>🔹 Consumer segmentation by income & exposure                                                |
| **5. Deliver professional storytelling**<br>– Must be crisp, data-backed & easy to navigate<br>– Must be useful for decision-makers                         | **Page 1: Executive Overview**<br>🔹 4 summary widgets linking to all detailed pages:<br> • AQI Risk Timeline<br> • EV vs AQI Visual<br> • Population-AQI Risk Score Map<br> • Consumer Pain Points & Product Demand<br>🔹 Clean design with filter interactivity |

---


## 📦 Deliverables
- 📁 Dashboard `.pbix` file
- 📁 Slide deck `.pptx`
- 📄 Documentation folder (with markdown files)
- 🎥 (Optional) Video walkthrough for stakeholders

---

