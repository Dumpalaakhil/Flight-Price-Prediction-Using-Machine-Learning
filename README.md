# Flight Price Prediction Using Machine Learning

## Project Overview
This project focuses on predicting flight ticket prices using machine learning techniques. It uses a structured flight dataset containing journey, airline, route, duration, stop, and timing information to build predictive models for airfare estimation.

The main aim of this study is to compare multiple regression models and identify the most accurate approach for predicting flight prices. The project shows how data cleaning, feature engineering, encoding, scaling, and model evaluation can improve prediction performance in a real-world travel pricing problem.

## Research Objective
The objective of this project is to develop and evaluate machine learning models that can accurately predict flight ticket prices based on flight-related features.

This study also aims to:
- Understand the major factors influencing ticket prices
- Apply effective data preprocessing and feature engineering techniques
- Compare different regression models using standard evaluation metrics
- Identify the best-performing model for flight price prediction

## Dataset
The dataset used in this project contains flight-related information such as:
- Airline
- Source city
- Destination city
- Flight date
- Departure time
- Arrival time
- Duration
- Number of stops
- Travel class
- Price

## Data Preprocessing
Several preprocessing steps were performed to make the dataset suitable for machine learning:

- Removed empty and duplicate columns/rows
- Standardised column names
- Trimmed unnecessary whitespace in text columns
- Converted `flight_date` into datetime format
- Converted departure and arrival times into minutes
- Cleaned and converted `price` into numeric format
- Converted duration into total minutes
- Extracted number of stops from text values
- Created additional date-based features such as:
  - flight day
  - flight month
  - flight weekday
- Renamed route columns for clarity
- Standardised categorical text values
- Handled missing values using imputers
- Applied one-hot encoding to categorical variables
- Applied scaling to numerical variables

## Exploratory Data Analysis
Exploratory data analysis was carried out to understand the structure and behaviour of the dataset. Key analyses included:

- Distribution of flight prices
- Log-transformed price distribution
- Correlation analysis of numerical features
- Price distribution by airline
- Model comparison plots
- Actual vs predicted price plots
- Residual distribution analysis
- Density comparison of actual and predicted prices

## Machine Learning Models Used
The following regression models were implemented and compared:

1. Linear Regression  
2. Decision Tree Regressor  
3. Random Forest Regressor  
4. Gradient Boosting Regressor  

## Model Training
The cleaned dataset was split into training and testing sets using an 80:20 ratio.

A machine learning pipeline was created using:
- `ColumnTransformer`
- `Pipeline`
- `SimpleImputer`
- `StandardScaler`
- `OneHotEncoder`

This ensured that preprocessing and modelling were combined into a single workflow for reliable training and evaluation.

## Evaluation Metrics
The models were evaluated using the following metrics:

- **MAE (Mean Absolute Error)**
- **RMSE (Root Mean Squared Error)**
- **R² Score**

These metrics were used to compare model accuracy and overall predictive performance.

## Results
The model comparison results are shown below:

| Model | MAE | RMSE | R² |
|------|------:|------:|------:|
| Random Forest Regressor | 1803.49 | 3511.10 | 0.9767 |
| Decision Tree Regressor | 2600.47 | 4796.76 | 0.9566 |
| Gradient Boosting Regressor | 2864.23 | 4998.66 | 0.9529 |
| Linear Regression | 4691.97 | 8088.46 | 0.8766 |

## Best Performing Model
The **Random Forest Regressor** achieved the best performance among all tested models.

### Why it performed best:
- Lowest MAE
- Lowest RMSE
- Highest R² score
- Better ability to capture non-linear relationships in the data

## Key Insights
- Flight price prediction can be effectively solved using supervised machine learning
- Features such as airline, duration, route, stops, and travel timing significantly affect ticket prices
- Proper preprocessing and feature engineering improved model performance
- Ensemble models outperformed the basic linear model
- Random Forest provided the most accurate and reliable predictions in this project
