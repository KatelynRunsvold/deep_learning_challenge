# deep_learning_challenge
Charity Fund Classification Model

Overview

This project aims to build a binary classification model to predict whether charity donations will be successful. Using a dataset of past donation applications, the model leverages features such as application type, classification, use case, organization, and more to forecast the success of future charity donations.

The model is built using a deep learning neural network (TensorFlow/Keras) and employs techniques like data preprocessing, categorical encoding, scaling, and model evaluation.

Dataset

The dataset used in this project contains information about charity donation applications with the following key columns:

APPLICATION_TYPE: The type of application submitted.
CLASSIFICATION: The category of the application.
USE_CASE: The purpose for which the funds are requested.
ORGANIZATION: Type of organization applying for funds.
STATUS: Current status of the application.
INCOME_AMT: The income bracket of the organization.
ASK_AMT: Amount requested by the organization.
IS_SUCCESSFUL: The target column (1 = Successful, 0 = Unsuccessful).
Project Structure
Data Preprocessing:

Dropped non-beneficial columns (EIN, NAME).
Replaced low-frequency values in categorical columns (APPLICATION_TYPE, CLASSIFICATION) with "Other".
Applied one-hot encoding to convert categorical variables into numerical format.
Scaled the feature data using StandardScaler to normalize the values.
Model Building:

Created a neural network model with TensorFlow/Keras, using two hidden layers.
The model uses relu activation for hidden layers and sigmoid for the output layer to handle binary classification.
The model is compiled using binary_crossentropy loss function and the adam optimizer.
Model Training & Evaluation:

The data was split into training (80%) and testing (20%) sets.
The model was trained for 100 epochs and evaluated using accuracy and loss metrics.
Plots for training and validation accuracy/loss were generated to help monitor overfitting.
Saving the Model:

The trained model is saved as an HDF5 file (AlphabetSoupCharity.h5).
