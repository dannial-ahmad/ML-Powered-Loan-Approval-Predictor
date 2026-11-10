# ML-Powered Loan Approval Predictor

A machine learning project that predicts whether a loan application will be **Approved** or **Rejected** based on applicant financial and demographic information.

Built with **Logistic Regression** and deployed as an interactive web app using **Gradio**.

---

## Project Overview

Banks and financial institutions receive thousands of loan applications. Manually reviewing each one is time-consuming. This project automates the initial screening process by training a binary classification model that predicts loan approval status using key features such as:

- Annual income
- Loan amount & term
- CIBIL score
- Asset values (residential, commercial, luxury, bank)
- Education & self-employment status
- Number of dependents

The model is wrapped in a simple Gradio interface so anyone can input applicant details and instantly get a prediction.

---

## Dataset

**File:** `loan_approval_dataset.csv`  
**Shape:** 4,269 rows × 13 columns

| Feature                      | Description                          |
|-----------------------------|--------------------------------------|
| `loan_id`                   | Unique identifier                    |
| `no_of_dependents`          | Number of dependents                 |
| `education`                 | Graduate / Not Graduate              |
| `self_employed`             | Yes / No                             |
| `income_annum`              | Annual income                        |
| `loan_amount`               | Requested loan amount                |
| `loan_term`                 | Loan duration (months)               |
| `cibil_score`               | Credit score (CIBIL)                 |
| `residential_assets_value`  | Value of residential assets          |
| `commercial_assets_value`   | Value of commercial assets           |
| `luxury_assets_value`       | Value of luxury assets               |
| `bank_asset_value`          | Bank balance / assets                |
| `loan_status`               | Target → Approved / Rejected         |

---

## Model Performance

| Metric              | Value      |
|---------------------|------------|
| Algorithm           | Logistic Regression |
| Test Accuracy       | ~72.9%     |
| Evaluation          | Accuracy + Confusion Matrix |

---

## Tech Stack

- **Python**
- **pandas** & **numpy** – data handling
- **matplotlib** & **seaborn** – visualization
- **scikit-learn** – Logistic Regression, metrics, train-test split
- **Gradio** – interactive web interface

---

## How to Run

### Option 1: Google Colab (Recommended)

1. Open `loan_aproval_predection.ipynb` in Google Colab.
2. Upload `loan_approval_dataset.csv` (or place it in `/content/`).
3. Run all cells in order.
4. The last cell launches a Gradio app with a public shareable link.

### Option 2: Local

```bash
# Clone the repository
git clone https://github.com/dannial-ahmad/ML-Powered-Loan-Approval-Predictor.git
cd ML-Powered-Loan-Approval-Predictor

# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn gradio

# Open and run the notebook
jupyter notebook loan_aproval_predection.ipynb
