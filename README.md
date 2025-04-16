# Module 20 Capstone Assignment

## Overview
This project explores how machine learning models can predict optimal ski conditions and season length, specifically focusing on Lake Tahoe ski resorts, by analyzing historical weather patterns and climate indicators. The analysis leverages data from multiple sources to identify the key factors influencing ski season duration in the Lake Tahoe region.

The Jupyter workbook that was used to come to the above findings is available in this GitHub repository here: [Capstone_InitialReport_and_EDA.ipynb](https://github.com/cjplumer/module20_submission/blob/2c2b72e9389cbf126447a26623c6b2597e218a9d/Capstone_InitialReport_and_EDA.ipynb)


## Research Question
How can machine learning models predict optimal ski conditions and season length for Lake Tahoe ski resorts by analyzing historical weather patterns and climate indicators?

## Data Sources
The analysis combines three primary datasets:
- NOAA weather station data from multiple locations around Lake Tahoe (2014-2025)
- Historical ski resort opening and closing dates for four major Tahoe resorts
- NOAA Oceanic Niño Index (ONI) data for El Niño/La Niña climate patterns

## Methodology

### Data Collection and Processing
1. Collected daily weather observations from NOAA stations in the Lake Tahoe area
2. Gathered opening and closing dates for Heavenly, Palisades, Sugar Bowl, and Kirkwood resorts
3. Integrated climate oscillation data (ONI) to capture broader weather patterns
4. Cleaned and aligned datasets to create a comprehensive analytical framework

### Feature Engineering
The analysis created several derived features to capture weather patterns:
- Rolling averages and sums for key metrics (7, 14, and 30-day windows)
- Cumulative seasonal values (total snowfall, precipitation, freezing days)
- Pre-season conditions (Nov 1 to resort opening)
- Total season metrics for each resort's operational period

### Modeling Approach
- Implemented a Random Forest Regression model to predict season length
- Used features including pre-season snow, ONI values, and resort-specific factors
- Evaluated performance using RMSE, MAE, and R² metrics

## Results

### Key Findings
1. Total seasonal snowfall shows a positive correlation with season length
2. Climate oscillations (El Niño/La Niña) demonstrate measurable influence on Tahoe ski seasons
3. Pre-season snowfall impacts resort opening dates
4. Distinct patterns emerge for different resorts based on elevation and location

### Model Performance
- The Random Forest model achieved:
  - RMSE: 25.25 days
  - MAE: 18.88 days
  - R² Score: 0.44
- Most important predictive features include:
  - Preseason_Freeze_Days
  - Resort_Palisades
  - Preseason_Prcp
  - Seasonal_ONI
  - Preseason_Snow
  - Snow_Depth_At_Opening
  - Resort_Kirkwood
  - Resort_Sugar
  - Resort_Heavenly

### Visualizations
The analysis produced several informative visualizations:
- Relationship between seasonal ONI values and season length
- Correlation between total seasonal snowfall and operating days
- Pre-season snow accumulation and opening date patterns
- Season length distributions by resort

## Implications
The findings suggest that:
1. Climate indicators can provide valuable early signals for resort operational planning
2. Resorts should consider different factors when planning opening vs. closing dates
3. El Niño/La Niña patterns offer insights for longer-term seasonal forecasting

## Limitations
- Limited historical data (only covering seasons since 2014-2015)
- Potential gaps in weather station observations
- Simplified representation of complex weather systems

## Next Steps
Potential extensions of this analysis include:
1. Incorporating additional climate indicators (Pacific Decadal Oscillation, atmospheric rivers)
2. Exploring time-series approaches (ARIMA, LSTM) for more granular predictions
3. Adding snowpack quality metrics beyond simple depth measurements
4. Expanding to include more resorts across different geographic regions
5. Developing separate models for opening and closing date predictions
