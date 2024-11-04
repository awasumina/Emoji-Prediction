# Emoji Prediction

This project classifies text into emojis based on the context of the sentence. It employs a Recurrent Neural Network (RNN) and Long Short-Term Memory (LSTM) architecture for emoji prediction from text. The model uses pre-trained GloVe embeddings to represent words, and two architectures—Simple RNN and LSTM—are trained to predict the emoji category.

## Dataset

The dataset consists of two files:
- `train_emoji.csv`: Training data with sentences and corresponding emoji labels.
- `test_emoji.csv`: Test data to evaluate model performance.

Each row contains a sentence followed by an emoji label.

## Emoji Dictionary

A dictionary (`emoji_dict`) is created for reference:
```python
emoji_dict = { 
    0 : ":heart:", 
    1 : ":baseball:", 
    2 : ":smile:", 
    3 : ":disappointed:", 
    4 : ":fork_and_knife:"
}
```

Emojis are printed using the `emoji` library.

## Word Embeddings

The project uses GloVe embeddings (`glove.6B.50d.txt`), where each word is represented by a 50-dimensional vector. These embeddings provide semantic information to the model by transforming words into vectors.

## Model Architectures

### Simple RNN
A Recurrent Neural Network (RNN) architecture is used to classify emojis:
- 2 SimpleRNN layers with dropout for regularization.
- Dense layer with softmax activation for output.

### LSTM
Long Short-Term Memory (LSTM) layers can also be implemented to improve performance.

## Training

The model is trained with categorical cross-entropy loss and the Adam optimizer. Training parameters:
- `epochs = 50`
- `batch_size = 32`

## Evaluation

The model's accuracy is computed on the test set. Incorrect predictions are displayed alongside the actual emojis for analysis.

  
## Results

The trained model can predict the appropriate emoji based on the context of the sentence. Future improvements can include using LSTM architecture for better accuracy in longer sequences.     

