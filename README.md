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

### Feature Engineering
1. Generated new columns:

Car_Age: Car age (2019 - Year). 2019 is the maximum of year in this dataset + 1.

2. Turn text into numerical data with one-hot encoding

Applied on Fuel_Type, Seller_Type and Transmission columns.

3. Transformation

Present_Price and Kms_Driven are right-skewed. So normalize data distributions will improve the performance. 
![image](https://github.com/user-attachments/assets/e4d01e1b-ee4f-467d-88b0-9027bedc4710)

