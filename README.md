# Car Price Prediction
Car_Name: Name of the car

Year: Year of manufacture

Selling_Price: Price at which the car is being sold

Present_Price: Current market price of the car

Kms_Driven: Total kilometers driven

Fuel_Type: Type of fuel the car uses (e.g., Petrol, Diesel)

Seller_Type: Type of seller (e.g., Dealer, Individual)

Transmission: Type of transmission (e.g., Manual, Automatic)

Owner: Number of previous owners

__________
dataset: car_price_prediction_incorrect.ipynb
### Feature Engineering
1. Generated new columns:

Car_Age: Car age (2019 - Year). 2019 is the maximum of year in this dataset + 1.

2. Turn text into numerical data with one-hot encoding

Applied on Fuel_Type, Seller_Type and Transmission columns.

3. Transformation

Present_Price and Kms_Driven are right-skewed. So normalize data distributions will improve the performance. 
![image](https://github.com/user-attachments/assets/87de0a61-3f6a-49ad-b06f-d00ce6f1151a)

![image](https://github.com/user-attachments/assets/280b0af0-0785-473c-9349-b110c40943ca)

### Evaluate Model
Training Data - Mean Squared Error (MSE): 0.60

Training Data - R² Score: 0.98

Test Data - Mean Squared Error (MSE): 1.06

Test Data - R² Score: 0.95

The model is overfitting. So I decided to check with cv.

Average Cross-Validated MSE: 1.673049547195078e+23
Average Cross-Validated R² Score: -8.615993705516049e+21

Given the persistent issues with extremely high Mean Squared Error (MSE) and extremely negative R² scores, even in simpler models like linear regression without polynomial features, it's clear that linear models may not be suitable for your dataset. These outcomes suggest a fundamental mismatch between the model type and the data characteristics, or possibly underlying issues with data quality or feature engineering. So, I redo the feature engineering section.

_________

### Redo Feature Engineering
1. Apply one-hot encoding correctly
2. Also apply log to Selling_Price.

### Result
Training Data - Mean Squared Error (MSE): 0.02

Training Data - R² Score: 0.97

Test Data - Mean Squared Error (MSE): 0.03

Test Data - R² Score: 0.95

Cross-Validated Mean Squared Error (MSE): 0.02

Cross-Validated R² Score: 0.96

The model performance is good and there is no overfitting indication.

