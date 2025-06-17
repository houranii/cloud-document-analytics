# 📊 Cloud-Based Document Analytics and Classification

This project is a **cloud-ready, Jupyter-based application** for collecting, searching, sorting, and classifying a large collection of academic documents. It uses arXiv's public API to fetch abstracts and PDFs from multiple categories and applies machine learning for classification.

---

## 🔧 Features

- **📥 Document Collection**  
  Automatically collects thousands of academic abstracts and PDF links from arXiv using web scraping (no manual upload required).

- **📑 Sorting by Title**  
  All fetched documents are sorted by their extracted titles (not filenames).

- **🔍 Search with Highlighting**  
  You can search the downloaded PDFs for keywords and display highlighted matches directly in the console.

- **🧠 Classification**  
  A Random Forest classifier trained on abstract content categorizes documents into:
  - AI/ML
  - Econometrics
  - General Physics
  - Neuroscience
  - Probability

- **📈 Analytics & Statistics**  
  The notebook prints:
  - Number of documents and unique categories
  - Classification training time
  - Weighted F1 Score on test set and via 5-fold cross-validation
  - Size of all referenced PDFs (even if not downloaded)

---

## 🚀 Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/your-username/cloud-document-analytics.git
cd cloud-document-analytics```

### 2. Install dependencies

```bash
pip install -r requirements.txt```

### 3. Run notebook
```bash 
jupyter notebook cloud_document_analytics.ipynb```

All intermediate files like arxiv_dataset.csv and downloaded PDFs will be created automatically.

### 4. Output files

| File/Folder         | Description                            |
| ------------------- | -------------------------------------- |
| `arxiv_dataset.csv` | Extracted metadata from arXiv          |
| `downloaded_pdfs/`  | Folder containing downloaded PDF files |

### 5. ML notes
- Vectorizer: TF-IDF with 10,000 features
- Classifier: RandomForestClassifier with 400 estimators
- Evaluation: Weighted F1-score, Confusion Matrix, Classification Report

### 6. Cloud-Readiness
- All document operations are automated (scraping, classification, search)
- Works with any cloud-hosted Jupyter notebook environment (e.g., Colab, Azure Notebooks, Binder)
- No manual file uploads are needed
