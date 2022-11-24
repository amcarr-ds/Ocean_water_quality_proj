# 506-OceanWater-Team1
Working Title: Forecasting the Ocean Quality by San Diego
This project is for USD’s ADS-506 Applied Time Series Analysis Course in Fall 2022

-- Project Status: [Active]

## Installation
You should add an instruction how this project to be used, installed, run, edited in others’ machine.
First clone the repo onto your device
> git init
>
> git clone

### Project Introduction/Objective
The main purpose of this project is ________. Describe the goals of the project and potential impacts. Mention the needs/applications of your project clearly. Limit to one/two short paragraph(s). 

### Partners and Contributors:
* Aaron Carr, Brianne Bell, Connie Chow
* Data sourced from:
  * Water Quality - Ocean Monitoring Program - City of San Diego Open Data Portal

### Methods Used:
* Exploratory Data Analysis (EDA) and Preprocessing
  * Time series plots
  * Autocorrelation and plots
  * tsibble
  * aggregation
  * dcast
  * mutate
* Modeling
  * Hunt-Winter's
* Evaluation Metric(s)
  * RMSE
  * MAPE

### Technologies
R Markdown in R Studio

## Project Description
The dataset was obtained through San Diego, California's (USA) open source data. The data is from 1990-2021 with the measured parameters occupying the same column (Parameters) but they included various chemical, optical, and biological measures for two general locations of sample stations in the Pacific Ocean off the coast of San Diego. Overall there are 1.2 million entries but when the data is reorganized so that each parameter is in its own column and measurements are averaged for each day or week, there are far fewer entries.
The data dictionary is as follows:
* sample
 * unique sample ID
* station
 * unique location ID of the sample
* depth_m
 * depth, in meters, sample was taken
* time
 * time that the sample was taken
* project
 * outfall region where sample was collected (general umbrella location for sample stations that fall under these)
 * PLOO (Point Loma Ocean Outfall)
 * SBOO (South Bay Ocean Outfall)
* parameter
 * factor being recorded
 * fluoremetry, DENSITY, DO, ENTERO, FECAL, OG, PH, SALINITY, SUSO, TEMP, TOTAL
* qualifier
 * symbols if the value needed clarification
 * <, >, e, LA, ND, NS
* value
 * actual value of measurement
* units
 * units for each factor
 * %, C, CFU/100mL, mg/L, pH, ppt, sigma-t, ug/L
 
Rearranging the data to a more model friendly format, especially when taking into accound the unevenly spaced samples for each parameter, was a lot more difficult and time consuming than we anticipated it would be. 

## License
The data was open-source data

## Acknowledgements
Thanks to Professor Rick Sanchez, MSc. for the support and feedback throughout the project
