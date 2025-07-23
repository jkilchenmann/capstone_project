# Predicting Airline Flight Times - Overview of Project

This project involves the creation of a machine learning model to determine whether it is possible to accurately predict flight times.  The model predicts flight times using the independent variables of departure airport, destination airport, time of day, aircraft type, and distance.  From these independent variables, the model predicts the dependent variable of flight length (or flight "duration").

## Details of Project

The model was trained using a dataset of 1,127 flights the author personally completed during the period from June 15, 2004 to June 10, 2025.  The original dataset is contained in Log.csv.

The original dataset was cleaned to remove excess information that did not factor into the analysis.  That dataset is contained in log_cleaned.csv.

The dataset was reviwed to determine basic statistical information, such as the most common departure airports and how many unique destinations each of those airports had.  This can be viewed in review_of_data.ipynb.

The cleaned dataset was trained and tested using RandomForestRegressor to determine the mean absolute error and R² values.  Initial testing showed that the Mean Absolute Error was 5.66 minutes and the R² Score was 0.96.  Showing that the model was able to reliably predict flight lengths with only a small amount of error.  This can be seen in training_and_testing.ipynb.

An additional listing of 20 flights was generated for flights occurring on July 15, 2025.  The model was used to predict the flight times.  Half of the flights involved airport pairings (e.g. ORD-MSP) that were in the trained dataset.  The other half involved pairings (e.g. AUS-MSY) that were not in the trained dataset.  Mean absolute error and R² values were calculated for the listing as a whole and for the first and second set of 10 flights.  While the errors were slightly worse than the original dataset, the R² values were slightly better.  This can be seen in predict_with_new_data.ipynb.

### To work with the dataset in a virtual environment:

## Instructions for Using Code

Establishing a Virtual Environment

```shell
python -m venv venv
```

Activating the Virtual Environment
```shell
venv\Scripts\activate
```

Installing Dependencies
```shell
pip install -r requirements.txt
```

Use Jupyter Notebook to view the code and results.