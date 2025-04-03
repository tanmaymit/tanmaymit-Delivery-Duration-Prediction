# tanmaymit-Delivery-Duration-Prediction
This project aims to build a predictive model for estimating the total delivery duration of orders placed on DoorDash. The model predicts the time taken from the moment a consumer places an order to when it is delivered. Accurate predictions are crucial for enhancing customer experience and optimizing delivery operations.

Dataset

The dataset used in this project contains historical delivery records from DoorDash, including details about orders, restaurants, delivery conditions, and marketplace state at the time of order placement.

Key Features

Time-based features: created_at, actual_delivery_time, hour_of_day, day_of_week, is_weekend

Store-related features: store_id, store_primary_category, order_protocol

Order-related features: total_items, subtotal, num_distinct_items, min_item_price, max_item_price

Market conditions: total_onshift_dashers, total_busy_dashers, total_outstanding_orders

Predictions from other models: estimated_order_place_duration, estimated_store_to_consumer_driving_duration

The target variable is total_delivery_duration_seconds, which represents the total time (in seconds) taken for the delivery.

Data Preprocessing

Converted timestamps to datetime format and extracted relevant time-based features.

Created new features such as dasher_utilization_rate, order_to_dasher_ratio, average_item_price, and price_range.

Encoded categorical variables using LabelEncoder.

Handled missing and infinite values by replacing them with the median.

Standardized numerical features using StandardScaler.

Model Selection & Training

We implemented and compared the following machine learning models:

Linear Regression

Random Forest Regressor

XGBoost Regressor

Support Vector Regressor (SVR)

K-Nearest Neighbors (KNN) Regressor

Each model was trained on 80% of the dataset, while 20% was used for testing.

Model Evaluation

The models were evaluated using the following metrics:

Mean Absolute Error (MAE)

Root Mean Squared Error (RMSE)

R² Score (coefficient of determination)

Explained Variance Score (EVS)

The results were analyzed and compared to determine the best-performing model.

Results

Model

MAE

RMSE

R² Score

Explained Variance

Linear Regression

X

X

X

X

Random Forest

X

X

X

X

XGBoost

X

X

X

X

SVR

X

X

X

X

KNN

X

X

X

X

(Replace 'X' with actual results after execution.)

Conclusion

The project successfully built and compared multiple machine learning models to predict DoorDash delivery times. Based on performance metrics, the best model can be selected for future enhancements and real-world deployment.

Next Steps

Fine-tune hyperparameters for further improvements.

Explore deep learning approaches such as neural networks.

Incorporate external factors like weather, traffic, and holidays.

Deploy the model as an API for real-time predictions.

Repository Structure

historical_data.csv: Dataset file

doordash_delivery_model.py: Python script for data preprocessing, modeling, and evaluation

README.md: Project documentation

This project demonstrates practical machine learning techniques for delivery time estimation and can serve as a foundation for further optimizations.

