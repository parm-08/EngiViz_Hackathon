# 🌦️ Kolkata Weather Dashboard

**Signals hidden in the record.** An interactive Streamlit dashboard that digs into a 5-year daily weather record for Kolkata to answer three specific questions: is the monsoon arriving earlier, do humid days predict cold snaps, and are winters warming?


---

## ✨ Features

- **Three data-driven chapters**, each built around one question:
  - 🌧️ **Monsoon Timing** — is onset shifting earlier or later, year over year?
  - ❄️ **Humidity & Cold Snaps** — do humid, rainy days predict sharp temperature dips?
  - 🌡️ **Winter Warming** — are average winter minimum temperatures trending up?
- **Live filter bar** — a year-range slider, season focus, and adjustable cold-snap window that recompute every KPI, chart, and the closing summary in real time.
- **Four headline KPIs** — monsoon onset shift, total onset shift, winter warming trend, and a humidity–cold-dip correlation, all derived directly from the data.
- **Interactive Plotly charts** — trend lines, bar charts, scatter plots, box plots, and a data table, each with custom hover tooltips, unified hover on trend charts, and cross-hair spike lines.
- **Polished dark UI** — a glassmorphic, gradient-based design with hover animations on every card, KPI, and section heading.
- **Honest about its limits** — the dashboard flags upfront that ~5 years of data means these are early signals, not confirmed long-term climate trends, and documents the precipitation-hours humidity proxy it uses.

## DEPLOYED LINK 
https://engivizhackathon.streamlit.app/

## SCREENSHOTS 
<img width="947" height="718" alt="Screenshot 2026-09-14 122236" src="https://github.com/user-attachments/assets/680adbd9-114f-4e08-aa72-1d7954e0262f" />
<img width="933" height="593" alt="Screenshot 2026-09-14 122309" src="https://github.com/user-attachments/assets/cc99421d-09ce-408e-9ea2-ebc5d073151d" />
<img width="917" height="661" alt="Screenshot 2026-09-14 122318" src="https://github.com/user-attachments/assets/717eed18-2b3e-4799-9adb-8556d055b697" />

## SCREEN RECORDING


https://github.com/user-attachments/assets/16d030cd-bba9-4548-bdf0-377f0c880a98



## 🧠 How the analysis works

| Question | Method |
|---|---|
| Monsoon onset | First day after April 1 where 3-day rolling rainfall ≥ 20mm; trend fit with a linear regression across years |
| Humidity vs. cold dips | "Dip" = how far a day's min. temperature falls below its 15-day centered rolling average; correlated against precipitation hours (used as a documented proxy for humidity, since the dataset has no humidity column) |
| Winter warming | Winters are grouped as Dec (of the prior year) + Jan + Feb; only winters with ≥ 80 days of data are included; trend fit with a linear regression across winter-years |

The first year in the dataset is excluded from monsoon-onset calculations since it's a partial year (record starts mid-year), which would otherwise bias the result.

## 🚀 Getting Started

### Prerequisites

- Python 3.9+
- A CSV file named `kolkata_weather.csv` in the project root (or update the path in `load_data()`), with at least these columns:

  ```
  time, temperature_2m_max, temperature_2m_mean, temperature_2m_min,
  rain_sum, precipitation_sum, precipitation_hours,
  sunshine_duration, wind_gusts_10m_max (or wind_speed_10m_max)
  ```

  This dashboard was built against daily data pulled from the [Open-Meteo Historical Weather API](https://open-meteo.com/), but any source with matching column names will work.

### Installation

```bash
git clone https://github.com/<your-username>/kolkata-weather-dashboard.git
cd kolkata-weather-dashboard
pip install -r requirements.txt
```

### Run it

```bash
streamlit run app.py
```

The app opens at `http://localhost:8501`.

## 📦 requirements.txt

```
streamlit
pandas
numpy
plotly
```

## 🗂️ Project Structure

```
.
├── app.py                 # Main Streamlit dashboard
├── kolkata_weather.csv    # Daily weather data (not included — bring your own)
├── requirements.txt
└── README.md
```

## 🎛️ Using the Dashboard

- Drag the **year range** slider to zoom the whole dashboard into a specific window — every KPI, chart, and the closing summary update instantly.
- Use **season focus** and **cold-snap window** to adjust how many extreme days show up in Chapter 2.
- Hover any chart for exact values and dates; hover any card for a subtle lift-and-glow interaction.

## ⚠️ Data Limitations

- The record spans roughly 5 years — long enough to spot patterns, not long enough to confirm climate trends. Treat the trend numbers as early signals.
- There's no humidity column in the source data, so Chapter 2 uses precipitation hours as a proxy, since humidity in Kolkata tracks closely with rainfall.

## 🛠️ Built With

- [Streamlit](https://streamlit.io/) — app framework
- [Plotly](https://plotly.com/python/) — interactive charts
- [Pandas](https://pandas.pydata.org/) / [NumPy](https://numpy.org/) — data wrangling and trend fitting

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

## 🙌 Acknowledgements

Weather data sourced from [Open-Meteo](https://open-meteo.com/), a free historical weather API.
