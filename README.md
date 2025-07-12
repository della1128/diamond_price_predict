
# 💎 Diamond Price Predictor

This machine learning project predicts the price of a diamond based on its physical characteristics and quality ratings. It is implemented in Python using the Scikit-learn library and visualized with Plotly. The project was developed and tested in Google Colab.

---

## 📌 Table of Contents
- [Overview](#overview)
- [Features Used](#features-used)
- [Model and Evaluation](#model-and-evaluation)
- [Dataset](#dataset)
- [How to Run](#how-to-run)
- [Results](#results)
- [Files in This Repo](#files-in-this-repo)
- [Future Improvements](#future-improvements)

---

## 📖 Overview

Diamonds vary in price depending on their **carat, cut, clarity, color, and physical size**. This project builds a regression model that learns the relationship between those attributes and the price.

We use:
- Data preprocessing
- Feature engineering (volume calculation)
- Data visualization (scatter plots, trendlines)
- Model performance evaluation using MAE, MSE, and R²

---

## 📊 Features Used

The model uses the following features to predict diamond price:
- `carat`: Weight of the diamond
- `cut`: Categorical (encoded to numeric)
- `color`: Categorical (encoded)
- `clarity`: Categorical (encoded)
- `depth`, `table`: Measurements of the diamond
- `size`: Computed as volume = length × width × depth

---

## 🧠 Model and Evaluation

The base model used is **RandomForestRegressor**. You can optionally switch to   `GradientBoostingRegressor` for improved performance.

**Evaluation Metrics (Linear Regression):**
- ✅ Mean Absolute Error (MAE): ₹791.81
- ✅ Mean Squared Error (MSE): ₹2,025,502.46
- ✅ R² Score: 0.8746 (Model explains 87.5% of the variation in price)

---

## 📁 Dataset

The dataset `diamonds.csv` was sourced from [Kaggle](https://www.kaggle.com/datasets/shivam2503/diamonds) 

It contains over 50,000 rows and includes the following columns:
- Carat, Cut, Color, Clarity
- Depth, Table
- Dimensions (x, y, z)
- Price (target)

---

## ⚙️ How to Run

### Option 1: Google Colab
Open the notebook in Google Colab:
```

diamond_price_predictor.ipynb

````

Run the cells from top to bottom. You can also try live prediction by entering:
- Carat
- Size
- Cut type (mapped to integer)

### Option 2: Local Setup

1. Clone the repository:
```bash
git clone https://github.com/della1128/diamond-price-predictor.git
cd diamond-price-predictor
````

2. Install requirements:

```bash
pip install -r requirements.txt
```

3. Run the notebook:

```bash
jupyter notebook diamond_price_predictor.ipynb
```

---

## 📈 Results

A sample prediction:

```
Input:
- Carat: 0.23
- Size: 38
- Cut (Ideal = 1): 1

Predicted Price: ₹387  
Actual Price: ₹327  
Error: ₹60 (18.3% overestimate)
```

---

## 📦 Files in This Repo

| File                            | Description                    |
| ------------------------------- | ------------------------------ |
| `diamond_price_predictor.ipynb` | Main notebook with full code   |
| `diamonds.csv`                  | Dataset used for training      |
| `requirements.txt`              | Python packages list           |
| `README.md`                     | Project documentation          |

---

## 🔮 Future Improvements

* Try advanced models like XGBoost or CatBoost
* Build a Streamlit web app for interactive prediction
* Perform hyperparameter tuning
* Add boxplots and heatmaps for deeper data insights
* Deploy with Flask or FastAPI

---

## 👩‍💻 Author

Della Cherian
Electronics & Communication Engineering graduate, aspiring Data Analyst and AI Engineer.

---

## 🌟 Acknowledgments

* Kaggle for dataset
* Scikit-learn & Plotly for tools
* Google Colab for easy experimentation

---

## 📌 License

This project is open-source under the [MIT License](LICENSE).


