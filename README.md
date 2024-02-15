# Sentiment Analysis with RNN
This project implements sentiment analysis using a Long Short-Term Memory (LSTM) neural network on the IMDB movie review dataset. The goal is to classify movie reviews as either positive or negative.

## Dataset
The IMDB movie review dataset contains 25,000 preprocessed movie reviews, with each review labeled as either positive or negative. Each review is represented as a sequence of integers, where each integer corresponds to a word in the review. The dataset has already been preprocessed, and each word is encoded by an integer representing its frequency in the dataset.

## Preprocessing
- The dataset is loaded using Keras and split into training and testing sets.
- Each review is padded or truncated to a fixed length of 250 words using Keras' pad_sequences function to ensure uniform input size for the neural network.

## Model Architecture
The neural network architecture consists of:
    - An embedding layer to convert integer-encoded words into dense vectors of fixed size.
    - An LSTM layer to process the sequence data effectively and capture long-term dependencies.
    - A dense layer with a sigmoid activation function to produce the final binary classification output.

## Training
The model is compiled with binary cross-entropy loss and the RMSprop optimizer. It is then trained on the training data for 10 epochs, with a validation split of 20%.

## Evaluation
The trained model is evaluated on the test data, and the loss value and accuracy metrics are computed.

## Making Predictions
A prediction function is defined to predict the sentiment of input text. The text is first encoded using the same preprocessing steps as the training data, and then fed into the trained model for prediction.

## Credits
This project is adapted from a tutorial on sentiment analysis with LSTM neural networks.
