Dataset Information

The dataset contains 10,886 records and 12 columns representing hourly bike rental data and associated environmental variables.

Features Used
Feature	Description
datetime	Date and time of observation
season	Spring, Summer, Fall, Winter
holiday	Whether the day is a holiday
workingday	Whether the day is a working day
weather	Weather condition category
temp	Actual temperature (°C)
atemp	Feeling temperature (°C)
humidity	Relative humidity (%)
windspeed	Wind speed (km/h)
casual	Count of casual users
registered	Count of registered users
count	Total rentals (Target Variable)
Project Objectives
Perform comprehensive EDA
Identify outliers and distribution patterns
Analyze relationships between key variables and demand
Conduct hypothesis testing
Generate statistically validated business insights
Recommend actions to improve demand and revenue
Exploratory Data Analysis (EDA)
Data Quality Checks
No missing values
No duplicate records
Converted categorical variables to category datatype
Converted datetime to proper datetime format
Key EDA Findings
Rental demand (count) is right-skewed with substantial variability
Weather and season strongly influence demand
Temperature has a positive relationship with rentals
Working day has minimal impact
Clear weather leads to much higher rentals
Summer and fall show the highest average demand
Hypothesis Testing
1. Independent 2-Sample T-Test

Objective: Determine whether working day affects bike rentals.

Null Hypothesis (H₀): Mean rentals are the same on working and non-working days.
Result: p-value = 0.216 (> 0.05)
Conclusion: Fail to reject H₀. Working day does not have a statistically significant impact.
2. ANOVA (Analysis of Variance)

Objective: Test whether rentals differ across weather and seasons.

Weather vs Count
p-value = 5.48e-42
Significant differences across weather categories
Season vs Count
p-value = 6.16e-149
Significant differences across seasons
Post-Hoc Analysis (Tukey HSD)
Identified specific groups with significant differences
Clear weather had much higher rentals than adverse conditions
All seasonal pairs showed significant differences
3. Chi-Square Test of Independence

Objective: Determine whether weather is dependent on season.

p-value = 1.55e-07
Reject H₀
Weather and season are statistically associated
Key Statistical Insights
Ranked Drivers of Demand
Weather
Season
Temperature
Working Day
Quantitative Highlight

Average rentals in clear weather are approximately 205, compared with 119 in rainy conditions, representing a 40–45% decline in demand.

Business Recommendations
Increase bike availability dynamically during favorable weather and peak seasons
Introduce discounts during poor weather to maintain utilization
Optimize fleet distribution based on seasonal trends
Use weather forecasts for operational planning
Promote leisure and weekend usage
Limitations
No pricing, location, or demographic information
External factors such as fuel prices and public transport are excluded
count is derived from casual + registered, which should be considered in predictive modeling to avoid data leakage
Tools and Technologies
Python
Pandas
NumPy
Matplotlib
Seaborn
SciPy
Statsmodels
Jupyter Notebook
