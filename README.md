Data Loading and Splitting:

The code uses the Pandas library to load a dataset from a CSV file named 'Creditcard_data.csv'.
The dataset is assumed to have a 'Class' column representing the target variable (1 for fraud, 0 for non-fraud).
The data is split into features (X) and the target variable (y), and then further divided into training and testing sets using train_test_split.
Class Balancing:

To address class imbalance (assuming fraud instances are relatively rare), the code employs resampling techniques.
Instances with the 'fraud' class (y_train == 1) are oversampled using the resample function from scikit-learn. The number of samples is set to match the number of 'non-fraud' instances.
Model Definition:

Five machine learning models are defined: two Random Forest classifiers (M1 and M4), two Logistic Regression models (M2 and M5), and a Support Vector Machine (M3).
Sampling Techniques:

Different sampling techniques are defined using lambda functions (Sampling1 to Sampling5), each resampling the data with a different percentage of the original data.
Model Training and Evaluation:

The code then iterates over each model and each sampling technique.
For each combination, it applies the specified sampling technique to the balanced training data, trains the model, makes predictions on the test set, and calculates the accuracy using scikit-learn's accuracy_score.
Results Display:

The accuracy results for each model and sampling technique are stored in a dictionary (results) and then printed. The output shows the accuracy for each combination of model and sampling technique.
