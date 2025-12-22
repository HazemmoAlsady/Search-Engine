# 🔍 Smart Document Search Engine

A TF-IDF based search engine with Arabic and English support. Built with Flask, NLTK, and PyPDF2.

> **Version**: 1.0.0 | **Status**: Production Ready

## 📁 Project Structure

```
Search-Engine/
├── Search_Engine_Complete.ipynb  # Complete implementation
├── templates/index.html          # Web interface
├── static/style.css              # Styling
├── pdfs/                         # Your PDF files
└── README.md
```

## 🚀 Quick Start

### 1. Install Dependencies
```bash
pip install flask nltk PyPDF2 jupyter
```

### 2. Add PDFs
```bash
mkdir pdfs
# Copy your PDF files here
```

### 3. Run Notebook
```bash
jupyter notebook Search_Engine_Complete.ipynb
```

### 4. Start Application
Run all cells in the notebook to start the Flask web app on `http://127.0.0.1:5000`

## ⚙️ Configuration

Edit the configuration cell in the notebook:

```python
FLASK_PORT = 5000                # Server port
TOP_K_RESULTS = 10               # Number of results
MAX_TEXT_DISPLAY_LENGTH = 250    # Preview text length
PDF_FOLDER = "pdfs"              # PDF directory
MIN_PARAGRAPH_LENGTH = 20        # Min text length
```

## 📚 How It Works

1. **Document Loading**: Scans PDFs folder, extracts text, splits into paragraphs
2. **Preprocessing**: Normalizes text, removes stopwords (Arabic & English), tokenizes
3. **Indexing**: Builds TF-IDF vectors for all documents
4. **Search**: Computes cosine similarity between query and documents
5. **Ranking**: Returns top-k most relevant results
6. **Display**: Shows results in web interface

**Key Formulas:**
- `TF(t,d) = count(t in d) / total_words(d)`
- `IDF(t) = log(total_docs / docs_containing(t))`
- `Cosine Similarity = (A · B) / (||A|| × ||B||)`

## ✨ Features

- ✅ Bilingual support (Arabic & English)
- ✅ TF-IDF based ranking
- ✅ Cosine similarity matching
- ✅ Multiple PDF support
- ✅ Minimalist web interface
- ✅ No JavaScript required
- ✅ Fast searching
- ✅ Easy configuration

## 🔧 Customization

Edit cells in the notebook to:
- Add custom stopwords
- Change result count
- Modify preprocessing
- Add new data sources
- Adjust similarity thresholds

## 📝 Tech Stack

- **Backend**: Flask
- **NLP**: NLTK
- **PDF**: PyPDF2
- **Frontend**: HTML5, CSS3
- **Language**: Python 3.8+
