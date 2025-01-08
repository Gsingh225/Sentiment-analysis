# Hybrid CNN-GRU with Multi-Head Attention for Sentiment Analysis

This repository contains a PyTorch implementation of a hybrid model combining **CNN**, **GRU**, and **Multi-Head Attention** for sentiment analysis. The model is designed to classify text into three sentiment categories: **positive**, **negative**, and **neutral**.

## Model Architecture
The model consists of the following layers:
1. **Embedding Layer**: Converts input text into dense word embeddings.
2. **CNN Layer**: Extracts local features from the embeddings.
3. **GRU Layer**: Captures sequential dependencies in the text.
4. **Multi-Head Attention**: Focuses on important parts of the sequence.
5. **Fully Connected Layer**: Produces the final classification output.

## Dataset
The model was trained on a small dataset with roughly the following distribution:
- **Positive**: 1,100 samples
- **Negative**: 1,000 samples
- **Neutral**: 1,400 samples

Due to the small size and slight class imbalance, the model may underperform on more complex or nuanced text. This architecture was chosen over a simple approaches to see how a unique approach to sentiment analysis would preform. It is constrained by the dataset size but still works. 

## Performance
The model achieved the following validation metrics:
- **Validation Loss**: 0.8852
- **Validation Accuracy**: 0.6811

While the model works and outperforms a random baseline, it is **underperforming** due to the limited dataset size and complexity. With a larger and more balanced dataset, the performance could be significantly improved.

## Training
The model was trained for 5 epochs with the following results:
- **Epoch 1 Training Loss**: 1.1941
- **Epoch 2 Training Loss**: 0.7642
- **Epoch 3 Training Loss**: 0.5999
- **Epoch 4 Training Loss**: 0.4903
- **Epoch 5 Training Loss**: 0.9831

The spike in training loss at the last epoch suggests potential overfitting or instability during training.

## Usage
To use the model for sentiment analysis:
Simply download the notebook, run it to train the model (takes about 2 mins on a free colab gpu) and navigate to the last cell to use. Feel free to modify the code or use a custom dataset.
