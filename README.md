# Robustness-Analysis-Interactive-Dashboard

This is the Power BI dashboard I built to bring together four separate data‑robustness projects I worked on over recent months. Each project looked at how forecast‑model error changes when we introduce missing records, outliers or sensor‑noise‑style shifts in the original datasets. My main aim was to practice measuring prediction reliability rather than only building basic predictive models.
 
## Project background
 
When I first started working on these datasets I ran separate charts and small Python scripts for each case one‑by‑one. After finishing the individual analyses I realised it would be helpful to create one interactive view so someone could quickly switch between the different case studies and compare the baseline error against disturbed‑data error side‑by‑side. That is why I put together this consolidated dashboard.
 
## Included case‑study projects
 
1. Robust ML Forecasting ‑ Retail Sales Data
 ‑ Looks at how prediction RMSE shifts after adding moderate‑quantity missing‑value scenarios to retail‑sales records. The relative error increase here was small (+2.16 %).
 
2. Robust ML Forecasting ‑ Estate‑Sales Subset
 ‑ Works on a filtered subset of property‑transaction figures, testing how extreme outlier entries change model‑fit quality. Here RMSE rose substantially (+234.96 %).
 
3. Robust ML Forecasting ‑ Café Daily‑Sales Records
 ‑ Uses small‑scale daily‑revenue readings from a café‑style dataset. Because the baseline‑RMSE value was already very low (0.01), the percentage‑increase reading appears very large (+4000.00 %). Important interpretation note: At first glance this high percentage looks alarming, but it comes from a tiny starting‑error value: a small absolute jump in RMSE creates a huge‑looking relative‑rise. The forecast did not completely fail; I learned here that for robustness work we always need to examine both absolute‑RMSE numbers and percentage shifts, not percentages alone. I will keep this check in mind in my future analyses.
 
4. Robust ML Forecasting ‑ São‑Paulo Air‑Quality Sensor Series
 ‑ Works on public‑domain environmental‑monitoring timestamped data; tests effects of simulated intermittent‑reading‑loss patterns. Error rose moderately (+29.40 %).

## Dashboard features
 
‑ Project‑selector panel to switch between each of the four analyses
‑ Bar chart showing RMSE values for clean‑baseline and modified‑data test‑cases
‑ Two‑gauge view: baseline RMSE value, plus percentage‑increase in RMSE after introducing data‑quality issues
‑ Quick‑view chart showing which original source‑CSV each case‑study draws from
 
## Files inside this repository
 
‑  Robustness‑Analysis‑Dashboard.pbix  ‑ main interactive Power BI file
‑ Four project‑screenshot PNGs: one view captured for each case‑study
‑ Source‑CSV files used as underlying input‑data
‑  dashboard‑checklist.md  ‑ my personal build‑and‑export notes for reference
 
## Skills practised through this work
 
‑ Data cleaning and baseline‑performance calculation in Python
‑ Creating controlled modified‑data scenarios to test model stability
‑ Measuring RMSE before‑and‑after each disturbance test
‑ Building interactive multi‑project reports using Power BI
‑ Documenting analysis outcomes and noting points needing careful interpretation
 
## Possible next‑steps I may explore later
 
‑ Add further environmental‑ or business‑dataset robustness tests
‑ Build a simple Streamlit script to run similar disturbance‑tests interactively
‑ Develop a short research‑proposal outline built upon these initial‑experiment‑findings
 
 ##  Note:

All datasets used are publicly available open‑source data; this work is my independent‑analysis portfolio‑project and is not linked to any official organisational study.

## Project created by Shumaila ‑ November 2026
