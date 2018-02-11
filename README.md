# Deep Learning Sentiment Classifier, RNN-LSTM
Predict the sentiment, positive or negative, of a movie review using a deep learning classifier. The sentiment classification task is accomplished using a recurrent neural network (RNN) with long short term memory (LSTM) architecture.
* Python, NLTK, Keras, Tensorflow, Numpy
## Overview
A deep learning sentiment classifier is developed using RNN-LSTM in order to classify moview reviews as positive or negative. The classifier is trained using the IMDB moview review dataset which contains 25,000 movie reviews with labled sentiment. This project was created using Python, and Keras running the Tensorflow backend.

## Preprocessing
In order to use Keras, the inputs must be the same length and we can achieve this by padding or truncating the inputs. The padding involves placing zeros into shorter sequences in order to lengthen them. The truncating achieves the opposite, and shortens reviews which are longer. For this project we padded and truncated reviews to achieve a move review length of 500 sequences.

## Model Details
An embedded layer is created with vector lengths for each word defined as 35. The long short term memmory layer is then created with 100 memory units specified. Finally, since we are developing a binary classifier, the output layer is created with a single neuron using the sigmoid function to make predictions of 0 or 1. We also specify a few other parameters which control the loss function, optimization algorithm, and performance metric we'd like to use. In this case we use the log loss function, the ADAM optimization algorithm, and accuracy as our performance metric.

## Training and Validation
We specify the parameters needed to fit our model, and perform validation by supplying as inputs: our training and validation data, specifying a cutoff limit for the number of passes over the entire dataset (called an epoch), and specifying a batch size to control the number of samples used per gradient update.

## Performance Metrics
The performance metric used for this example is the classification accuracy. This simple recurrent neural network with long short term memory is able to guess whether or not a review is positive almost 9 out of 10 times.
