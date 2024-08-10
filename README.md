# Bike Sharing Demand Prediction using AutoGluon

This repository contains my project on predicting bike-sharing demand using the AutoGluon library, as part of the Kaggle Bike Sharing Demand competition.

## Project Overview

The goal of this project was to predict bike-sharing demand using historical data. Accurate predictions of bike-sharing demand are crucial for companies like Uber, Lyft, and DoorDash to prepare for spikes in services and improve customer experience by reducing delays.

This project demonstrates the use of AutoGluon for training multiple iterations of models and optimizing them for better predictions. The process included initial model training, exploratory data analysis (EDA), feature engineering, hyperparameter tuning, and model evaluation.

## Dataset

The dataset was provided by the Kaggle competition and contains the following features:

- **datetime**: Date and time of the observation
- **season**: Season of the year
- **weather**: Weather situation
- **temp**: Temperature in Celsius
- **atemp**: "Feels-like" temperature in Celsius
- **humidity**: Humidity level
- **windspeed**: Wind speed
- **casual**: Number of casual users
- **registered**: Number of registered users
- **count**: Total number of bike rentals (target variable)

## Project Phases

### 1. Initial Training

Initially, models were trained using the provided data without any modifications. It was crucial to ensure that all predicted values were non-negative, as negative predictions for bike-sharing demand are unrealistic.

**Top-performing model**: WeightedEnsemble_L3, which combines predictions from multiple base models to capture diverse aspects of the data.

### 2. Exploratory Data Analysis and Feature Creation

During EDA, histograms were plotted to understand the distribution of features. This analysis led to the creation of additional datetime-based features such as hour, day, week, month, and year, which helped capture temporal patterns in the data.

**Impact of additional features**: The model's performance improved significantly, with the Kaggle score decreasing from 1.80344 to 0.61088, indicating a better fit.

### 3. Hyperparameter Tuning

Further tuning of hyperparameters led to a slight improvement in model performance, with the score decreasing to 0.50732.

### 4. Final Results

The iterative process of model training, feature engineering, and hyperparameter tuning culminated in a model capable of making accurate predictions. The final model was submitted to the Kaggle competition, achieving a competitive rank.

| Model           | HPO1        | HPO2        | HPO3        | Kaggle Score |
|-----------------|-------------|-------------|-------------|--------------|
| Initial         | -53.137922  | -53.444992  | -55.076511  | 1.80344      |
| After Features  | -30.440743  | -30.711589  | -31.140419  | 0.61088      |
| After HPO       | -33.975272  | -33.975272  | -34.941020  | 0.50732      |

## Summary

This project highlights the importance of iterative model development, including thoughtful feature engineering and careful hyperparameter tuning, in achieving accurate predictions. The improvements made at each stage of the project demonstrate the potential of AutoGluon for handling complex machine learning tasks with minimal manual intervention.

## Future Work

Given more time, I would explore training the dataset on the top 5 performing algorithms individually, experimenting with different hyperparameters to further refine the model and achieve even better predictions.

## License

This project is licensed under the MIT License - see the LICENSE file for details.
