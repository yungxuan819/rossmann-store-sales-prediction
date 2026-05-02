# 🛒 Rossmann Store Sales Prediction

A machine learning project that predicts retail store sales using a **Random Forest model** with an interactive **Power BI dashboard** for business insights and visualization.

---

## 📌 Project Overview

Rossmann is a European drug store chain operating over 3,000 stores across 7 countries. This project aims to forecast store sales based on historical data and store-specific factors such as promotions, competition distance, store type, and holidays.

The project covers the full data science pipeline:
- Data cleaning & preprocessing
- Exploratory Data Analysis (EDA)
- Feature engineering
- Machine learning model building
- Interactive dashboard with embedded ML predictions

---

## 📊 Dashboard Preview

> Screenshots of the Power BI dashboard

![Dashboard Overview](screenshots/dashboard_overview.png)

---

## 🔍 Key Features

- ✅ Sales prediction using **Random Forest Regressor (91% Accuracy)**
- ✅ **ML model embedded in Power BI** — predictions generated live inside the dashboard
- ✅ Interactive slicers for **Store, Date, DayOfWeek, Promo**
- ✅ Visualizations:
  - Predicted Sales Table (Store + Date + Predicted Sales)
  - Competition Distance vs Predicted Sales (Scatter Plot)
  - Total Predicted Sales by StoreType (Bar Chart)
  - Predicted Sales Trend Over Time (Line Chart)
  - Promo vs No Promo Sales Comparison (Column Chart)

---

## 🛠️ Technologies Used

| Tool | Purpose |
|------|---------|
| Python | Data cleaning, EDA, model building |
| Pandas | Data manipulation |
| Scikit-learn | Random Forest model |
| Matplotlib & Seaborn | Data visualization |
| Power BI | Interactive dashboard |
| Git & GitHub | Version control |

---

## 📁 Project Structure

```
rossmann-store-sales/
├── script.ipynb                              # Main notebook (cleaning, EDA, modelling)
├── rossmann_sales_prediction_dashboard.pbix  # Power BI dashboard file
├── df_test_normalized.csv                    # Cleaned & normalized test dataset
├── df_test_raw_result.csv                    # Raw test dataset with predictions
├── train.csv                                 # Original training dataset
├── test.csv                                  # Original test dataset
├── store.csv                                 # Store information dataset
├── screenshots/                              # Dashboard screenshots
└── README.md
```

---

## 📂 Dataset

The dataset is sourced from the [Rossmann Store Sales Kaggle Competition](https://www.kaggle.com/competitions/rossmann-store-sales).

| File | Description |
|------|-------------|
| `train.csv` | Historical sales data for training |
| `test.csv` | Store data for prediction |
| `store.csv` | Supplemental store information |

---

## 🤖 Model Performance

| Metric | Score |
|--------|-------|
| **Accuracy** | 91% |
| **Model** | Random Forest Regressor |
| **Validation** | 80/20 Train-Validation Split |

---

## ⚙️ How to Reproduce the Model

1. Clone this repository:
```bash
git clone https://github.com/yungxuan819/rossman-store-sales-prediction.git
```

2. Install required libraries:
```bash
pip install pandas scikit-learn matplotlib seaborn numpy
```

3. Open and run the notebook:
```bash
jupyter notebook script.ipynb
```

4. The notebook will retrain the model and save `sales_model.pkl` locally

5. Open `rossmann_sales_prediction_dashboard.pbix` in **Power BI Desktop** and update the pkl file path in the Python visual script

---

## 📝 Notes

- `train.csv` is **37MB**, therefore cannot be uploaded - users are advised to download them through the official Kaggle link
- `sales_model.pkl` is **326MB** — if it cannot be opened from GitHub, download it directly and place it in the project folder
- Power BI Desktop (free) is required to open the `.pbix` file — download at [powerbi.microsoft.com](https://powerbi.microsoft.com)
- Python must be enabled in Power BI Desktop under **File → Options → Python Scripting**
