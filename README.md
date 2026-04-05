# Mexico Real Estate Market Analysis

## 1. Overview

This project analyzes over 21,000 real estate listings in Mexico collected from Properati.com. The main objective is to understand the key factors that influence housing prices, with a focus on:

1. Property size
2. Geographic location

The project goes beyond basic analysis by combining data cleaning, geospatial visualization, and statistical analysis to extract meaningful insights.

---

## 2. Problem Statement

Real estate prices are influenced by multiple factors, but two of the most important are:

1. Property size (area in square meters)
2. Location (state and geographic coordinates)

This project aims to answer the following question:

Is property price driven more by size or by location?

---

## 3. Dataset Description

The dataset consists of three separate files that were merged after preprocessing. It includes:

1. Property prices (USD / MXN)
2. Area in square meters
3. Geographic coordinates (latitude and longitude)
4. State and location metadata

Total records: approximately 21,000 properties.

---

## 4. Data Preparation

### 4.1 Data Cleaning

1. Removed missing values from all datasets
2. Standardized column formats across datasets
3. Fixed inconsistent structures (e.g., splitting combined columns)

### 4.2 Currency Normalization

Prices originally in Mexican Peso were converted into USD to ensure consistency across the dataset.

### 4.3 Feature Engineering

1. Extracted `state` from hierarchical location data
2. Split `lat-lon` into separate `lat` and `lon` columns
3. Created a new feature:

* Price per square meter:

```
price_per_m2 = price_usd / area_m2
```

This feature was critical for fair comparison across regions.

---

## 5. Exploratory Data Analysis

### 5.1 Geospatial Analysis

The dataset includes latitude and longitude for each property, which enabled geospatial visualization.

Instead of treating location as raw numbers, it was transformed into an interactive map using Plotly.

Key idea:

Geographic coordinates (lat, lon) were used to visualize property distribution across Mexico.

Tool used:

Plotly (scatter_mapbox)

Purpose:

1. Understand spatial distribution of properties
2. Identify high-density areas
3. Explore how location impacts pricing

Insight:

Properties are highly concentrated in major urban areas, especially Mexico City, where prices are significantly higher.

---

### 5.2 Categorical Analysis (State)

State-level analysis revealed:

1. Uneven distribution of listings across regions
2. Some states dominate the dataset
3. Regional variation in pricing patterns

---

### 5.3 Numerical Analysis

Descriptive statistics showed:

1. Mean price is higher than median → right-skewed distribution
2. High standard deviation → large variability in prices
3. Presence of high-value outliers

---

### 5.4 Distribution Analysis

1. Property sizes are concentrated in mid-range values
2. Prices are heavily skewed due to expensive properties
3. Boxplots confirmed the presence of outliers

---

## 6. Key Analysis

---

## 6.1 Most Expensive Locations

Initial analysis using mean price per state was misleading due to size differences.

A more accurate metric was introduced:

Price per square meter

Key findings:

1. Mexico City has the highest price per square meter
2. Location plays a major role in price determination
3. Economic activity correlates with higher real estate prices

---

## 6.2 Size vs Price Relationship

### Correlation Analysis

Correlation between area and price:

Approximately 0.58

Interpretation:

Moderate positive relationship

---

### Regional Comparison

1. In smaller states (e.g., Morelos):
   Strong correlation between size and price

2. In major cities (e.g., Mexico City):
   Weak correlation

Interpretation:

In large urban areas, price is influenced more by location, demand, and economic factors than by size alone.

---

## 7. Key Insights

1. Location is the dominant factor in real estate pricing
2. Size has a moderate influence overall
3. Price per square meter is a more reliable metric than total price
4. Urban markets behave differently from smaller regions
5. Geospatial analysis provides deeper understanding than traditional methods

---

## 8. Tools and Technologies

1. Python
2. Pandas
3. Matplotlib
4. Plotly
5. Jupyter Notebook

---

## 9. Skills Demonstrated

1. Data Cleaning and Preprocessing
2. Data Transformation and Feature Engineering
3. Exploratory Data Analysis (EDA)
4. Geospatial Data Analysis
5. Data Visualization (Static and Interactive)
6. Statistical Analysis (Correlation)
7. Insight Generation and Business Understanding

---

## 10. Future Improvements

1. Build a machine learning model to predict house prices
2. Apply outlier detection and removal techniques
3. Perform feature scaling and selection
4. Develop an interactive dashboard (Streamlit or Power BI)
5. Extend the analysis to other countries (e.g., Brazil dataset)

---

## 11. Conclusion

This project demonstrates how raw real estate data can be transformed into actionable insights through data analysis.

The results show that:

Location is the most influential factor in pricing, especially in large cities, while property size plays a secondary role.

---
