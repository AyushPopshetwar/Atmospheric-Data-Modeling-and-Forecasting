# AeroTrend-Atmospheric-Data-Modeling-and-Forecasting

## Overview

This project analyzes meteorological and soil data from the INCOMPASS project with the goal of predicting air temperature (Ta). By examining the relationship between weather conditions like radiation, humidity, wind speed, and soil moisture, the project develops predictive models for temperature forecasting. The workflow includes data preprocessing, dimensionality reduction using PCA, and application of machine learning models such as Linear Regression and Random Forest. Visualization techniques are used to explore relationships and improve model understanding.

## Goals and Objectives

- Analyze and model meteorological data to understand the interplay between air temperature, relative humidity, soil physics, and energy fluxes using the INCOMPASS dataset.
- Preprocess data to handle missing values, outliers, and inconsistencies.
- Perform exploratory data analysis (EDA) using correlation matrices, scatter plots, and regression lines.
- Apply principal component analysis (PCA) for dimensionality reduction.
- Train predictive models such as Linear Regression, Random Forest, and Gradient Boosting.
- Evaluate model performance using metrics like MAE, MSE, and R².
- Examine seasonal and diurnal variations for meteorological insights.

## Dataset

- **Source:** Energy and Carbon Dioxide Fluxes, Meteorology, and Soil Physics Observed at INCOMPASS Land Surface Stations in India (2016–2017).
- **Stations:** Kanpur, Dharwad, and Berambadi.
- **Frequency:** 30-minute intervals.
- **Rows/Features:** ~3500 rows and 44 features per region.

### Key Features

- DateTime: Timestamp of the observation
- H: Sensible heat flux (W/m²)
- LE: Latent heat flux (W/m²)
- Tau: Friction velocity (m/s)
- NEE: Net ecosystem exchange of CO₂ (μmol CO₂/m²/s)
- CO2 strg: CO₂ storage (μmol CO₂/m²/s)
- Pa: Atmospheric pressure (Pa)
- Ta: Air temperature (°C)
- RH: Relative humidity
- SWin/SWout/LWin/LWout: Incoming/outgoing shortwave and longwave radiation (W/m²)
- Rnet: Net radiation (W/m²)
- G1/G2: Soil heat flux at 5cm/10cm (W/m²)
- Tsoil, VWC: Soil temperature and volumetric water content at various depths
- Precipitation: Rainfall (mm)
- WS/WD: Wind speed/direction at multiple heights
- Ustar, TKE, Tstar, L, zL: Turbulence and boundary layer metrics
- x_peak, x_10, x_30, x_50, x_70, x_90: Spectral and frequency features

## Packages Required

- pandas
- requests
- numpy
- matplotlib.pyplot
- seaborn
- warnings
- missingno
- sklearn.decomposition.PCA
- sklearn.preprocessing.StandardScaler, OneHotEncoder
- sklearn.compose.ColumnTransformer
- sklearn.pipeline.Pipeline
- sklearn.impute.SimpleImputer
- sklearn.model_selection.train_test_split
- sklearn.linear_model.LinearRegression
- sklearn.ensemble.RandomForestRegressor, GradientBoostingRegressor
- sklearn.svm.SVR
- sklearn.metrics.mean_absolute_error, mean_squared_error, r2_score

## Approach

1. **Data Collection:** Download and load the INCOMPASS dataset.
2. **Data Cleaning:** Handle missing values and outliers; impute missing data.
3. **Exploratory Data Analysis:** Visualize distributions, relationships, and temporal patterns.
4. **Dimensionality Reduction:** Apply PCA to reduce feature space.
5. **Modeling:** Train and evaluate Linear Regression, Random Forest, Gradient Boosting, and SVR models.
6. **Evaluation:** Use MAE, MSE, and R² to assess model performance.

## Usage

1. Clone the repository.
2. Install the required dependencies.
3. Download and prepare the dataset.
4. Run the provided notebooks or scripts for data analysis and modeling.
5. Review results and visualizations.

## Results

- Machine learning models can effectively predict air temperature using meteorological and soil data.
- PCA helps reduce dimensionality and improve model interpretability.
- Visualization techniques reveal key patterns and relationships in the data.

## Future Work

- Incorporate additional meteorological stations and time periods.
- Explore deep learning models for improved forecasting.
- Integrate external climate and remote sensing data for enhanced predictions.
