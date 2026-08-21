# 🏥 Medical Insurance Cost Predictor

Predicting medical insurance charges using **Multiple Linear Regression** and **Polynomial Regression**, while exploring how increasing model complexity affects performance.

## 📌 Project Overview

This project predicts medical insurance charges based on a person's demographic and health-related attributes using the **Medical Cost Personal Dataset** from Kaggle.

Instead of training only one model, I compared **Multiple Linear Regression** with **Polynomial Regression (Degree 2–5)** to understand whether a more complex model actually improves prediction accuracy.

## 📊 Dataset

- **Source:** Kaggle – Medical Cost Personal Dataset
- **Records:** 1,338
- **Target Variable:** `charges`

### Features

| Feature | Type |
|---------|------|
| `age` | Numerical |
| `sex` | Categorical |
| `bmi` | Numerical |
| `children` | Numerical |
| `smoker` | Categorical |
| `region` | Categorical |
| `charges` | Target |

## 🚀 What I Implemented

- Data preprocessing with Pandas
- One-Hot Encoding using `ColumnTransformer` and `OneHotEncoder`
- Train/Test split (80/20)
- Multiple Linear Regression
- Polynomial Feature Generation (Degree 2–5)
- Model comparison on unseen test data

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Jupyter Notebook

## 📈 Model Performance

| Model | R² Score | MAE |
|-------|---------:|----:|
| **Multiple Linear Regression** | **0.870** | **2652.41** |
| Polynomial Regression (Degree 2) | ~0.86 | — |
| Polynomial Regression (Degree 3) | 0.843 | 3002.74 |
| Polynomial Regression (Degree 5) | ~0.34 | Much worse |

## 🔍 Key Findings

- Multiple Linear Regression performed best on the test set.
- Increasing the polynomial degree did not improve performance.
- Higher polynomial degrees eventually caused **overfitting**, leading to a significant drop in test accuracy.

> **Key takeaway:** A more complex model does not always produce better predictions.

## 🧩 Challenges Faced

While building this project, I encountered and resolved several practical implementation issues:

- Correct use of `fit_transform()` vs `transform()`
- One-Hot Encoding with `ColumnTransformer`
- Converting Pandas Series to NumPy arrays for reshaping
- Matching prediction and test data dimensions
- Debugging train/test preprocessing pipelines

These debugging steps helped me understand the complete machine learning workflow beyond simply calling `fit()`.

## 📂 Project Structure

```text
medical_insurance_predictor/
│── insurance.csv
│── Medical_Insurance_Predictor.ipynb
└── README.md
```

## ⚙️ How to Run

1. Clone the repository

```bash
git clone https://github.com/vinayak932/medical_insurance_predictor.git
cd medical_insurance_predictor
```

2. Install dependencies

```bash
pip install pandas numpy scikit-learn matplotlib
```

3. Open the notebook and run all cells.

## 📚 What I Learned

This project strengthened my understanding of:

- Multiple Linear Regression
- Polynomial Regression
- One-Hot Encoding
- Train/Test Splitting
- Model Evaluation
- Overfitting and model complexity

## 🔮 Future Improvements

- Add Actual vs Predicted visualization
- Residual analysis
- Compare with Decision Tree and Random Forest Regression
- Experiment with feature engineering and regularization

---

## 👨‍💻 Author

**Vinayak Dubey**

- GitHub: https://github.com/vinayak932
- Repository: https://github.com/vinayak932/medical_insurance_predictor
