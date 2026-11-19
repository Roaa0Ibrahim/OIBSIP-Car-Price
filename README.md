# Car Price Prediction

Task from the **Oasis Infobyte Data Science Internship** (OIBSIP), June 2024.

## Question
A car's price depends on many factors: brand, age, mileage, fuel type, transmission and more. Can a model learn from past sales to predict the selling price?

## Data
`car data.csv`: **301 used cars × 9 variables**: name, year, selling price, present (showroom) price, kilometres driven, fuel type, seller type, transmission and number of previous owners. Numerical and categorical.

## What I did
1. **Data inspection:** structure, unique values and value counts; no missing values; removed duplicate rows.
2. **Distributions and skewness:** none of the numerical features was normally distributed.
3. **Visual analysis:** pair plot, count plots and box plots of selling price against year, fuel type, seller type and transmission; correlation heatmap.
4. **Preparation:** dropped `Car_Name`, one-hot encoded the categorical features, split 70/30, and **fitted the Min-Max scaler on the training set only**, so the test set stayed unseen.
5. **Model:** linear regression.

## Result
| | Training | Test |
|---|---|---|
| R² | 0.89 | **0.71** |
| MAE | | 1.29 |
| RMSE | | 2.56 |

The gap between training and test R² shows the model fits the training data better than new data; the test score is the honest measure.

## Tools
Python · Pandas · NumPy · scikit-learn · Matplotlib · Seaborn · Jupyter

## Files
- `Car Price.ipynb`: analysis and model
- `car data.csv`: dataset

## Data source
Used-car sales data (the "Vehicle dataset from CarDekho", commonly shared on Kaggle), provided with the internship task. Prices are in lakhs of Indian rupees.

## Running it
Place `car data.csv` next to the notebook and change the `read_csv` path to `"car data.csv"`.
