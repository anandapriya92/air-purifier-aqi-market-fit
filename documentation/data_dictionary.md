# 📚 Data Dictionary

This document explains the structure, fields, and purpose of each dataset used in this project. All datasets were sourced from the **Dataful platform** as part of the Codebasics x Dataful Resume Project Challenge.

---

## 📁 1. `aqi.csv`
**Title**: Daily AQI Values for Indian Cities and Towns (2022–2025)

**Purpose**: Tracks daily air quality index and pollutant information for major cities.

| Column Name               | Description                                                        | Example                    |
|---------------------------|--------------------------------------------------------------------|----------------------------|
| `date`                   | Date of AQI measurement (format: DD-MM-YYYY)                       | 15-03-2025                 |
| `state`                  | State name where data is recorded                                  | Maharashtra                |
| `area`                   | City or locality name                                              | Mumbai                     |
| `number_of_monitoring_stations` | Count of active air monitoring stations                       | 6                          |
| `prominent_pollutants`   | Key pollutants observed (comma-separated)                          | PM2.5, PM10                |
| `aqi_value`              | Numerical AQI value (scaled index)                                 | 312                        |
| `air_quality_status`     | AQI category (e.g., Good, Poor, Very Poor, etc.)                   | Very Poor                  |
| `unit`                   | Measurement unit (index-based)                                     | Index                      |
| `note`                   | Any additional observation or info                                 | Nil                        |

---

## 📁 2. `idsp.csv`
**Title**: Disease Outbreak Surveillance Data (IDSP – 2022 to 2025)

**Purpose**: Tracks weekly disease cases and deaths reported under India’s Integrated Disease Surveillance Programme (IDSP).

| Column Name            | Description                                                         | Example        |
|------------------------|----------------------------------------------------------------------|----------------|
| `year`                | Year of outbreak                                                     | 2024           |
| `week`                | Week number (1–52)                                                   | 36             |
| `outbreak_starting_date` | Date when the disease outbreak was identified                      | 01-09-2024     |
| `reporting_date`      | Date when the report was submitted                                   | 06-09-2024     |
| `state`               | State where the disease outbreak occurred                            | Delhi          |
| `district`            | District affected                                                    | South Delhi    |
| `disease_illness_name`| Name of illness or disease                                           | Chickenpox     |
| `status`              | Report status (typically "Reported")                                 | Reported       |
| `cases`               | Number of reported cases                                             | 45             |
| `deaths`              | Number of related deaths                                             | 0              |
| `unit`                | Unit of measurement (absolute count)                                 | Number         |
| `note`                | Notes related to data collection                                     | Nil            |

---

## 📁 3. `vahan.csv`
**Title**: Monthly State-Wise Vehicle Registration by Fuel Type and Class

**Purpose**: Details the number of vehicles registered each month by fuel category, aiding in analysis of EV trends and emissions sources.

| Column Name      | Description                                                        | Example             |
|------------------|--------------------------------------------------------------------|---------------------|
| `year`           | Year of registration                                               | 2023                |
| `month`          | Month of registration                                              | 07                  |
| `state`          | State name                                                         | Tamil Nadu          |
| `rto`            | Regional Transport Office (usually "All Vahan Running Office")     | All Vahan...        |
| `vehicle_class`  | Type of vehicle registered (e.g., Car, Scooter, Bus)               | MOTOR CAR           |
| `fuel`           | Fuel type (e.g., PETROL, DIESEL, ELECTRIC, HYBRID, PURE EV)        | PURE EV             |
| `value`          | Number of registered vehicles (absolute)                           | 11234               |
| `unit`           | Measurement unit (number of vehicles)                              | Number              |
| `note`           | Miscellaneous notes                                                | Nil                 |

---

## 📁 4. `population_projection.csv`
**Title**: Projected State-Wise Population by Gender

**Purpose**: Provides monthly population forecasts per state for demand sizing and exposure estimation.

| Column Name | Description                                            | Example       |
|-------------|--------------------------------------------------------|---------------|
| `year`     | Projected year                                          | 2024          |
| `month`    | Month of projection                                     | 06            |
| `state`    | Indian state                                            | Gujarat       |
| `gender`   | Gender classification (Total, Male, Female)            | Total         |
| `value`    | Population value (in thousands)                         | 78910         |
| `unit`     | Measurement unit                                        | Thousands     |
| `note`     | Notes on projection model                               | Sample Model  |

---

## 📁 5. `meta_data.txt`
**Purpose**: Text document containing official descriptions for all fields and tables. Source: Dataful platform.

---

## 📁 6. `external_sources_notes.md`
**Purpose**: Stores web links, news clippings, competitor info, Google Trends, and research studies used to supplement secondary analysis.

---

## 📌 Note:
All datasets were used only for academic/research purposes and are publicly available. Sensitive or private data was not involved in this project.

---
