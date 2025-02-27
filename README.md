# Hate-speech-detection-US-Election-
# Hate Speech Classification

## Overview
This project focuses on classifying hate speech in textual data related to the US elections. We implemented and compared various deep learning models, including LSTM, GRU, BERT, and DistilBERT, to evaluate their performance in sentiment classification.

## Dataset
The dataset consists of text data labeled as either positive (1) or negative (0). It underwent preprocessing steps such as noise removal and tokenization before being used for training and evaluation.

## Models Implemented
We experimented with the following models:
- **LSTM** (Long Short-Term Memory)
- **GRU** (Gated Recurrent Unit)
- **BERT** (Bidirectional Encoder Representations from Transformers)
- **DistilBERT** (A lightweight version of BERT)

## Results
| Model       | Epochs | Validation Accuracy | Precision | Recall | F1-score |
|------------|--------|---------------------|-----------|--------|----------|
| LSTM       | 5      | 75.00%              | 0.64      | 0.60   | 0.60     |
| GRU        | 5      | 75.00%              | 0.62      | 0.58   | 0.56     |
| BERT       | 3      | 78.00%              | 0.76      | 0.77   | 0.76     |
| DistilBERT | 6      | 82.53%              | 0.83      | 0.82   | 0.82     |

Among these models, **DistilBERT** demonstrated the best performance with an accuracy of **82.53%** and balanced precision-recall scores.

## Installation
To set up the project, follow these steps:

1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/hate-speech-classification.git
   cd hate-speech-classification
   ```
2. Create a virtual environment (optional but recommended):
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows use: venv\Scripts\activate
   ```
3. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```

## Usage
Run the training script:
```sh
python train.py --model <model_name>
```
Replace `<model_name>` with `LSTM`, `GRU`, `BERT`, or `DistilBERT`.

## Contributions
Contributions are welcome! Feel free to fork the repository and submit pull requests.


