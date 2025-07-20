# Amazon ML Challenge 2024 – OCR + BART Text Prediction

This project is part of the Amazon ML Challenge 2024, where the goal is to build a machine learning pipeline capable of extracting text from images and predicting corresponding entity values using deep learning models.

## 🔍 Project Overview

The system performs **end-to-end OCR-driven text prediction** using:

- **PaddleOCR** for image text extraction.
- **BERT** for contextual embedding generation.
- **BART (Bidirectional and Auto-Regressive Transformer)** for sequence classification and entity prediction.
- **BLEU Score and Accuracy** for evaluation.

---

## 📊 Key Components

### 1. **Image Text Extraction**
- Images are processed using `OpenCV` and `PaddleOCR` to extract English text.
- Extracted text is stored and used for downstream training.

### 2. **Text Embeddings with BERT**
- The extracted text is tokenized and passed through `bert-base-uncased` to obtain dense vector embeddings.
- These embeddings provide context-aware representations for classification.

### 3. **Entity Classification with BART**
- A BART model is fine-tuned using Hugging Face Transformers to classify and predict the target `entity_value` based on `combined_text`.

### 4. **Evaluation**
- **BLEU Score**: Used to evaluate the closeness of predicted sequences.
- **Exact Match Accuracy**: Measures how many predictions exactly match the true values.

---

## 🚀 Technologies & Libraries Used

- Python  
- PaddleOCR  
- OpenCV  
- Hugging Face Transformers (`BERT`, `BART`)  
- PyTorch  
- Pandas  
- Numpy  
- NLTK (for BLEU score)  
- Requests (for image fetching)

---

## 📈 Results

| Metric                | Value        |
|----------------------|--------------|
| Exact Match Accuracy | 64.78%       |
| Average BLEU Score   | 0.2549       |

The model demonstrated high precision in entity prediction, especially for short and clear text spans. BLEU scores varied with sequence length and complexity.

---

## 💡 Insights

- **Strengths**: PaddleOCR proved highly effective in text extraction, and the fine-tuned BART model achieved strong alignment with ground truth in many cases.
- **Challenges**: Longer sequences reduced accuracy; BLEU scores showed sensitivity to minor text variations.

---


