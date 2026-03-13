# Global Energy Trends: Fossil vs Renewable (2000–2022)
### Power BI Analysis & Data Visualization Project

This project explores how countries around the world have shifted their electricity generation from fossil fuels to renewable sources over the last two decades. Using Power BI, I built a set of visuals, DAX measures, and trend analyses to understand global patterns and highlight the progress of the energy transition.

## Data Limitations - important
The dataset only provides percentage values for fossil and renewable electricity generation. Because there are no absolute figures (such as total electricity produced in GWh), it isn’t possible to calculate deeper metrics like total energy output, year‑over‑year growth in real units, or the scale of each country’s energy system. As a result, the analysis focuses on relative comparisons and trends, rather than full quantitative modeling.

## Objectives
Compare fossil vs renewable electricity generation globally

Analyze long‑term trends from 2000 to 2022

Use median values to represent the “typical” country and avoid distortion from outliers

Build country‑level comparisons using Top N filtering

Create a clean, interactive Power BI dashboard suitable for portfolio presentation

## Key Visuals
### Global Median Trend Line (2000–2022)  
Shows how the typical country’s fossil and renewable electricity shares evolved over time.

### Fossil vs Renewable (2021)  
Country‑level comparison using DAX measures.

### Top 10 Countries  
Highlights the leaders in renewable or fossil electricity using Power BI’s Top N filtering.

### Country Snapshot Table  
Displays raw values alongside calculated measures for validation.

## Core DAX Measures
Fossil 2021
DAX
Fossil_2021 =
CALCULATE(
    AVERAGE(global_renewable_and_fossil_fuel_energy_2000_2022[Electricity_from_FOSSIL_fixpercent]),
    global_renewable_and_fossil_fuel_energy_2000_2022[Yearcal] = 2021)
    
Renewable 2021
DAX
Renewable_2021 =
CALCULATE(
    AVERAGE(global_renewable_and_fossil_fuel_energy_2000_2022[Electricity_from_REN_percent]),
    global_renewable_and_fossil_fuel_energy_2000_2022[Yearcal] = 2021)
    
Global Median (Fossil)
DAX
Global_Fossil_Median =
MEDIAN(global_renewable_and_fossil_fuel_energy_2000_2022[Electricity_from_FOSSIL_fixpercent])
Global Median (Renewable)
DAX
Global_Renewable_Median =
MEDIAN(global_renewable_and_fossil_fuel_energy_2000_2022[Electricity_from_REN_percent])

## Why Use Medians?
Energy data varies massively between countries. A few extreme values (e.g., countries with nearly 100% renewables) can distort averages.
Using medians gives a fair, stable representation of the typical country and makes year‑to‑year comparisons more meaningful.

## Insights Summary
### Fossil electricity has steadily declined since 2000.

### Renewable electricity grew strongly until around 2014, then stabilized.

### The global median shows that the typical country now relies less on fossil electricity than two decades ago.

### Some countries (e.g., Uruguay) have extremely high renewable shares, showing rapid energy transitions.

### The shift toward cleaner energy is real, but progress varies widely across regions.

### Renewable energy adoption in 2021 shows a clear regional divide: North America and Europe & Central Asia lead with the highest renewable shares, while South Asia, East Asia & Pacific, and especially the Middle East & North Africa lag far behind, highlighting uneven progress in the global energy transition.

## Extra insight 2025 update

<details>
  <summary>🌋 Top 10 Fossil‑Dependent Countries (2021) — 2025 Status Overview</summary>

  
## **Top 10 Fossil‑Dependent Countries (2021) — 2025 Status Table**

| Country | Fossil % (2021) | Fossil % (2025, Official) | 2025 Trend | Notes |
|--------|------------------|----------------------------|------------|-------|
| **Comoros** | 100.00% | *Not published* | ⬇️ Decreasing | New World Bank solar projects (6.3 MWp) reducing diesel dependence. |
| **Gibraltar** | 100.00% | *Not published* | ➡️ Stable | Still relies on diesel generation; limited renewable expansion. |
| **Sint Maarten (Dutch part)** | 100.00% | *Not published* | ➡️ Stable | Electricity still mainly from diesel; renewable plans not yet large‑scale. |
| **Turkmenistan** | 99.98% | *Not published* | ➡️ Stable | Electricity remains almost entirely natural gas; no major renewable shift. |
| **Libya** | 99.97% | *Not published* | ➡️ Stable | Political instability slowed renewable development; grid still fossil‑based. |
| **Bahrain** | 99.93% | *Not published* | ⬇️ Slight decrease | Solar expansion underway; fossil still dominant but diversification started. |
| **Trinidad and Tobago** | 99.92% | *Not published* | ➡️ Stable | Electricity generation remains almost fully natural gas. |
| **Brunei Darussalam** | 99.91% | *Not published* | ➡️ Stable | Still relies on natural gas; renewable projects remain small‑scale. |
| **Kuwait** | 99.77% | *Not published* | ⬇️ Slight decrease | Solar mega‑projects (e.g., Shagaya) expanding, but fossil still primary. |
| **Saudi Arabia** | 99.76% | *Not published* | ⬇️ Noticeable decrease | Rapid solar growth under Vision 2030; several GW‑scale plants active. |

</details>

<details>
  <summary>🌱 Top 10 Renewable‑Dependent Countries (2021) — 2025 Status Overview</summary>

  
## **Top 10 Renewable‑Dependent Countries (2021) — 2025 Status Table**

| Country | Renewable % (2021) | Renewable % (2025, Official) | 2025 Trend | Notes |
|--------|----------------------|-------------------------------|------------|-------|
| **Lesotho** | 99.79% | *Not published* | ➡️ Stable | Hydropower remains dominant; no major fossil expansion reported. |
| **Costa Rica** | 99.37% | *Not published* | ➡️ Stable | Continues to generate nearly all electricity from renewables (hydro, wind, geothermal). |
| **Norway** | 99.10% | *Not published* | ➡️ Stable | Hydropower still supplies almost all electricity; renewable share remains extremely high. |
| **Central African Republic** | 96.47% | *Not published* | ➡️ Stable | Electricity system still small and hydro‑based; no major fossil growth. |
| **El Salvador** | 95.56% | *Not published* | ⬆️ Increasing | Expanding geothermal and solar capacity; renewable share expected to rise. |
| **Tajikistan** | 93.38% | *Not published* | ➡️ Stable | Hydropower continues to dominate; new dams under development. |
| **Andorra** | 93.34% | *Not published* | ➡️ Stable | Imports most electricity from renewable‑heavy neighbors; mix remains stable. |
| **Belize** | 92.86% | *Not published* | ➡️ Stable | Hydropower and biomass remain primary sources; renewable share steady. |
| **Zambia** | 92.08% | *Not published* | ➡️ Stable | Hydropower remains the backbone; drought risk is the main challenge. |
| **Angola** | 91.71% | *Not published* | ⬆️ Increasing | Large hydropower projects (e.g., Lauca) boosting renewable generation. |

</details>

## Repository Contents
Energy.pbix — Power BI file

data/ — [Kaggle](https://www.kaggle.com/datasets/nishant30488/global-renewable-and-fossil-fuel-energy?resource=download)

screenshots/ — images of the dashboard

README.md — project documentation

## How to Use
Download the .pbix file.

Open it in Power BI Desktop.

Explore the dashboard, interact with filters, and review the DAX measures.

📬 Contact
If you’d like to discuss the project or collaborate, feel free to reach out.
