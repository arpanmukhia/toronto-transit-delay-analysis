# 🚇 Toronto Transit Delay Analysis

## Project Overview
This project analyzes TTC transit delay data to understand when, where, and why delays occur across the network. The analysis combines TTC delay records with weather data, explores operational delay patterns, and presents the findings through a Tableau dashboard.

## Objective
The goal of this project is to identify:
- Peak hours when delays happen most often
- Hours when delays are most severe
- Lines and stations with the highest delay impact
- Whether weather has a noticeable relationship with delays
- Whether a simple machine learning model can classify longer delays

## Tools Used
- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Tableau Public
- VS Code / Jupyter Notebook
- GitHub

## Dataset
The project uses:
- TTC delay records
- Daily weather data

The datasets were cleaned, merged by date, and prepared for analysis using Python.

## Key Features Created
- `hour` — extracted from delay time
- `day_name` — day of the week
- `month` — month of delay
- `is_weekend` — weekday vs weekend flag
- `datetime` — combined date and hour
- `delay_label` — classification label for delays over 10 minutes

## Key Insights
- Delay frequency is highest during peak commuting hours, especially around 7–9 AM and 4–6 PM.
- The most severe delays occur during early morning hours, showing that fewer incidents can still cause longer disruptions.
- Weekend delays are slightly higher on average compared to weekdays.
- Stations such as Eglinton, Kipling, and Sheppard West show consistently high delay impact.
- Delay patterns vary by line, suggesting uneven operational performance across the network.
- Weather was explored, but the stronger patterns came from time, station, and line-level factors.

## Tableau Dashboard
The Tableau dashboard summarizes delay patterns by hour, weekday/weekend, line, and station.

![Tableau Dashboard](dashboard/dashboard.png)

## Machine Learning Component
A simple classification model was created to predict whether a delay would be longer than 10 minutes.

The model used:
- Hour of day
- Mean temperature

The purpose of the model was not to build a perfect prediction system, but to test whether basic features could help identify higher-impact delays.

## Project Structure

toronto-transit-delay-analysis/
│
├── data/
│ ├── ttc_delays.csv
│ ├── weather.csv
│ └── cleaned_data.csv
│
├── notebooks/
│ └── ttc_analysis.ipynb
│
├── dashboard/
│ └── dashboard.png
│
└── README.md


## Conclusion
This project shows how transit delay data can be cleaned, explored, visualized, and used for basic predictive modeling. The strongest findings came from operational patterns such as hour of day, station, and line, rather than weather conditions. These insights can help identify where service reliability issues are concentrated and where further investigation may be useful.

## Author
Arpan Mukhia
