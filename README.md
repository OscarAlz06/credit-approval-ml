# Car Loan Approval Prediction Model (Sales-Oriented Approach)

## Project Description
This project develops a machine learning model to predict car loan approvals in a dealership context, with the objective of optimizing commercial performance and maximizing the identification of potential customers.

The model is designed to support the sales team by prioritizing customers with a high likelihood of approval.

---

## Objective
Build a predictive model that enables:

- Identification of as many potentially approvable customers as possible  
- Reduction of missed commercial opportunities  
- Prioritization of leads for the sales team  

---

## Dataset
The dataset contains customer and loan application information, including:

- Sociodemographic variables (e.g., gender, employment profile)  
- Financial variables (income, expenses, payment capacity)  
- Vehicle information (new/used)  
- Target variable:
  - `resultado`:  
    - 1 = Loan approved  
    - 0 = Loan rejected  

### Key Consideration
The dataset presents a **high class imbalance** (~95% rejected vs ~5% approved).

---

## Data Preprocessing

The following steps were applied:

- Removal of missing values  
- Standardization of column names  
- Binary encoding of categorical variables  
- Scaling of monetary variables (to millions of currency units)  
- Conversion of all variables to numeric format  
- Removal of extreme outliers (measurement errors)  

---

## Exploratory Data Analysis (EDA)

The analysis included:

### Target Variable
- Identification of significant class imbalance  

### Continuous Variables
- Outlier detection and removal using boxplots  

### Discrete Variables
- Analysis of approval proportions by category  

### Correlation
- Evaluation of relationships between variables  

---

## Handling Class Imbalance

The following approach was implemented:

- Random undersampling without replacement on the training set  
- Approximate 60-40 class balance  

The test set was kept **unchanged** to simulate real-world conditions.

---

## Models Evaluated

The following models were trained and compared:

- Logistic Regression  
- Decision Tree  
- Random Forest  
- XGBoost  

Each model was evaluated on:
- Original (imbalanced) dataset  
- Balanced dataset  

---

## Evaluation Metrics

Given the commercial focus, the main metric was:

- **Recall (primary metric)** – to capture as many potential customers as possible  

Additional metrics:
- Precision  
- ROC-AUC  
- Precision-Recall curves  

---

## Selected Model

### Random Forest (balanced dataset)

- **Recall:** 0.80  
- **Precision:** 0.0837  

---

## Results Interpretation

The model achieves:

- Identification of **80% of potentially approvable customers**  
- Improvement over the random baseline (~5%) with a precision of **8.37%**  

### Commercial Use Case

The model is designed to:

- Prioritize leads with higher approval likelihood  
- Optimize sales team efforts  
- Serve as an initial filtering tool in the sales process  

It is not intended to directly approve loans, but rather to support commercial decision-making.

---

## Limitations

- Low precision due to class imbalance  
- High number of false positives  
- Limited predictive power of individual variables  

---

## Future Work

- Feature engineering to improve precision  
- Hyperparameter tuning (GridSearchCV)  
- Evaluation of oversampling techniques (e.g., SMOTE)  
- Threshold optimization based on business objectives  

---

## Conclusions

- The model is effective for identifying commercial opportunities  
- It reduces the risk of missing potential customers  
- It should be used as a prioritization tool, not a final decision system  
- Its value lies in maximizing the reach of the sales team  

---

## Technologies Used

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Imbalanced-learn  
- Matplotlib / Seaborn  

---

## Author

Developed by Oscar Ivan Alzate Martinez