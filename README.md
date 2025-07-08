Titanic Survival Prediction

A machine learning project that predicts passenger survival on the Titanic using Random Forest classification.
Project Overview
This project analyzes the famous Titanic dataset to build a predictive model that determines whether a passenger survived the disaster. The model uses passenger characteristics such as class, sex, age, and family relationships to make predictions.
Dataset
The project uses the classic Titanic dataset which contains information about passengers aboard the RMS Titanic. The dataset is split into:

Training data: Used to train the machine learning model
Test data: Used to generate predictions for evaluation

-Features Used

Pclass: Passenger class (1st, 2nd, 3rd)
Sex: Gender of the passenger
Age: Age of the passenger
SibSp: Number of siblings/spouses aboard
Parch: Number of parents/children aboard
Fare: Passenger fare
Embarked: Port of embarkation (S = Southampton, C = Cherbourg, Q = Queenstown)

-Data Preprocessing

The model handles missing data through several strategies:

Age: Missing values filled with median age
Embarked: Missing values filled with mode (most frequent port)
Fare: Missing values filled with median fare
Categorical encoding:

Sex: male=0, female=1
Embarked: S=0, C=1, Q=2

-Model Details

Algorithm: Random Forest Classifier
Parameters: 100 estimators, random_state=42
Features: 7 numerical features after preprocessing
Target: Binary classification (0=Did not survive, 1=Survived)

-Running the Model

Ensure you have the training data (train.csv) and test data (test.csv) in the same directory
Run the Jupyter notebook titanic.ipynb
The model will generate predictions and save them to predictions.csv

-Results

The model generates predictions for 418 test passengers and outputs them in the required format:
csvPassengerId,Survived
892,0
893,0
894,0
...

-Key Insights

Based on the Titanic dataset, survival was influenced by:

Gender: Females had higher survival rates
Passenger Class: First-class passengers had better survival chances
Age: Younger passengers, especially children, had higher survival rates
Family Size: Passengers with small families had better survival rates than those traveling alone or with large families
