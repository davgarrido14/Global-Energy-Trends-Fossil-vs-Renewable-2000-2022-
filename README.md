#Global Energy Trends: Fossil vs Renewable (2000–2022)
Power BI Analysis & Data Visualization Project

This project explores how countries around the world have shifted their electricity generation from fossil fuels to renewable sources over the last two decades. Using Power BI, I built a set of visuals, DAX measures, and trend analyses to understand global patterns and highlight the progress of the energy transition.

##🎯 Objectives
Compare fossil vs renewable electricity generation globally

Analyze long‑term trends from 2000 to 2022

Use median values to represent the “typical” country and avoid distortion from outliers

Build country‑level comparisons using Top N filtering

Create a clean, interactive Power BI dashboard suitable for portfolio presentation

## Key Visuals
Global Median Trend Line (2000–2022)  
Shows how the typical country’s fossil and renewable electricity shares evolved over time.

Fossil vs Renewable (2021)  
Country‑level comparison using DAX measures.

Top 10 Countries  
Highlights the leaders in renewable or fossil electricity using Power BI’s Top N filtering.

Country Snapshot Table  
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
Fossil electricity has steadily declined since 2000.

Renewable electricity grew strongly until around 2014, then stabilized.

The global median shows that the typical country now relies less on fossil electricity than two decades ago.

Some countries (e.g., Uruguay) have extremely high renewable shares, showing rapid energy transitions.

The shift toward cleaner energy is real, but progress varies widely across regions.

## Repository Contents
dashboard.pbix — Power BI file

data/ — dataset or link to source

screenshots/ — images of the dashboard

README.md — project documentation

## How to Use
Download the .pbix file.

Open it in Power BI Desktop.

Explore the dashboard, interact with filters, and review the DAX measures.

📬 Contact
If you’d like to discuss the project or collaborate, feel free to reach out.
