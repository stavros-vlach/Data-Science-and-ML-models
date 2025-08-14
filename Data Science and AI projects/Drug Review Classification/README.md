# Drug Review Classification with BioBERT

This notebook demonstrates a text classification pipeline using the Drugs.com dataset. The goal is to predict the medical condition associated with a drug based on its name.
a
The workflow includes:

1. Loading and splitting the dataset into training, validation, and test sets.  
2. Filtering for the top 6 most frequent conditions and encoding labels for classification.  
3. Tokenizing drug names using BioBERT (`dmis-lab/biobert-base-cased-v1.1`) and preparing the data for training.  
4. Fine-tuning a BioBERT-based classifier with Hugging Face `Trainer`.  
5. Evaluating model performance using accuracy, precision, recall, and F1 score.  
6. Running predictions on the test set and mapping predicted labels back to conditions.

This notebook focuses on a clean, end-to-end pipeline for sequence classification while demonstrating reproducible preprocessing, model training, evaluation, and inference.
