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
| `district`            | District affect
