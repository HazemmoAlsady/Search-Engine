# Multilingual Ranked Search Engine (TXT & PDF)

This project implements a **mini search engine** based on core
**Information Retrieval (IR)** concepts.  
The system supports **file-based document ingestion**, **ranked retrieval**, 
and works with **both Arabic and English documents**.

The search engine is implemented using **Python** and executed on **Google Colab**.

---

## 📚 Concepts Covered

This project applies concepts from the Information Retrieval course:

- **Lecture 3** – Tokenization, Stopwords, Lemmatization
- **Lecture 4** – Dictionary and Indexing Concepts
- **Lecture 5** – Ranked Retrieval, TF-IDF, Vector Space Model

---

## ⚙️ Features

- Supports **TXT and PDF documents**
- Accepts **multiple files with any filename**
- Works with **Arabic and English text**
- Text preprocessing:
  - Tokenization
  - Stopword removal
  - Lemmatization (English)
  - Normalization (Arabic)
- TF (Term Frequency) computation
- IDF (Inverse Document Frequency) computation
- TF-IDF vector representation
- Ranked retrieval using **Cosine Similarity**
- Interactive, web-like search interface

---

## 🛠️ Technologies Used

- Python
- NLTK
- PyPDF2
- Google Colab

---

## 📥 Input

### Document Collection
- Users can upload **TXT and/or PDF files**
- Each line (TXT) or paragraph (PDF) is treated as a separate document

Example TXT file:
