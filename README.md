# Sequence-to-Sequence Model for Derivative Prediction

## Overview

This assessment contains two main Python scripts, `main.py` and `train.py`, which are part of a sequence-to-sequence model for predicting derivatives of mathematical functions. The model is trained to take mathematical functions as input and generate their corresponding derivatives as output.

## Approach

### `train.py`

1. **Data Preparation**: The training data is loaded from the `train.txt` file, which contains pairs of mathematical functions and their derivatives. The data is split into two lists, `train_functions` and `train_derivatives`.

2. **Text Tokenization**: The `Tokenizer` from TensorFlow is used to tokenize both the functions and derivatives. This step involves converting text data into numerical sequences.

3. **Sequence Padding**: To ensure that all sequences have the same length, padding is applied to both the function and derivative sequences. This is important for the model to process the data efficiently.

4. **Model Architecture**: The core of the model is a sequence-to-sequence architecture. The encoder and decoder components are both built using LSTM layers. The encoder processes the input function sequences, while the decoder generates derivative sequences. An attention mechanism is used to capture relevant information from the encoder's output.

5. **Custom Loss Function**: A custom loss function, `custom_loss`, is defined to train the model for sequence prediction. It calculates the loss while considering sequence lengths, as sequences may have different lengths due to padding.

6. **Training**: The model is compiled with the Adam optimizer and the custom loss function. It is trained on the preprocessed data for a specified number of epochs with a reduced batch size.

7. **Model Saving**: Once training is complete, the model is saved to a file named `derivative_model`.

### `main.py`

1. **Data Loading**: The input for inference is loaded from the `test.txt` file, which contains a list of mathematical functions.

2. **Model Loading**: The pre-trained model, `derivative_model`, is loaded, including the custom loss function.

3. **Text Tokenization**: The input functions are tokenized using the same tokenizer that was used during training.

4. **Inference**: The pre-trained model is used to predict the derivatives for the input functions. The predicted sequences are obtained as output.

5. **Scoring**: A binary scoring function is applied to compare the predicted derivatives with true derivatives. The score is calculated based on whether the predicted and true derivatives match.

6. **Result**: The average score across all input functions is computed and printed as the final result.

## Usage

### Training the Model

To train the model on your own data, create a `train.txt` file with function-derivative pairs and run the `train.py` script. The trained model and network summary will be saved to files `derivative_model` and `network.txt`, respectively.

