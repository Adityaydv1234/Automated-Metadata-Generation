
---

```markdown
# ✨ MetaGen: Automated Metadata Generator

MetaGen is a smart, lightweight AI-powered system that extracts and generates semantically rich metadata from unstructured documents. It supports a wide range of formats such as **PDF**, **DOCX**, and **TXT**, combining front-end simplicity with back-end intelligence using NLP, OCR, and semantic analysis.

> 🔒 All processing can run entirely in your browser — ensuring complete privacy.  
> 🧠 For advanced semantic processing, a backend option using Python and NLP tools is also included.

---

## 🌐 Project Overview

The goal of MetaGen is to enhance **document discoverability**, **classification**, and **analysis** by producing **structured metadata** automatically. The metadata includes key statistics, summaries, semantic sections, and named entities.

### 🔍 Key Features
- 📄 Upload and process **PDF**, **DOCX**, and **TXT** files
- 🧠 Extract text using **PDF.js**, **Mammoth**, and **EasyOCR**
- 🧾 Generate metadata including:
  - Filename, word/character count, reading time
  - Language detection
  - Key sentence extraction
  - Named Entity Recognition (NER)
- 🎨 Beautiful UI with in-browser drag-and-drop functionality
- 🧪 Python backend using `spaCy`, `sentence-transformers`, `langdetect`, `PyMuPDF`, and `easyocr` for deeper NLP-based processing (optional)

---

## 🛠️ Tech Stack

| Frontend | Backend (Optional) |
|----------|--------------------|
| HTML, CSS, JavaScript | Python 3.10+ |
| PDF.js, Mammoth.js | `spaCy`, `easyocr`, `langdetect`, `PyMuPDF` |
| In-browser file processing | `sentence-transformers`, `nltk`, `Pillow` |

---

## 📦 Folder Structure

```

├── automated\_metagenerator.html   # Frontend web app
├── generate.py / MetaGen.ipynb    # Python backend for richer metadata
├── assets/                        # Fonts, icons (if any)
├── README.md                      # This file

````

---

## 🚀 How to Use

### 🔸 1. Use In-Browser Web App (No Installation Needed)
1. Open `automated_metagenerator.html` in your browser.
2. Drag and drop a `.pdf`, `.docx`, or `.txt` file into the upload zone.
3. Wait for in-browser analysis (no server or backend required).
4. Download the metadata report.

> ✅ All processing stays in-browser — perfect for lightweight, private usage.

---

### 🔸 2. Use Python Backend for Rich NLP Metadata (Colab Recommended)

#### ⚙️ Step-by-Step (Google Colab or local Python)
1. Install required dependencies:

```bash
pip install easyocr python-docx langdetect PyMuPDF sentence-transformers spacy nltk
python -m spacy download en_core_web_sm
````

2. Save your file (e.g. `sample.pdf`) to a known path or Google Drive.

3. Run the backend code:

```python
from generate import generate_metadata
print(generate_metadata("path/to/your/document.pdf"))
```

> 📌 **NOTE:** PDF OCR is automatically triggered if no text is extractable via PyMuPDF.

---

## 🧪 Sample Output

```txt
Filename: sample.pdf
Extracted on: 2025-06-25 14:12:02 IST
Document length: 4829 characters
Word count: 739
Approx. Reading Time: 4 min
Paragraphs: 32
Detected Language: EN
Dominant Entity Type: ORG

=== Summary Sections ===
1. This report outlines the impact of globalization on labor relations across sectors...
2. Key stakeholders involved include multinational corporations, labor unions...
3. The findings suggest a significant policy gap in labor regulation enforcement...

=== Named Entities ===
ORG: World Bank, Infosys, UNCTAD
PERSON: Roluahpuia, Aaditya Singhvi
DATE: 2025-05-21, 2025-06-01
GPE: India, Germany, Singapore
```

---

## 🎥 Demo Video

▶️ **[Watch the Demo (2 mins)](https://drive.google.com/open?id=1gBW7eg2eqeGFcxZe8Y3AhhbDrbUtZUJ3&usp=drive_copy)**
*Shows file upload, metadata generation, and download functionality*

---

## ✅ Deliverables

| Component                           | Status        |
| ----------------------------------- | ------------- |
| ✅ Web App HTML Interface            | ✔️ Complete   |
| ✅ Jupyter Notebook or `generate.py` | ✔️ Included   |
| ✅ README File                       | ✔️ This file  |
| ✅ 2-min Demo Video                  | 📎 Link Above |

---

## 📌 Reproducibility Notes

If using Colab:

* Mount Google Drive:

```python
from google.colab import drive  
drive.mount('/content/drive')  
```

* Set path to your uploaded file:

```python
pdf_path = '/content/drive/My Drive/sample.pdf'  
print(generate_metadata(pdf_path))
```

---


