# campaign-analysis
# 📊 Personal Loan Campaign Analysis

---

## 🎯 Project Objective

The goal of this project is to:
- Clean and prepare bank marketing data for storage in a structured PostgreSQL database.
- Conduct exploratory data analysis (EDA) to understand customer behavior.
- Identify key patterns and factors affecting loan campaign success.
- Build a predictive machine learning model to estimate the likelihood of campaign success.

---

## 🗂️ Project Structure

- `loan_analysis.ipynb` – Jupyter notebook containing all steps: cleaning, EDA, modeling.
- `client.csv` – Cleaned client demographic data.
- `campaign.csv` – Campaign interaction history.
- `economics.csv` – Economic indicators relevant to the campaign.
- `charts/` – (Optional) Folder containing visualizations used in the analysis.

---

## 🧹 Data Cleaning Steps

- Removed duplicates and handled missing values.
- Mapped categorical variables (e.g. `yes` / `no` → boolean).
- Converted textual dates to proper datetime format.
- Split original dataset into three relational tables:
  - `client.csv`
  - `campaign.csv`
  - `economics.csv`

---

## 🔍 Exploratory Data Analysis (EDA)

Key insights:
- 📈 Older clients are slightly more likely to have mortgages, but no strong age difference was observed.
- 🧑‍🎓 Higher education level tends to correlate with higher campaign success.
- 💬 Clients previously contacted in successful campaigns are more likely to respond positively.

**Questions Answered:**
- What is the age distribution of loan takers?
- Does education level influence campaign success?
- Which job types respond most positively?
- Do previous campaign outcomes impact current results?

---

## 🤖 Predictive Modeling

A **Random Forest Classifier** was trained to predict `campaign_outcome`.

Steps:
1. Categorical encoding using `OneHotEncoder`.
2. Feature selection and train/test split.
3. Hyperparameter tuning using `GridSearchCV`.

**Model performance:**
- Accuracy: ~91%
- F1-score for positive class: ~0.55 (class imbalance)

---

## 🧠 Technologies Used

- Python
- Pandas, NumPy
- Seaborn, Matplotlib
- Scikit-learn
- Jupyter Notebook

---

## 📌 Future Improvements

- Handle class imbalance using oversampling (SMOTE) or class weights.
- Deploy the model using Streamlit for business users.
- Automate data ingestion pipeline into PostgreSQL.
