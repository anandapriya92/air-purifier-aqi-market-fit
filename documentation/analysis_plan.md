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


---

### 🔵 **Page 1: National AQI Summary & Hotspot KPIs**
> **Theme:** High-level KPIs and national risk snapshot

**Includes:**
- Most polluted city (last 6 months)
- City with most severe days
- Highest AQI spike
- National average AQI
- MoM% changes for all above

📍 *No business question mapped, but this is foundational context for every other page.*

---

### 🟠 **Page 2: Severity Mapping (City/Time-Based)**
> **Theme:** Identifying severe regions and temporal pollution patterns

**Mapped Questions:**
- Primary Q1: Top 5 / Bottom 5 AQI cities (Dec 2024 – May 2025)
- Primary Q3: AQI on weekdays vs weekends – metro cities
- Primary Q4: Worst AQI months across states
- Primary Q5: AQI category days – e.g., Bengaluru

**Visuals:** Column charts, matrix tables, line charts with tooltips

---

### 🟢 **Page 3: Health Impact & Disease Mapping**
> **Theme:** Health outcomes linked with poor air quality

**Mapped Questions:**
- Primary Q6: Top 2 diseases per state with AQI
- Secondary Q1: Most affected age groups by city

**Containers & Add-ons:**
- Disease matrix + AQI average
- Stacked column (age group)
- Health burden index map
- Pediatric asthma vs AQI trend

🧠 *Focus: Support R&D with medical relevance and regional differences.*

---

### 🔵 **Page 4: Demand Triggers & Market Behavior**
> **Theme:** Understanding consumer behavior, EV patterns, and awareness

**Mapped Questions:**
- Primary Q7: EV adoption vs AQI
- Secondary Q3: Population vs AQI
- Secondary Q4: AQI awareness + health understanding

**Visuals:**
- Correlation charts
- Pie/column for awareness distribution
- KPI: Search spike behavior during AQI events

---

### 🔴 **Page 5: Product Strategy & Market Fit**
> **Theme:** Turning insights into product + market prioritization

**Mapped Questions:**
- Primary Q2: Top/Bottom pollutants in South India
- Secondary Q2: Competitor benchmarking
- Secondary Q5: Govt policies & pollution reduction

**Deliverables:**
- City Risk Score matrix
- Competitor Feature Gap Table
- Suggested product features (PM2.5 sensor, smart sync, etc.)
- Policy impact vs AQI trend

---

✅ This report structure ensures every question is visually backed by actionable insights and targeted toward AirPure’s product, strategy, and R&D direction.


## 📦 Deliverables
- 📁 Dashboard `.pbix` file
- 📁 Slide deck `.pptx`
- 📄 Documentation folder (with markdown files)
- 🎥 (Optional) Video walkthrough for stakeholders

---

