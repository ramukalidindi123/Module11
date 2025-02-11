# Module11
# **Used Car Price Prediction - CRISP-DM Approach**
## Project Overview 
This project aims to analyze and predict used car prices based on various factors such 
as **vehicle condition, mileage, manufacturer, fuel type, drivetrain, and more**. Using a structured data science methodology, we implement different 
**regression models** to provide insights and recommendations for a used car dealership.
## **🔹 CRISP-DM Framework**
The project follows the **CRISP-DM (Cross Industry Standard Process for Data Mining)** methodology:
## **1 Business Understanding**
The goal is to determine key factors that influence the price of used cars and provide actionable insights for a used car dealership
Which car attributes (e.g., make, model, year, mileage, condition, features) have the greatest impact on price?

### **Key Business Questions**
1. Are certain Mak/models more valuable in the used market?
2. How do car condition, mileage, and other features affect price
3. What trends exist based on region or fuel type
4.  What Insights  can be given to the dealership to optimize pricing and purchasing
## **2️⃣ Data Understanding**
### **Dataset Overview**
The dataset contains information on **426,000 used cars** with features including:

| Column Name         | Description |
|---------------------|-------------|
| `id`               | Unique identifier |
| `region`           | Region where the car is listed |
| `price`            | Selling price (target variable) |
| `year`             | Model year |
| `manufacturer`     | Car brand (e.g., Toyota, Ford) |
| `model`            | Car model |
| `condition`        | Vehicle condition (new, excellent, good, etc.) |
| `cylinders`        | Engine type |
| `fuel`             | Fuel type (gas, diesel, hybrid, electric) |
| `odometer`         | Total miles driven |
| `title_status`     | Title type (clean, salvage, etc.) |
| `transmission`     | Automatic or manual |
| `drive`            | Drivetrain (FWD, RWD, AWD) |
| `size`             | Vehicle size |
| `type`             | Vehicle type (SUV, truck, sedan, etc.) |
| `paint_color`      | Exterior color |
| `state`            | U.S. state where the car is listed |

### **Exploratory Data Analysis (EDA)**
- **Missing Data Analysis**: Identified missing values in `condition`, `drive`, `cylinders`, and more.
- **Outlier Detection**: Removed Outliers in price and Odometer manually instead of 		 
- **Feature Correlation**: Examined relationships between `price` and other variables.

---
## **3️ Data Preparation**
### **Cleaning Steps**
    ** calculated percatnge of missing data for ecah columns and made necessary cleansing decisions
    **Removed extreme outliers** in `price` (kept only cars between **$500 - $500,000**).  
    **Imputed missing values** for categorical columns like `condition`, `drive`, and `fuel`.  
    **Dropped unnecessary columns** ( `VIN`, ' Size' ) that do not impact price.  
**Created new features**:
- **`car_age = 2024 - year`** → Captures depreciation impact.
- **`manufacturer_location`** → Categorized manufacturers by country (`America, Japan, Germany, etc.`).


## **Modeling**
### **Regression Models Used**
## Linear Regression", "Polynomial Regression", "Decision Tree", "Random Forest


---
## ** Evaluation & Insights**
### **Key Findings**
✔ **Car Condition & Age Matter Most**: Newer and well-maintained cars have **higher resale value**.  
✔ **Luxury Brands Hold Value**: Toyota, Honda, BMW, and Mercedes retain their worth **better than American brands**.  
✔ **Fuel Type & Drivetrain Influence Price**: Hybrid/electric cars are priced higher, and AWD/4WD vehicles are valued more in **snow-prone regions**.  

### **Cross-Validation & Metrics**
- **Root Mean Squared Error (RMSE)** → Evaluates model accuracy.

## **💡 How to Run the Project**
### **🔹 Prerequisites**
- Python 3.8+
- Libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `sklearn`, `xgboost`

```

---
## **📜 Conclusion**
This project successfully predicts **used car prices** by analyzing key features such as **condition, mileage, manufacturer, fuel type, and drivetrain**. The insights generated can help **dealerships make data-driven pricing decisions**.
