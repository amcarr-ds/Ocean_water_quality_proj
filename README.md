# 506-OceanWater-Team1
Forecasting Ocean Quality within the San Diego Coastal Region

This project is for USD’s ADS-506 Applied Time Series Analysis Course in Fall 2022

-- Project Status: [Complete]

## Installation
First clone the repo onto your device, then load into R studio. The data is stored in the "data/Ocean Water" subfolder while the code (.rmd file) is in the "markdown" subfolder.

### Project Introduction/Objective
The main purpose of this project is to develop time series models to forecast various parameters for ocean water quality. This is to allow businesses and communities to know if additional measures to keep the water clean need to be taken or if there is  a health risk to being in the water at certain times (i.e. regular spikes in entero type microbes that could cause a health crisis). 

### Partners and Contributors:
* Aaron Carr, Brianne Bell, Connie Chow
* Data sourced from:
  * Water Quality - Ocean Monitoring Program - City of San Diego Open Data Portal

### Methods Used:
* Exploratory Data Analysis (EDA) and Preprocessing
  * Time series plots
  * Autocorrelation and plots
  * tsibble
  * timetk for ts tibble
  * aggregation
  * dcast
  * mutate
* Modeling
  * Hunt-Winter's
  * ARIMA
   * ARIMA with Predictors
  * Time Series Linear Regression
* Evaluation Metric(s)
  * RMSE
  * MAPE
  * MAE

### Technologies
R Markdown in R Studio

## Project Description
The dataset was obtained through San Diego, California's (USA) open source data. The data is from 1990-2021 with the measured parameters occupying the same column (Parameters) but they included various chemical, optical, and biological measures for two general locations of sample stations in the Pacific Ocean off the coast of San Diego. Overall there are 1.2 million entries but when the data is reorganized so that each parameter is in its own column and measurements are averaged for each day or week, there are far fewer entries.

| feature name | dictionary | further notes, if any |
--- | --- | --- |
| sample | unique sample ID  |
| station | unique location ID of the sample | 
| depth_m | depth, in meters, sample was taken | 
| time | time that the sample was taken |
| project | outfall region where sample was collected | PLOO (Point Loma Ocean Outfall) or SBOO (South Bay Ocean Outfall) |
| parameter | factor being recorded | fluoremetry, DENSITY, DO, ENTERO, FECAL, OG, PH, SALINITY, SUSO, TEMP, TOTAL |
| qualifier | symbols if the value needed clarification | <, >, e, LA, ND, NS | 
| value | actual value of measurement | 
| units | units for each factor | %, C, CFU/100mL, mg/L, pH, ppt, sigma-t, ug/L | 
 
Rearranging the data to a more model friendly format, especially when taking into accound the unevenly spaced samples for each parameter, was a lot more difficult and time consuming than we anticipated it would be. 

## License
The data was open-source data

## Acknowledgements
Thanks to Professor Rick Sanchez, MSc. for the support and feedback throughout the project
