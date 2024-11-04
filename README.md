# SMS Spam Classification App

This project is an interactive SMS Spam Classification app built with Gradio and Scikit-Learn. The app uses a pre-trained machine learning model to classify SMS messages as "spam" or "not spam" based on the message content. Users can enter an SMS message into the app's input textbox, and the app will display the classification result.

## Features

- **Input Textbox**: Users can enter an SMS message in the textbox labeled "SMS Message."
- **Output Textbox**: The app displays whether the SMS message is classified as "spam" or "not spam" in the "Classification Result" textbox.
- **Interactive UI**: The app provides an intuitive and interactive interface powered by Gradio for easy usage.

## Installation

To run this app, you'll need Python and a few Python libraries. You can install the required libraries with:
- pip install pandas scikit-learn gradio
## Usage

- Clone the repository and navigate to the project directory.
- Ensure your data file (`SMSSpamCollection.csv`) is in the correct format with columns for SMS messages and labels.
- Run the app:
   - python app.py
## Code Overview

The main components of the app are as follows:

- **Model Training**:
   - The `sms_classification` function loads the SMS dataset, processes the data, and trains a model using TF-IDF vectorization and `LinearSVC` for classification.
   - The trained model pipeline is saved in a variable called `text_clf` for future use.

- **Prediction Function**:
   - The `sms_prediction` function takes an SMS message as input and returns the classification result ("spam" or "not spam").
   - This function is used within the Gradio interface to provide predictions.

- **Gradio Interface**:
   - A Gradio app is created with a labeled input textbox for SMS message input and an output textbox for displaying the result.
   - The interface launches a web-based application with `.launch()`.
## Example

After starting the app, enter an SMS message in the input box, and the app will display whether it is classified as "spam" or "not spam" in the output box.

## Requirements

- Python 3.6+
- `pandas`
- `scikit-learn`
- `gradio`