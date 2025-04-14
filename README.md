# TwitBERT-NER 🧠📲  
**BERT-based Named Entity Recognition for Twitter Data**

TwitBERT-NER is a deep learning project focused on identifying and classifying named entities (e.g., persons, organizations, locations, products) within tweets using transformer-based models. It leverages the power of BERT and BERTweet to overcome the noise, abbreviations, and informal syntax typical of social media content.

---

## 🚀 Objective

To develop a robust NER system that accurately detects entities from tweets without relying on user-provided hashtags—enabling improved trend analysis, targeted advertising, content recommendation, and user behavior insights.

---

## 🔍 Features

- ✅ Fine-tuned `bert-base-uncased` and `BERTweet` models on Twitter-specific data
- ✅ CoNLL-formatted BIO tagging (B-XXX, I-XXX, O)
- ✅ Support for multiple entity types: Person, Organization, Location, Product, Facility, Movie, TV Show, and more
- ✅ Early stopping, dropout regularization, and hyperparameter tuning
- ✅ Token-label alignment with support for subword tokenization
- ✅ Evaluation using precision, recall, and F1-score
- ✅ Trained model saving and inference on custom tweet inputs

---

## 📁 Dataset

- Format: **CoNLL BIO Tagging Scheme**
- Source: Public Twitter datasets / Tweebank-NER  
- Each token is tagged with its entity type or marked as non-entity (O)

**Example**:  
Harry B-PER
Potter I-PER
lives O
in O
London B-geo-loc

## 🧪 Model Architecture

### LSTM + CRF (Baseline)
- Word2Vec Embeddings  
- BiLSTM for context  
- CRF for sequence-level predictions

### Transformer-based (Final Model)
- `bert-base-uncased` and `BERTweet` models from Hugging Face  
- Fine-tuning for NER task with token classification head  
- Tokenizer and subword alignment handled via Transformers API

---

## 🛠️ Tech Stack

- Python 3.8+  
- Hugging Face Transformers  
- TensorFlow / PyTorch  
- Simple Transformers  
- NumPy, Pandas, scikit-learn  
- Jupyter Notebooks for experimentation

---

## 📊 Results

Achieved high F1-scores in identifying noisy social media entities across multiple classes. Fine-tuned BERT models showed significant improvement over traditional LSTM-based methods.

# Applications
- Real-time trend detection

- Social media listening & brand monitoring

- Personalized content recommendation

- Context-aware advertising
