# titanic-day1-eda
# Titanic Dataset – Data Cleaning, EDA and Feature Engineering

## Project Overview

This project analyzes the Titanic passenger dataset. The main goal is to clean the data, explore important patterns, create visualizations, and engineer new features that may help build a machine learning model in the future.

## Dataset

The dataset contains information about Titanic passengers, including:

* Passenger class
* Name
* Sex
* Age
* Number of siblings or spouses
* Number of parents or children
* Ticket information
* Fare
* Cabin
* Embarkation port
* Survival status

## Tasks Completed

### Data Cleaning

* Identified missing values
* Filled missing age values using grouped median values
* Filled missing embarkation values using the most frequent value
* Handled missing cabin information
* Checked for duplicate rows
* Checked for invalid and obvious outlier values
* Capped extreme fare values using the IQR method

### Exploratory Data Analysis

The notebook includes visualizations for:

* Missing-value percentages
* Age distribution by survival
* Survival rate by sex and passenger class
* Fare distribution by passenger class
* Correlation heatmap
* Survival rate by family size

### Feature Engineering

The following new features were created:

* `FamilySize` – total number of family members travelling together
* `IsAlone` – indicates whether the passenger travelled alone
* `Title` – extracted from the passenger’s name
* `HasCabin` – indicates whether cabin information is available
* `Deck` – extracted from the cabin number
* `FarePerPerson` – fare divided by family size
* `AgeGroup` – passenger age category
* `Fare_Capped` – fare after handling extreme values
* `LogFare` – logarithmic transformation of fare

## Key Insights

1. Female passengers had a much higher survival rate than male passengers.
2. First-class passengers had a higher survival rate than third-class passengers.
3. Passengers with cabin information had a higher survival rate.
4. Passengers travelling with family had a higher survival rate than passengers travelling alone.
5. Passengers who embarked from Cherbourg had a higher survival rate than passengers from other ports.

## Files in This Repository

* `titanic_eda_feature_engineering.ipynb` – main notebook
* `Titanic-Dataset.csv` – original dataset
* `Titanic-Cleaned-Engineered.csv` – cleaned dataset with new features
* `README.md` – project documentation
* `requirements.txt` – required Python libraries

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Google Colab
* Jupyter Notebook

## How to Run the Project

1. Open the notebook in Google Colab or Jupyter Notebook.
2. Upload `Titanic-Dataset.csv`.
3. Run all cells from top to bottom.
4. Review the cleaning results, charts, insights, and exported cleaned dataset.

## Final Validation

The final dataset was tested to confirm that:

* No missing values remain
* No duplicate rows remain
* No invalid age values remain
* All engineered features were created successfully
