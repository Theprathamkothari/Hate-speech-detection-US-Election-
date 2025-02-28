# Hate Speech Classification using Deep Learning  

## 📖 Project Overview  
This project focuses on classifying hate speech in text data related to US elections using deep learning models. The models evaluated include **LSTM, GRU, BERT, and DistilBERT**, and their performance is compared based on accuracy, precision, recall, and F1-score.  

## 🚀 Features  
- **Data Preprocessing Pipeline:** Tokenization, noise removal, and formatting for training.  
- **Multiple Model Implementations:** LSTM, GRU, BERT, and DistilBERT.  
- **Training and Optimization:** Hyperparameter tuning, dropout regularization, and learning rate scheduling.  
- **Experiment Tracking:** Model performance metrics logged for analysis.  
- **Deployment-Ready:** Trained models can be exported for real-world applications.  

## 🗂️ Dataset Details  
- **Source:** Textual data related to the US elections.  
- **Labels:** Binary classification – Positive (1) and Negative (0).  
- **Preprocessing Steps:**  
  - Text cleaning and tokenization  
  - Stopword removal  
  - Word embeddings (e.g., Word2Vec, GloVe, BERT embeddings)  

## 🔧 Model Implementations  

| Model       | Framework | Validation Accuracy | Precision | Recall | F1-score |
|------------|-----------|---------------------|-----------|--------|----------|
| **LSTM**    | TensorFlow | 75.00%              | 0.64      | 0.60   | 0.60     |
| **GRU**     | TensorFlow | 75.00%              | 0.62      | 0.58   | 0.56     |
| **BERT**    | PyTorch    | 78.00%              | 0.76      | 0.77   | 0.76     |
| **DistilBERT** | PyTorch | 82.53%              | 0.83      | 0.82   | 0.82     |

## 🛠️ Model Training & Optimization  
- **LSTM & GRU (TensorFlow)**  
  - Embedding layer with pre-trained word vectors  
  - Bidirectional layers for better context learning  
  - Dropout and Batch Normalization  
  - Adam optimizer with learning rate decay  

- **BERT & DistilBERT (PyTorch)**  
  - Hugging Face `transformers` library  
  - Fine-tuning with custom classification head  
  - Learning rate tuning with **linear warm-up**  
  - Mixed-precision training with `torch.cuda.amp`  

## 📊 Experiment Tracking  
- Results logged using **TensorBoard** for visualization.  
- Model checkpoints saved for reproducibility.  
- Hyperparameter tuning logs included.  

## 🏆 Results & Findings  
- Transformer-based models (BERT & DistilBERT) outperform LSTM/GRU.  
- **DistilBERT** provides the best accuracy (82.53%) with fewer parameters.  
- Using **pre-trained embeddings** significantly improves model performance.  

## 📁 Repository Structure  
├── dataset/ # Processed dataset files ├── models/ # Trained models saved ├── src/ │ ├── preprocess.py # Data cleaning and preprocessing │ ├── train_lstm.py # LSTM model training │ ├── train_gru.py # GRU model training │ ├── train_bert.py # BERT model fine-tuning │ ├── train_distilbert.py # DistilBERT fine-tuning │ ├── evaluate.py # Model evaluation script ├── notebooks/ # Jupyter notebooks for experiment tracking ├── results/ # Logs and metrics ├── README.md # Project documentation

## 📌 How to Run  

### 1️⃣ Install Dependencies  
```bash
pip install -r requirements.txt
python src/preprocess.py
python src/train_lstm.py
python src/train_distilbert.py
python src/evaluate.py --model distilbert
🎯 Future Work
Extend dataset with multilingual hate speech detection.
Deploy model as an API using FastAPI or Flask.
Implement model distillation for efficient mobile deployment.
🔗 Contributions to Open Source
We welcome contributions! You can:

Improve model training scripts.
Add more evaluation metrics.
Experiment with other architectures (e.g., RoBERTa, T5).
