# TD4 — Time series: collection, cleaning, smoothing, and honest projection

Real hourly atmospheric CO2 (ppm) for Le Mans (48.0061, 0.1996), pulled from
[Open-Meteo's Air Quality API](https://open-meteo.com/en/docs/air-quality-api)
(CAMS reanalysis + forecast model, keyless), aggregated to daily means.

- `scripts/fetch_series.py` — fetches the last 90 days of hourly CO2 and writes `data/series.csv`
  (one row per day, with the number of real hourly readings behind each daily mean).
