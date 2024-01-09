# 🚀 Spotflix Churn Prediction and Forecast

Ever wondered how streaming platforms keep you hooked? Well, churn prediction is their secret weapon! It's a crystal ball for understanding customer behavior, foreseeing when users might say goodbye to our streaming world.

So, how does this magic work? 🎩✨ With subscription streaming service Spotflix's data treasure, we explore user interactions, preferences, and habits. It's like a backstage pass helping us figure out what makes users binge-watch and what might make them take a break. Come along as we explore the future of streaming engagement with actionable insights delivered on ThoughtSpot’s AI-powered analytics platform! 🚀🎬
Overview
In this project, we use Snowflake, Python, machine learning, and ThoughtSpot to predict customer churn and forecast user engagement patterns. We use ThoughtSpot’s AI-powered search experience and interactive liveboards to explore customer demographics and subscription information to uncover insights and run forecasts that guide strategic decisions. 


## Churn Prediction

### Connection Establishment
We kick off by establishing a connection to the Snowflake database using Snowpark Python.

### Data Selection
We curate customer demographics, shows, and subscription data from Snowflake for a comprehensive analysis.

### Data Preprocessing
Before diving into machine learning, we perform crucial data preprocessing steps:

- Calculated Columns: Create a churn column using open and close date columns.
- Feature Engineering: Transform existing columns like view duration to derive meaningful insights.
- Data Cleaning: Tidy up the dataset by handling missing values, ensuring consistency, and imputing null values strategically.
- Encoding: Prepare the data for model training by encoding categorical columns.

### 🌍 Discover who's sticking around and who's saying goodbye 
<img src = "images/churn_by_region.png" >

### Feature Selection and Model Training
Prior to training machine learning models, we conduct feature selection using chi-square test. The selection is based on significant columns identified through chi-square testing. Finally, we train a Random Forest model, evaluating performance metrics like MSE and R2.

### 🎲 Exploring Features: Dive into the impact each feature adds to our churn prediction game. 📊
<img src = "images/chi2testresult.png" width = 400 height = 300>

### Heatmap of Confusion Matrix: it's a glimpse into the accuracy and missteps of our churn predictions.
<img src = "images/confusion matrix.png" width = 400 height = 300>

### The Churn Risk Spectrum 📊 : 📈 We're not just predicting churn; we're classifying risk levels! Low, medium, or high 📉
<img src = "images/customers_classification.png" width = 400 height = 300>

## Time Series Forecasting
### Connection Establishment
Similar to churn prediction, we establish a seamless connection to the Snowflake database using Snowpark Python.

### Data Selection
For time series forecasting, we focus on historical customer and subscription data, preparing it for in-depth analysis.

### Data Transformation and Aggregation
Transforming Snowflake data into a Pandas DataFrame, we aggregate based on 'view date' and derive additional insights such as the days a customer spent before leaving the platform.

### Model Selection and Tuning
Choosing the XGBoost Regressor for its prowess in handling intricate data relationships, we fine-tune parameters like the learning rate, maximum depth, and number of estimators.

### Streamlined Training and Forecasting
To streamline the entire process, we implement functions for creating datasets at the customer level, training models, and forecasting for various time periods.

### Forecast for Next Month: 🚀 a sneak peek into the future of Spotflix
<img src = "images/customer_interactions_forecast.png" >

Now our XGBoost model is ready to start forecasting customer viewing pattern for the next 6 months or 1 year. This will give us crucial insights to make better decisions.

### Witness how we predict engagement levels and pinpoint those high-risk viewers 🌟
<img src = "images/customer_engagement.png" >

## Guide to use .tml files
For step-by-step instructions on how to import .tml files into your ThoughtSpot cluster please refer [How to use TML files](https://docs.thoughtspot.com/cloud/latest/scriptability#_how_to_use_tml_files)
