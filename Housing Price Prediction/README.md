# 🏡 King County House Price Prediction  

This project uses the **King County House Sales Dataset** (from Kaggle) to build regression models for predicting house prices.  
The goal is to compare **Ridge Regression**, **Lasso Regression**, and **Elastic Net Regression** and identify the most accurate model.  

---

## 📂 Dataset Overview  

The dataset contains **21,613 records** of house sales in King County (USA).  
Each record represents a house and its features at the time of sale.  

---

## 📑 Column Descriptions  

1. **id**: Unique identifier for each house sale  
2. **date**: Date of the house sale  
3. **price**: Sale price of the house (target variable)  
4. **bedrooms**: Number of bedrooms  
5. **bathrooms**: Number of bathrooms (can include fractional values, e.g., 1.5 = one full and one half bathroom)  
6. **sqft_living**: Square footage of the interior living space  
7. **sqft_lot**: Square footage of the lot (land area)  
8. **floors**: Number of floors (levels) in the house  
9. **waterfront**: Whether the property has a waterfront view (0 = No, 1 = Yes)  
10. **view**: Quality of the view from the house (0 = None, 1–4 = Better views)  
11. **condition**: Condition of the house (1 = Poor, 2 = Fair, 3 = Average, 4 = Good, 5 = Very Good)  
12. **grade**: Overall grade of the house, based on construction and design (1 = Lowest quality, 13 = Highest quality)  
13. **sqft_above**: Square footage of the house above ground  
14. **sqft_basement**: Square footage of the basement  
15. **yr_built**: Year the house was originally built  
16. **yr_renovated**: Year the house was last renovated (0 if never renovated)  
17. **zipcode**: ZIP code of the house location  
18. **lat**: Latitude coordinate of the property  
19. **long**: Longitude coordinate of the property  
20. **sqft_living15**: Average living area of the 15 nearest houses  
21. **sqft_lot15**: Average lot size of the 15 nearest houses  

---

## 🎯 Project Goal  

1. Perform **Exploratory Data Analysis (EDA)** to understand trends and correlations.  
2. Train and evaluate **Ridge, Lasso, and Elastic Net regression models**.  
3. Compare their performance to determine the **most accurate model** for predicting house prices.  

---

## ⚙️ Tech Stack  

- **Python** (Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn)  
- **Jupyter Notebook** for analysis and modeling  

---

## 🚀 How to Run  

1. Clone this repository:  
   ```bash
   git clone https://github.com/yourusername/kc-house-price-prediction.git
   cd kc-house-price-prediction
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
3. Run the Jupyter notebooks:
   ```bash
   jupyter notebook

##📊 Model Evaluation
Each model is evaluated using metrics such as:
1. Mean Squared Error (MSE)
2. Root Mean Squared Error (RMSE)
3. R² Score
4. Mean Absolute Error (MAE)

##📌 Notes
1. Outliers in features such as price, bedrooms, bathrooms, and sqft_living may impact performance.
2. Feature scaling and regularization parameters significantly affect Ridge, Lasso, and Elastic Net results.
