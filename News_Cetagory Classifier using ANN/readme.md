# 20 Newsgroups Text Classification Using Artificial Neural Network (ANN)

## Project Overview

This project implements a text classification model on the **20 Newsgroups** dataset — a popular benchmark dataset containing approximately 20,000 newsgroup posts evenly distributed across 20 different categories. The goal is to classify newsgroup posts into their correct category based on the content of the text.

## Dataset

- The dataset is loaded from `scikit-learn`'s built-in `fetch_20newsgroups` function.
- Headers, footers, and quotes were removed from the text to focus on the main content.
- The dataset includes posts across 20 different categories such as `sci.space`, `rec.sport.baseball`, `comp.graphics`, and more.

## Approach

- **Text preprocessing**:  
  Text data was converted into numerical features using **TF-IDF vectorization**, limiting the vocabulary size to 20,000 and removing English stopwords for better quality features.
  
- **Model architecture**:  
  A simple fully connected **Artificial Neural Network (ANN)** with the following layers:
  - Input layer matching the size of TF-IDF features
  - Two dense layers with ReLU activation and dropout regularization
  - Output layer with softmax activation to classify into 20 categories
  
- **Training**:  
  - The model was compiled with the Adam optimizer and sparse categorical cross-entropy loss.
  - Trained for 10 epochs with batch size 32.
  
- **Performance**:  
  The trained ANN achieved an accuracy of approximately **72%** on the test set, demonstrating decent performance for a simple feedforward network on TF-IDF features.

## How to Use

1. Clone the repository.
2. Install required libraries: TensorFlow, scikit-learn, pandas.
3. Run the notebook to train the model or load the pre-trained model saved in Google Drive.
4. Use the vectorizer and model to classify new text samples.

## Future Improvements

- Experiment with advanced text embeddings like Word2Vec, GloVe, or transformers (BERT).
- Increase model complexity or use convolutional/recurrent architectures.
- Perform hyperparameter tuning and early stopping for better generalization.
- Improve text preprocessing and data augmentation techniques.

## Acknowledgments

- Dataset courtesy of scikit-learn.
- TensorFlow and Keras for deep learning framework.

