# Challenge Objectives
The goals of this challenge are:

Import, analyze, clean, and preprocess a “real-world” classification dataset.
Select, design, and train a binary classification model of your choosing.
Optimize model training and input data to achieve desired model performance.

# Resources
Data Source: charity_data.csv

Software: Jupyter Notebook, Python

# Summary
Using our knowledge of machine learning and neural network model building, we created a binary classifier that is capable of predicting whether or not an applicant will be successful if funded by Alphabet Soup using the features collected in the provided dataset.

# Pre-processing the data
1. I decided to drop the EIN column and use Name as the identifier
2. Name and Classification Data were binned to reduce noise
3. All categorical values were encoded

# Choosing the model
As the objective was to predict if the organization will be successful, target y is "IS_SUCCESSFUL" column.

After splitting and scaling the dataset, the training dataset has 80 columns and over 34299 rows, so my first model had two layers to handle the larger amount of data, with a smaller number of nodes (10 and 8 respectively).

Even though the first model already achieved an accuracy of 75.50% accuracy, I tried to see if the performance can be further optimzed.

Original:                                                          accuracy score: 75.50%
Optimization 1:	Binning "ASK_AMT"	                                 accuracy score: 75.34%
Optimization 2:	Increase neurons in 1st layer to 20	               accuracy score: 75.64%
Optimization 3:	Increase neurons in 2nd layer to 12	               accuracy score: 75.07%
Optimization 4:	Change activation to Leaky Relu	                   accuracy score: 75.18%

The best optimized performance was binning the Ask_Amt with increased neurons in the first layer.

# Implement a different model
As an alternative, I would use Random Forest Classifier. The original dataset was already in a tabular format, and is large enough to handle data being split into subset data for training. It is able to train and predict such a large data set in a more efficient manner.

In comparision, I would choose the Random Forest Classifier. The accuracy score is 75.40%, and more efficient.
