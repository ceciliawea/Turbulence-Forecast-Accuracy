# How Do Passengers Perceive Turbulence Risk Compared to Actual Forecast Accuracy?

## Aviation Meteorology & Risk Communication Project
**Author:** Cecilia S. Weaver  
**Institution:** Community College of Denver  
**Date:** April 2025 (Project Concept & Survey Phase)

---

## 📌 Project Overview
This interdisciplinary project examines the disconnect between public perception of atmospheric turbulence risk and the actual predictive accuracy of modern meteorological forecasting systems. 

While advanced tools like Doppler spectrum width analysis, Spatial Turbulence Intensity (STI), and the European Centre for Medium-Range Weather Forecasts (ECMWF) Integrated Forecasting System (IFS) have made rapid strides in resolution and precision, survey data indicates that roughly **75% of commercial airline passengers still perceive turbulence as highly dangerous or unpredictable**. 

This repository serves as a hub to bridge the gap between social science survey data and quantitative aviation weather metrics.

---

## 🛠 Future Scope & Coding Roadmap (EDR & ECMWF Validation)
The next phase of this project will transition from qualitative analysis to quantitative data science. The goal is to ingest real-world meteorological datasets and simulate how automated turbulence alerts map against historical events (such as regional mountain-wave turbulence over the Colorado Rockies).

### Planned Features:
1. **ECMWF IFS Model Ingestion:** Write Python scripts to pull and process planetary/regional wind vector and velocity fields using machine learning configurations to forecast micro-scale turbulence events (~10-30 meter grid resolution).
2. **Eddy Dissipation Rate (EDR) Validation:** Process objective aircraft-derived EDR telemetry data and compare it with traditional, subjective pilot reports (PIREPs) to calculate objective metrics of forecast success.
3. **Perception Alignment Mapping:** Code an interactive visualization tool to plot actual atmospheric instability (EDR values) alongside a synthetic passenger anxiety index to pinpoint optimal thresholds for mid-flight pilot communication.

---

## 📁 Repository Structure

```text
├── Data/
│   ├── Survey_Responses_April2025.csv       # Survey data from 106 airline travelers
│   └── GRIB_Outputs/                        # (Future) Folder for raw ECMWF IFS forecast files
├── Scripts/
│   ├── plot_survey_results.py               # Visualizes passenger risk perception charts
│   ├── edr_processor.py                     # (Future) Script to ingest and parse EDR metrics
│   └── ecmwf_ifs_downloader.py              # (Future) API client to fetch atmospheric wind shear files
├── Document/
│   └── Weaver_Turbulence_Risk_Paper.pdf     # Full research paper text
└── README.md                                # Project documentation
```

---

## 🚀 Getting Started

### Initial Requirements (Current Phase)
To run the survey data plotting scripts, install the standard data stack:
```bash
pip install pandas matplotlib seaborn
```

### Future Data Engine Requirements
To prepare for the upcoming ECMWF and weather model data processing engine, you will need to add the following geospatial and atmospheric packages:
```bash
pip install eccodes cfgrib xarray netcdf4
```

---

## 📑 Core Theoretical Framework
* **Fluid Dynamics:** Evaluation of turbulent flow regimes using the **Reynolds number ($Re$)** to express ratios of inertial to viscous forces in localized mountain lee waves.
* **Scale-Dependent Metrics:** Transitioning turbulence forecasting away from raw kilometer-scale models to modern finer-scale mapping techniques using Doppler spectrum widths to track rapid velocity fluctuations in real time.

---

## 📚 References & Literature Baseline
* **ECMWF IFS & Case Studies:** Gisinger et al. (2024). *Severe convectively induced turbulence hitting a passenger aircraft and its forecast by the ECMWF IFS model.*
* **EDR & Aircraft Detection:** Sharman, R., Lane, T. (2016). *Aviation turbulence: Processes, detection, prediction.*
* **Radar & Spatial Intensity:** Duncan, J. et al. (2019). *Airborne radar Doppler spectrum width as a scale-dependent turbulence metric.*
