# NLP-project-Emotion-Classification
## Team Member: 
- Bhavana Ramesh

## Project Overview
This project explores **emotion classification from tweet texts** using different Natural Language Processing (NLP) models studied during the course.  
The goal is to understand how model complexity and representation choices impact performance on a real-world text classification task.

The emotions include categories such as *joy, sadness, anger, fear*, and related emotional states.

---

## Dataset
The dataset consists of short tweet texts labeled with their dominant emotion.  
It is divided into:
- a **training set** for model learning,
- a **test set** for model comparison,
- and a **validation set**, used only at the end to verify generalization and avoid overfitting.

All preprocessing and experiments were designed to prevent any form of data leakage.

---

## Models Implemented
Several models were implemented progressively, following the structure of the course:

1. **Fully Connected Neural Network (TF-IDF based)**  
   This model serves as a baseline and relies on TF-IDF representations.  
   While simple and efficient, it ignores word order and long-range dependencies.  
   *(Course 2)*

2. **Recurrent Neural Networks (LSTM and BiLSTM)**  
   These models process text as sequences, allowing them to capture contextual and temporal information.  
   The Bidirectional LSTM further improves performance by considering both past and future context.  
   *(Course 3)*

3. **Fine-tuned Transformer Model**  
   A pretrained Transformer model was fine-tuned on the dataset.  
   Thanks to self-attention and large-scale pretraining, this model captures rich semantic and contextual information.  
   *(Course 4)*

---

## Project Structure
NLP/
├── dataset/
├── models/
├── notebooks/
│ ├── 1_preprocessing.ipynb
│ ├── 2_fc_baseline.ipynb
│ ├── 3_lstm_model.ipynb
│ ├── 4_bilstm_model.ipynb
│ ├── 5_transformer_model.ipynb
│ └── 6_model_comparison.ipynb


Each notebook corresponds to a clear step in the experimentation process.

---

## Evaluation
All models are evaluated on the **test dataset** using:
- Accuracy
- Weighted F1-score

The final comparison and detailed analysis of the results are presented in **Notebook 6**.

Hyperparameters for all models were selected using the validation set.
The test set was used only once for final model comparison to ensure an unbiased evaluation.

---

## Key Observations
- The TF-IDF baseline provides a strong starting point but lacks contextual understanding.
- LSTM-based models significantly improve performance by modeling word order.
- The Transformer model achieves the best results due to its attention mechanism and pretrained language knowledge.

---

## Conclusion
This project highlights the importance of choosing appropriate text representations and models for NLP tasks.  
While simpler models remain useful in constrained settings, pretrained Transformer models offer the best performance for emotion classification when computational resources allow.

Overall, the project demonstrates a clear progression from basic representations to modern deep learning approaches in NLP.