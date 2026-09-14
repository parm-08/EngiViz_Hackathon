# 🌦️ Kolkata: When Heat Meets Water

> **Signals hidden in the record.**

An interactive **Streamlit weather analytics dashboard** that explores a 5-year daily weather record for Kolkata (2021–2025), revealing how **temperature, rainfall, sunshine, wind, and seasonal patterns** shape the city's weather rhythm.

The dashboard turns raw weather data into a visual story — from scorching summer heat to the monsoon's arrival and the transition from heat-dominated to rain-dominated conditions.

---

## 🚀 Live Demo

👉 **[View the Live Dashboard](https://engivizhackathon.streamlit.app/)**

---

## 📌 Project Overview

Kolkata's weather follows a strong seasonal rhythm.

This dashboard explores that rhythm through interactive visualizations and data-driven questions such as:

- 🌧️ **Is the monsoon arriving earlier over the years?**
- 🌡️ **Are Kolkata's winters getting warmer?**
- 💧 **How does rainfall and precipitation relate to temperature changes?**
- ☀️ **When does Kolkata receive the most sunshine?**
- 🌦️ **How does the city transition from extreme heat to the monsoon?**

Rather than presenting charts independently, the dashboard is designed as a **data story**, guiding the viewer from summer heat → monsoon transition → yearly patterns → research questions.

---

# ✨ Key Features

### 📊 Interactive Weather Dashboard

- Interactive year and season filters
- Dynamic KPIs and visualizations
- Plotly-based interactive charts
- Hover tooltips with detailed values
- Responsive dark-themed interface
- Story-driven dashboard structure

### 🌡️ Four Headline Weather Indicators

The dashboard highlights four major weather extremes:

- **Hottest Day**
- **Heaviest Rainfall**
- **Maximum Sunshine**
- **Strongest Wind Gust**

These provide a quick snapshot of the most extreme conditions found in the dataset.

### 📈 Temperature Analysis

Explore:

- Daily maximum temperature
- Daily average temperature
- Daily minimum temperature
- Seasonal temperature patterns
- Year-to-year temperature variation

### 🌧️ Rainfall & Monsoon Analysis

The dashboard examines:

- Daily rainfall
- Extreme rainfall events
- Seasonal rainfall contribution
- Monsoon rainfall dominance
- Monsoon onset timing
- Rainfall trends across years

### ☀️ Sunshine Analysis

Visualize:

- Average daily sunshine duration
- Monthly sunshine patterns
- Changes in sunshine during the monsoon
- The relationship between sunshine and seasonal weather

### 📅 Seasonal Transition

One of the central stories of the dashboard is the transition between:

**Summer Heat → Monsoon → Rainfall Peak → Reduced Sunshine**

The dashboard compares April and August to show how dramatically Kolkata's weather changes within a few months.

### 🔬 Research Deep-Dive

The dashboard investigates key research questions using statistical trends, including:

- **Monsoon onset timing**
- **Winter minimum temperature trends**

Trend lines are fitted across yearly observations to identify potential changes in the weather pattern.

---

# 📖 Dashboard Story

The dashboard is organized into four chapters.

## Chapter 1 — The Heat

### Kolkata's Heat Has a Seasonal Rhythm

Daily maximum, average, and minimum temperatures reveal Kolkata's repeating annual temperature cycle.

This section identifies:

- Hottest recorded day
- Daily temperature variation
- Extreme heat periods
- Temperature behavior across years

---

## Chapter 2 — The Turning Point

### April vs August: Two Different Faces of Kolkata

Within just a few months, Kolkata transitions from a heat-dominated environment to a rain-dominated monsoon season.

The dashboard compares:

### April — Heat Peak

- High average maximum temperature
- Lower rainfall
- Longer sunshine duration

### August — Rainfall Peak

- Lower average maximum temperature
- Extremely high rainfall
- Reduced sunshine duration

This creates the central story of the dashboard:

> **Heat gives way to water.**

---

## Chapter 3 — The Monsoon

### Rainfall, Sunshine & the Year-on-Year Picture

This section explores:

- Seasonal contribution to total rainfall
- Monthly sunshine duration
- Year-by-year temperature variation
- Year-by-year rainfall variation

The analysis shows that the **monsoon contributes the majority of Kolkata's recorded rainfall** during the study period.

---

## Chapter 4 — Research Deep-Dive

### Answering the Key Research Questions

The dashboard uses statistical analysis to investigate longer-term patterns within the available dataset.

#### Q1 — Is the Monsoon Arriving Earlier?

Monsoon onset is defined as the first date after April 1 where **3-day rolling rainfall reaches at least 20 mm**.

A linear trend is then fitted across yearly onset dates.

The dashboard indicates an **earlier-onset signal**, but this should be interpreted cautiously because the dataset covers only a limited number of years.

#### Q2 — Are Kolkata's Winters Getting Warmer?

Winter is defined using:

- December
- January
- February

The analysis calculates the average winter minimum temperature for each year and fits a linear trend.

The result suggests a **warming signal in winter minimum temperatures**, although the short time span means this should not be interpreted as definitive evidence of long-term climate change.

---

# 🧠 How the Analysis Works

| Research Question | Method |
|---|---|
| **Monsoon onset** | First date after April 1 where 3-day rolling rainfall reaches ≥ 20 mm |
| **Monsoon trend** | Linear regression across yearly monsoon-onset dates |
| **Winter warming** | Average minimum temperature during Dec–Feb |
| **Winter trend** | Linear regression across yearly winter minimum temperatures |
| **Seasonal rainfall** | Total rainfall grouped by season |
| **Sunshine analysis** | Average daily sunshine duration grouped by month |
| **Extreme weather** | Maximum/minimum values calculated from daily observations |

The first incomplete year is excluded from monsoon-onset calculations where necessary to avoid bias caused by partial-year data.

---

# 📊 Key Findings

Some of the major observations highlighted by the dashboard include:

- 🌡️ Kolkata experiences a strong recurring annual temperature cycle.
- 🔥 Summer contains the most extreme heat conditions.
- 🌧️ The monsoon dominates Kolkata's annual rainfall.
- ☀️ Sunshine duration changes substantially throughout the year.
- 🌦️ April and August represent dramatically different weather regimes.
- 📉 The calculated monsoon-onset trend suggests an earlier onset over the recorded years.
- 🌡️ Winter minimum temperatures show a positive trend in the available data.

> ⚠️ These findings represent patterns within the available dataset and should not be treated as definitive long-term climate conclusions.

---

# 📁 Dataset

The dashboard uses the following Kolkata weather dataset:

**Kolkata Climate and Weather 2021–2025 — Daily Data**

👉 [View Dataset on Kaggle](https://www.kaggle.com/datasets/sumanbera19/kolkata-climate-and-weather-20212025-daily-data)

The dataset contains daily weather observations including variables such as:

- Temperature
- Maximum temperature
- Minimum temperature
- Rainfall
- Precipitation
- Precipitation hours
- Sunshine duration
- Wind speed / wind gusts

---

# 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| 🐍 **Python** | Data analysis and application logic |
| 🎈 **Streamlit** | Interactive dashboard |
| 🐼 **Pandas** | Data manipulation and analysis |
| 🔢 **NumPy** | Numerical operations |
| 📊 **Plotly** | Interactive visualizations |
| 📈 **Linear Regression** | Trend analysis |
| 📄 **CSV** | Weather dataset |

---

# 🗂️ Project Structure

```text
Kolkata-Weather-Dashboard/
│
├── app.py
│
├── kolkata_weather.csv
│
├── requirements.txt
│
├── README.md
│
└── LICENSE
