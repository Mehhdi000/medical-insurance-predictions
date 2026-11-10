# Insurance Cost Prediction and Feature Engineering

An exploratory machine learning project focused on predicting medical insurance charges with an emphasis on transparency, feature engineering, and model interpretability. Built as a hands-on learning project to evaluate why interpretable white-box models can outperform complex algorithms when paired with robust domain logic.

---

## Core Skills & Technical Stack

* **Data Analysis & Preprocessing:** Handled data cleaning, structure organization, and exploratory sanity checks.
  * **Libraries:** Pandas, NumPy

* **Feature Engineering:** Designed targeted interaction terms based on real-world risk factors to capture non-linear compounding effects.
  * **Libraries:** Pandas

* **Supervised Learning:** Trained, tuned, and compared linear regression against tree-based algorithms.
  * **Libraries:** Scikit-Learn, XGBoost

* **Model Evaluation & Interpretation:** Conducted residual analysis, metric tracking, and coefficient-based feature importance auditing.
  * **Libraries:** Scikit-Learn, Matplotlib, Seaborn

---

## The Dataset

The project utilizes a standard medical insurance dataset containing demographic and health characteristics for individuals. The structure includes:

* **`age`**: Age of the primary beneficiary.
* **`sex`**: Gender of the contractor.
* **`bmi`**: Body mass index, measuring weight relative to height.
* **`children`**: Number of dependents covered by insurance.
* **`smoker`**: Smoking status of the individual.
* **`region`**: Residential area in the United States (northeast, southeast, southwest, northwest).
* **`charges`**: Individual medical costs billed by health insurance (the target prediction variable).

---

## Project Overview & Methodology

The primary objective was to move beyond black-box tuning and systematically investigate how domain-driven adjustments affect model performance. 

1. **Preprocessing and Exploration:** The workflow was separated into a dedicated cleaning notebook and a modeling notebook to ensure a structured data pipeline.
2. **Feature Engineering:** Rather than treating variables independently, high-impact drivers like smoking status, age, and BMI were combined into targeted interaction terms to model compounding financial risk accurately.
3. **Model Tournament:** Evaluated Linear Regression against tree-based algorithms (Random Forest and XGBoost) using identical feature sets.
4. **Interpretation:** Analyzed linear regression coefficients to isolate the exact mathematical impact of each feature on the predicted insurance charges.

<img width="1768" height="1298" alt="scattersmoke" src="https://github.com/user-attachments/assets/c1cd9c39-beff-44c1-865a-63de2c854194" />


---

## Key Results

* **Winning Model:** Linear Regression achieved an **$R^2$ score of 0.82**.
* **Model Comparison:** Linear regression outperformed Random Forest (~0.79) and XGBoost (~0.79) because the engineered interaction terms matched the underlying linear structure of the compounded risk factors.
* **Key Drivers:** Coefficient analysis proved that smoking status and tailored interaction flags accounted for the vast majority of the prediction weight.

<img width="1728" height="1302" alt="my_seaborn_plot" src="https://github.com/user-attachments/assets/856a2fe2-2505-4423-b1b3-735435e48b1c" />


---

## Repository Structure

```text
├── cleaning.ipynb         # Data preprocessing and structure cleanup
├── ml.ipynb               # Feature engineering, model training, and evaluation
├── .gitignore             # Excluded environment files and system checkpoints
└── README.md              # Project documentation
