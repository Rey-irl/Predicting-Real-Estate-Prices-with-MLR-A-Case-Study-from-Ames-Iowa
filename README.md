# 🏠 Predicting Housing Prices Using Multiple Linear Regression

This project uses **Multiple Linear Regression (MLR)** to identify and quantify the most influential factors on **housing prices** in Ames, Iowa. The dataset includes a mix of numerical and categorical variables, and the analysis was conducted following the **CRISP-DM methodology**.

---

## 🔹 Objective

To predict housing prices based on multiple factors such as:
- Year built
- Square footage
- Number of bathrooms
- Fireplaces
- Condition ratings
- Geographic location
- House style and type

---

## 🧰 Methodology: CRISP-DM

1. **Business Understanding:** Identify the main drivers of house prices.
2. **Data Understanding:** Explore and describe the dataset (18 variables, 2,413 records).
3. **Data Preparation:** 
   - Log-transform skewed variables
   - Encode categorical variables using one-hot and ordinal encoding
   - Detect and remove outliers
4. **Modeling:** Apply and refine Multiple Linear Regression through 4 model iterations.
5. **Evaluation:** Use statistical metrics (Adjusted R², VIF, residual plots) to assess model quality.

---

## 📊 Key Insights

- **Best Model (Model 4):** Achieved an **Adjusted R² of 78.3%**
- **Significant Predictors:**
  - `Year_Built`, `Total_Bsmt_SF`, `First_Flr_SF`, `Full_Bath`
  - `Fireplaces`, `Latitude`, `Lot_Area`, `House Style (One-and-a-Half, Two-and-a-Half)`
- **Insignificant Predictors:** Variables like `Longitude`, number of kitchens, and certain house styles did not improve the model and were excluded.
- **Transformations:** Log transformation improved normality for skewed data.
- **Multicollinearity:** Controlled via VIF analysis and model refinement.

---

## 🧮 Final Regression Formula

Log(Sale_Price) = -46.06 + 0.0059×Year_Built + 0.0003×Lot_Frontage + 0.0783×Overall_Cond + 0.0003×Total_Bsmt_SF + 0.1405×Full_Bath + 0.0202×Bedroom_AbvGr + 0.1298×Fireplaces + 1.0375×Latitude + 0.1071×Log(Lot_Area) + 0.1218×Log(First_Flr_SF) + 0.0634×(1.5 Story House) + 0.2165×(2.5 Story House)


---

## 📚 References

- Ople, M. *Find the Right Property, Buy at the Right Price*. Wrightbooks, 2012.
- Pardoe, I. *Applied Regression Modeling*. Wiley, 2020.
- Cirillo, A. *R Data Mining*. Packt Publishing, 2017.
- Nguyen, H.H. et al. *Building Statistical Models in Python*, Packt, 2023.

---

## 🧠 Author

**Reyna Vargas**  
National College of Ireland  

---

## 💻 Tools Used

- Python (Pandas, Statsmodels, Seaborn, Matplotlib)
- Jupyter Notebook
- CRISP-DM Framework

---


