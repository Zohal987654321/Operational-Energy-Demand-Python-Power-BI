# Operational-Energy-Demand-Python-Power-BI
Operational energy demand analysis
Australian Energy Demand Insights Report
Analysis Period: 10th February 2025 – 11th April 2025

1. Data Source & Methodology
Data Source:
The data was sourced from the Australian Energy Market Operator (AEMO) and consists of half-hourly operational demand readings across five Australian regions. The region identifier NSW1 includes both New South Wales and the Australian Capital Territory (ACT).
Data Preparation Workflow:

Download & Extraction:
Data was obtained as multiple .zip files from the AEMO website and consolidated into a single folder on the local machine.
ETL in Python (Jupyter Notebook via Anaconda):
All .csv files were programmatically extracted and concatenated using Python.
Column names were cleaned, and data types were validated and corrected.
The DateTime field was split into separate Date and Time columns for flexibility in time-series analysis.
Negative energy demand values were omitted due to their lack of logical validity; further investigation with a domain expert is recommended to assess their cause and relevance.
A 30-day forecast was generated using the ARIMA method in Python, enabling future comparison with actual demand data.
Population Data:
Population estimates as of March 2024 were obtained from the Australian Bureau of Statistics to calculate per capita energy consumption. The combined population of NSW and ACT was used for the NSW1 region.
Python File for ETL and Forecast ML Model:
Power BI Integration:

A dynamic date table was created in Power Query using the M language, configured to automatically adjust with new data additions.
The operational demand data was grouped by hour and structured into a star schema for optimized reporting.
Custom measures were defined using DAX, and interactive visualizations were built to uncover actionable insights.
![Screenshot 2025-04-15 032536](https://github.com/user-attachments/assets/8bbf678a-511f-440e-8025-e6460ceb1f33)

2. Key Insights
1. Per Capita Operational Demand
Tasmania recorded the highest operational demand per 1,000 persons, suggesting a higher individual energy usage relative to other regions. This trend highlights a strong opportunity for targeted energy conservation programs in collaboration with Tasmanian stakeholders. Explore Tasmania data

2. Total Energy Demand
The NSW1 region exhibited the highest overall energy demand, accumulating approximately 21 million megawatt-hours during the reporting period. This is directly tied to its larger population size, underlining the importance of enhanced resource allocation, grid resilience planning, and budget forecasting. NSW1 energy profile
3. Demand Anomalies
An unexpected drop in energy demand was observed on 27th March 2025. This anomaly requires further analysis to determine potential causes, such as:

Extreme weather conditions
Grid maintenance or outages
Changes in industrial or residential usage patterns
Engaging with AEMO or regional energy providers may provide further clarity. Investigate anomaly
4. Daily Demand Patterns
Morning Peaks (~7:00 AM):
Consistently high demand aligns with household morning routines and commercial activity startups.
Evening Peaks (6:00 PM – 9:00 PM):
The highest demand levels were observed during this period, especially on Tuesdays and Wednesdays, likely reflecting a blend of residential and commercial energy use. 
3. Recommendations
Energy Efficiency Initiatives for Tasmania
Collaborate with local councils and utilities to promote energy-saving habits and explore smart energy infrastructure investments.
Strategic Planning for NSW1
Prioritize infrastructure expansion, renewable energy integration, and demand-side management initiatives to cater to NSW1’s growing needs.
Anomaly Tracking & Forecast Accuracy
Regularly compare forecasted vs. actual demand trends to fine-tune predictive models and prepare for potential demand surges or drops.
![Screenshot 2025-04-15 034638](https://github.com/user-attachments/assets/58961906-4085-4723-b433-9db6d10f565c)
