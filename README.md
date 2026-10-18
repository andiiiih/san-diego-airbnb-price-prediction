# San Diego Airbnb Price Prediction

## Project Description
This project uses machine learning to predict Airbnb prices in San Diego.

The goal is to predict the nightly price of an Airbnb listing based on features like location, room type, bedrooms, bathrooms, beds, reviews, availability, and host information.

This is a regression project because the target variable is price.

---

## Files
- airbnb_san_diego.ipynb
- listings.csv
- README.md

---

## Requirements
Make sure Python is installed.

Install the needed libraries:

- pip install numpy pandas matplotlib scikit-learn notebook

---

## Dataset

The dataset used in this project comes from [Inside Airbnb](https://insideairbnb.com/get-the-data/), specifically the detailed listings dataset for San Diego, California.

- **Source:** Inside Airbnb
- **Location:** San Diego, California
- **Original file:** `listings.csv.gz`
- **Extracted file:** `listings.csv`
- **Prediction target:** Airbnb listing price

We selected the detailed listings dataset because it contains information about property characteristics, location, room type, availability, reviews, and pricing.

Rather than combining multiple datasets, we focused on selecting the most relevant features from the detailed listings data. We removed unnecessary columns and cleaned the remaining data before training our machine learning models.

### Download Instructions

1. Visit [Inside Airbnb – Get the Data](https://insideairbnb.com/get-the-data/).
2. Find San Diego, California.
3. Download the detailed listings file (`listings.csv.gz`).
4. Extract the file and save it as `listings.csv`.
5. Place `listings.csv` in the same folder as `airbnb_san_diego.ipynb`.

**Note:** Inside Airbnb updates its datasets periodically, so results may differ when using a newer version of the data.

---

## How to Run
1. Open the project folder in VS Code.
2. Make sure the notebook and CSV file are in the same folder.
3. Install the required libraries.
4. Open:

- airbnb_san_diego.ipynb

5. Run the notebook cells from top to bottom or click the run all button.



---

## What the Code Does
The notebook:
- loads the Airbnb dataset
- cleans the price and bathroom columns
- converts true/false columns into numbers
- removes missing values
- removes extreme prices above $1000
- creates graphs
- prepares the data for machine learning
- trains regression models
- compares model results

---

## Models Used
The project uses three models:

1. Linear Regression
2. Decision Tree Regressor
3. Random Forest Regressor

---

## Results
The Random Forest model performed the best.

| Model | Test MAE | Test RMSE | Test R² |
|---|---:|---:|---:|
| Random Forest | 55.65 | 93.21 | 0.6745 |
| Linear Regression | 62.27 | 102.76 | 0.6043 |
| Decision Tree | 65.13 | 103.36 | 0.5997 |

Random Forest had the lowest error and the highest R², so it made the most accurate price predictions.

The results also showed that bedrooms, bathrooms, location, room type, and neighborhood-related features were important for predicting Airbnb prices.

---

## Output
When the notebook is run, it creates:
- price distribution graph
- log price distribution graph
- average price by room type graph
- correlation heatmap
- Linear Regression coefficient graph
- actual vs predicted price graph
- Decision Tree graph
- Random Forest feature importance graph
- model comparison table
- model comparison graph

---

## Contributors
- Cole Tamashiro
- Andy Huang
