﻿# Energy Consumption Prediction

This project predicts energy consumption based on the time of day and temperature using machine learning techniques. The model is trained on a dataset containing historical energy consumption data, and the prediction is based on two main features: hour of the day and temperature.

## Table of Contents

1. [Project Description](#project-description)
2. [Features](#features)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Directory Structure](#directory-structure)
6. [License](#license)

## Project Description

The goal of this project is to develop a machine learning model that predicts energy consumption based on the time of day and temperature. The model is trained on a dataset containing historical energy usage data and is stored in a pickle file for easy deployment.

The model is built using Python, Pandas, Scikit-Learn, and other related libraries. The code follows a clean structure that separates data processing, model training, and prediction logic.

## Features

- *Machine Learning Model*: A regression model trained to predict energy consumption.
- *Data Processing*: Data preprocessing to clean and prepare the dataset.
- *Model Saving*: The trained model is saved as a .pkl file for later use.
- *Energy Prediction*: The model can be used to predict energy consumption based on hourly time and temperature.

## Installation

To set up this project locally, follow these steps:

### Prerequisites

- Python 3.6+
- pip (Python package installer)

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/erenaktuerk/energy-consumption-prediction.git
   cd energy-consumption-prediction

	2.	Create and activate a virtual environment:

python -m venv energy_predict_env
source energy_predict_env/bin/activate  # On Windows, use energy_predict_env\Scripts\activate


	3.	Install the required dependencies:

pip install -r requirements.txt


	4.	Make sure that the dataset (energy_consumption.csv) is placed in the data folder.

Usage

Once the environment is set up, you can train the model and use it for predictions.

Training the Model

To train the model, run the following command:

python train_model.py

This will train the model on the dataset and save it as energy_model.pkl in the model/ directory.

Making Predictions

Once the model is trained, you can use the following code to make predictions:

import pandas as pd
from app import predict_energy_consumption

# Example input data
data = {
    'hour': [12, 14, 18],  # Example hours of the day
    'temperature': [25, 22, 19]  # Example temperatures in °C
}

# Convert the data to a DataFrame
input_data = pd.DataFrame(data)

# Predict energy consumption
predictions = predict_energy_consumption(input_data)

# Print the predictions
print(predictions)

This code imports the prediction function from the app folder, prepares input data, and outputs energy consumption predictions.

Directory Structure

Here’s a breakdown of the project’s folder structure:

energy-consumption-prediction/
│
├── app/
│   ├── _init_.py
│   ├── energy_analysis.ipynb
│   └── predict_energy.py
│
├── data/
│   └── energy_consumption.csv
│
├── model/
│   └── energy_model.pkl
│
├── train_model.py
├── requirements.txt
├── .gitignore
└── README.md

	•	app/: Contains the logic for making predictions and the Jupyter notebook for analysis.
	•	data/: Contains the dataset (energy_consumption.csv).
	•	model/: Stores the trained model (energy_model.pkl).
	•	train_model.py: Script for training the model.
	•	requirements.txt: List of dependencies required for the project.
	•	.gitignore: Git ignore file to exclude unnecessary files from version control.

License

This project is licensed under the MIT License - see the LICENSE file for details.
