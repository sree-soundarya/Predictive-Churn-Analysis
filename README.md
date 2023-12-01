# 🚀 Spotflix Churn Prediction and Forecast

Ever wondered how streaming platforms keep you hooked? Well, churn prediction is their secret sauce! 🍿 Churn prediction is like having a crystal ball for customer behavior. It helps predict when users might decide to bid farewell to our streaming haven.

Now, how do we pull off this streaming magic? 🎩✨ Using the treasure trove of data from Spotflix, we dive deep into user interactions, preferences, and habits. It's like a backstage pass to understand what keeps users binging and what might make them hit pause. Join us on this journey to peek into the future of streaming engagement! 🚀🎬

## Overview 
This project combines the power of Snowflake, Snowpark Python, and machine learning to predict customer churn and forecast user engagement patterns. We delve into customer demographics, show data, and subscription information to unravel insights that drive strategic decisions.

## Churn Prediction

#### Connection Establishment
We kick off by establishing a connection to the Snowflake database using Snowpark Python.

#### Data Selection
We curate customer demographics, shows, and subscription data from Snowflake for a comprehensive analysis.

#### Data Preprocessing
Before diving into machine learning, we perform crucial data preprocessing steps:

- Calculated Columns: Create a churn column using open and close date columns.
- Feature Engineering: Transform existing columns like view duration to derive meaningful insights.
- Data Cleaning: Tidy up the dataset by handling missing values, ensuring consistency, and imputing null values strategically.
- Encoding: Prepare the data for model training by encoding categorical columns.
  
#### Feature Selection and Model Training
Prior to training machine learning models, we conduct feature selection using chi-square test. The selection is based on significant columns identified through chi-square testing. Finally, we train a Random Forest model, evaluating performance metrics like MSE and R2.

## Time Series Forecasting
#### Connection Establishment
Similar to churn prediction, we establish a seamless connection to the Snowflake database using Snowpark Python.

#### Data Selection
For time series forecasting, we focus on historical customer and subscription data, preparing it for in-depth analysis.

#### Data Transformation and Aggregation
Transforming Snowflake data into a Pandas DataFrame, we aggregate based on 'view date' and derive additional insights such as the days a customer spent before leaving the platform.

#### Model Selection and Tuning
Choosing the XGBoost Regressor for its prowess in handling intricate data relationships, we fine-tune parameters like the learning rate, maximum depth, and number of estimators.

#### Streamlined Training and Forecasting
To streamline the entire process, we implement functions for creating datasets at the customer level, training models, and forecasting for various time periods.

Now our XGBoost model is ready to start forecasting customer viewing pattern for the next 6 months or 1 year. This will give us crucial insights to make better decisions.
