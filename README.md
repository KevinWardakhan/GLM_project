# Bike-Sharing Demand Analysis and Prediction Using Generalized Linear Models (GLM)

## Overview

This project investigates the factors influencing bike-sharing demand in urban areas. By leveraging a detailed dataset and employing Generalized Linear Models (GLM), we constructed predictive models to understand and forecast bike-sharing usage patterns. The results provide actionable insights that could guide operational improvements in bike-sharing systems.

This work is the result of a collaborative effort between **Kevin Wardakhan**, **Ibrahim Abdelatif**, and **Erwan Ouabdesselam**, showcasing teamwork and shared expertise throughout the project.

## Table of Contents

- [Objectives](#objectives)
- [Methodology](#methodology)
- [Results and Insights](#results-and-insights)
- [Future Improvements](#future-improvements)
- [Contributors](#contributors)

## Objectives

- Identify key environmental, temporal, and contextual factors affecting bike-sharing demand.
- Build and validate a robust predictive model to forecast demand.
- Use insights to better understand the behavior of users and inform management decisions for optimizing bike-sharing operations.

## Methodology

This project followed a structured and methodical approach with the following phases:

### 1. Data Preparation and Exploration

**Dataset:**  
The dataset consists of 1,817 observations with 13 explanatory variables, encompassing environmental, temporal, and contextual factors.

**Preprocessing:**
- Removed irrelevant columns and redundant data.
- Transformed categorical variables into factors to facilitate statistical analysis.
- Addressed missing data to ensure dataset completeness.
- Split the dataset into training (70%) and testing (30%) subsets for model building and evaluation.

**Exploratory Analysis:**
- Conducted descriptive statistical analysis to understand variable distributions.
- Visualized relationships between the predictors (e.g., temperature, humidity, season) and the target variable (number of bike rentals).

### 2. Statistical Analysis

**Correlation Matrix:**
- Identified strong correlations among variables to avoid multicollinearity (e.g., high correlation between temperature measures).

**Key Predictors Identified:**
- **Temperature:** Both mean and perceived temperatures show a positive influence on bike rentals.
- **Humidity:** High humidity negatively impacts bike usage.
- **Temporal Factors:** Demand is highest during peak commuting hours and in warmer seasons.

### 3. Modeling with GLM

**Transformations:**
- Applied Box-Cox transformation to normalize the bike rentals variable.
- Added quadratic terms for humidity to better capture its non-linear relationship with demand.

**Variable Selection:**
- Used forward, backward, and stepwise approaches with criteria like AIC, BIC, and Mallow's CP to determine the most impactful predictors.
- Compared and validated multiple models for performance.

**Model Assumptions:**
- Validated homoscedasticity, normality of residuals, and absence of multicollinearity.
- Performed ANOVA tests to ensure the statistical significance of included predictors.

### 4. Interaction Effects

Explored and included meaningful interactions to refine the model:
- **Time of Day × Season:** Seasonal variations in daily usage patterns.
- **Weather × Time of Day:** Behavior changes under varying weather conditions.
- **Temperature × Humidity:** Combined effect on user comfort and demand.

These interactions improved the model's explanatory power and predictive accuracy.

### 5. Model Evaluation

**Metrics:**
- Final model achieved an **MSE of 217.84**, indicating strong predictive accuracy.
- **AIC of 4674.7** confirmed model optimization relative to alternatives.

**Final Model:**
- Forward-selected model with interactions was chosen for its balance of simplicity and performance.

## Results and Insights

**Key Findings:**
- Temperature (mean and perceived) significantly increases bike rentals.
- High humidity reduces demand, highlighting user sensitivity to weather conditions.
- Seasonal and time-based patterns suggest higher demand during summer and peak hours.
- Weather and temporal interactions provide nuanced insights into user behavior.

**Practical Applications:**
- Redistribute bikes dynamically based on seasonal and hourly trends.
- Improve planning for extreme weather events to ensure optimal service availability.

**Model Performance:**
- Predicted values closely align with actual demand, with minimal error.

## Future Improvements

To further enhance the model and insights:

**Incorporate additional predictors:**
- Local events and public holidays.
- Infrastructure-related factors (e.g., bike lanes, station proximity).

**Explore advanced modeling techniques:**
- Machine learning approaches to capture non-linear relationships.
- Regularization methods like Ridge or LASSO regression to minimize overfitting.

## Contributors

- **Kevin Wardakhan**
- **Ibrahim Abdelatif**
- **Erwan Ouabdesselam**

This project represents a collaborative effort, with each contributor bringing unique perspectives and expertise. For questions, feedback, or collaboration opportunities, feel free to reach out or open an issue.
