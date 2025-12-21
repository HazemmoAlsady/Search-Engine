# 🔍 Smart Document Search Engine

A clean, modular TF-IDF based search engine with Arabic and English support.

## 📁 Project Structure

```
Search-Engine/
├── app.py                  # Flask application (entry point)
├── config.py              # Configuration & constants
├── preprocessing.py       # Text preprocessing (Arabic & English)
├── document_loader.py     # PDF document loading
├── search_engine.py       # TF-IDF & cosine similarity
├── sample_documents.py    # Default sample documents
├── templates/
│   └── index.html        # HTML template
├── static/
│   └── style.css         # CSS styling
├── pdfs/                 # Place your PDF files here
└── README.md             # This file
```

## 🎯 Single Responsibility Principle

Each module has a single, well-defined responsibility:

### `config.py`
- **Responsibility**: Configuration and constants
- **Contains**: Stopwords, Flask settings, search parameters

### `preprocessing.py`
- **Responsibility**: Text preprocessing
- **Contains**: Arabic normalization, tokenization, stopword removal, lemmatization

### `document_loader.py`
- **Responsibility**: Document loading
- **Contains**: PDF reading, folder scanning

### `search_engine.py`
- **Responsibility**: Search logic
- **Contains**: TF-IDF calculation, cosine similarity, ranking

### `sample_documents.py`
- **Responsibility**: Sample data
- **Contains**: Default documents for testing

### `app.py`
- **Responsibility**: Web application
- **Contains**: Flask routes, initialization

## 🚀 Quick Start

### 1. Install Dependencies
```bash
pip install flask nltk PyPDF2
```

### 2. Add Your PDFs
Create a `pdfs` folder and add your PDF files:
```bash
mkdir pdfs
# Copy your PDF files to the pdfs folder
```

### 3. Run the Application
```bash
python app.py
```

### 4. Open Browser
Navigate to: `http://127.0.0.1:5000`

## ⚙️ Configuration

Edit `config.py` to customize:

```python
# Flask settings
FLASK_HOST = "127.0.0.1"
FLASK_PORT = 5000
FLASK_DEBUG = True

# Search settings
TOP_K_RESULTS = 10
MAX_TEXT_DISPLAY_LENGTH = 250

# PDF settings
PDF_FOLDER = "pdfs"
MIN_PARAGRAPH_LENGTH = 20
```

## 📚 How It Works

### 1. **Document Loading** (`document_loader.py`)
- Scans the `pdfs` folder
- Extracts text from all PDF files
- Splits into paragraphs

### 2. **Preprocessing** (`preprocessing.py`)
- Normalizes Arabic text
- Removes stopwords (Arabic & English)
- Lemmatizes English words
- Tokenizes text

### 3. **Indexing** (`search_engine.py`)
- Builds TF (Term Frequency) for each document
- Computes IDF (Inverse Document Frequency)
- Creates TF-IDF vectors

### 4. **Search** (`search_engine.py`)
- Preprocesses query
- Creates query TF-IDF vector
- Computes cosine similarity with all documents
- Returns top-k ranked results

### 5. **Web Interface** (`app.py`)
- Displays search form
- Shows ranked results
- Handles user requests

## 🎨 Features

- ✅ **Bilingual**: Supports Arabic and English
- ✅ **TF-IDF Ranking**: Advanced relevance scoring
- ✅ **Cosine Similarity**: Accurate similarity measurement
- ✅ **PDF Support**: Load multiple PDF files
- ✅ **Clean Design**: Google-style minimal UI
- ✅ **Modular Code**: Single Responsibility Principle
- ✅ **No JavaScript**: Pure server-side rendering

## 🔧 Extending the System

### Add New Stopwords
Edit `config.py`:
```python
ARABIC_STOPWORDS.add("كلمة_جديدة")
```

### Change Number of Results
Edit `config.py`:
```python
TOP_K_RESULTS = 20  # Show 20 results instead of 10
```

### Add Custom Preprocessing
Edit `preprocessing.py` and modify the `preprocess()` function.

### Use Different Document Sources
Edit `app.py` and modify `initialize_search_engine()`.

## 📊 Code Quality

- **Modular**: Each file has a single responsibility
- **Documented**: All functions have docstrings
- **Type Hints**: Function parameters and returns are typed
- **Error Handling**: Graceful handling of missing files
- **Clean Code**: Following PEP 8 standards

## 🐛 Troubleshooting

### No PDFs found
- Make sure the `pdfs` folder exists
- Check that PDF files are in the folder
- The app will use sample documents as fallback

### NLTK errors
- The app automatically downloads required NLTK data
- If issues persist, manually run:
  ```python
  import nltk
  nltk.download('stopwords')
  nltk.download('wordnet')
  ```

### PDF reading errors
- Ensure PDFs are not encrypted
- Check PDF file permissions
- Try with different PDF files

## 📝 License

Open-source for educational purposes.

## 👨‍💻 Technical Stack

- **Backend**: Flask (Python)
- **NLP**: NLTK
- **PDF**: PyPDF2
- **Frontend**: HTML5, CSS3
- **Design**: Google-style minimalism

---

Made with ❤️ using Flask & TF-IDF
