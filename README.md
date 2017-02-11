# Week 2:

## Mini-project: build a neural network for sentiment analysis on movie review data

### Steps:
- Convert movie reviews into word vectors

	- Use Collections : Counter class to count word frequency

		- Only keep 10,000 most frequent words in corpus

	- Create a look-up table of 10,000 most frequent words

	- Create input layer to neural network for each review

		- Initialize layer to zeros; length = 10,000 words

		- For every word in review, look-up the index for that word, and increment the input layer at that index by one

		- Repeat input layer method for each review

- Create 90 - 10 train - test splits (TFLearn will create validation set later)

	- Create a 'shuffled' list of review indices (25,000 reviews or indices) using 'np.random.shuffle'

	- Take the first 90% of the shuffled indices

		- Select the word vectors corresponding to those indices and set them as the training set 

		- Select the review labels corresponding to those indices and set them as the training labels

	- Take the remaining 10% of the shuffled indices 

		- Select the word vectors corresponding to those indices and set them as the test set

		- Select the review leabels corresponding to those indices and set them as the test labels

- Use TFLearn, a high-level library built on top of TensorFlow, to build the neural network

	- Define an input layer

	- Define hidden layer(s)

	- Define the output layer

	- Initialize the model

	- Train the model

		- Adjust hyperparameters (num of hidden units, learning rate, num of epochs)

		- Refer to validation accuracy

	- Test model accuracy and make predictions with new reviews 