# 📑 PDF Text Extraction Benchmark

This project compares multiple Python libraries and tools for extracting text from a **PDF with over 500 pages**.  
The goal is to evaluate **which tool provides the maximum information** while balancing **speed and accuracy** for both **unscanned (text-based) PDFs** and **scanned (image-based) PDFs**.

---

## 📂 Data
- One Scanned PDF: `scanned_484.pdf` (484 pages)  
- One Unscanned PDF: `unscanned_360.pdf` (360 pages)

---

## ⚙️ Extraction Methods Tested

### 1. PyPDF2
- 📄 **Unscanned PDF**
  - Text Length: `1,220,915`
  - Time Taken: `20.6s`
- 🖼️ **Scanned PDF**
  - Text Length: `0`
  - Time Taken: `0.3s`

---

### 2. pdfplumber
- 📄 **Unscanned PDF**
  - Text Length: `1,217,863`
  - Time Taken: `1m 11.4s`
- 🖼️ **Scanned PDF**
  - Text Length: `0`
  - Time Taken: `0.6s`

---

### 3. pdfminer.six
- 📄 **Unscanned PDF**
  - Text Length: `1,311,791`
  - Time Taken: `30.9s`
- 🖼️ **Scanned PDF**
  - Text Length: `484`
  - Time Taken: `0.7s`

---

### 4. PyMuPDF + pytesseract (Hybrid OCR)
- 📄 **Unscanned PDF**
  - Text Length: `1,235,582`
  - Time Taken: `1.5s`
- 🖼️ **Scanned PDF**
  - Text Length: `1,219,432`
  - Time Taken: `26m 42.4s`

---

### 5. Unstructured (by Unstructured.io)
- 📄 **Unscanned PDF**
  - Text Length: `1,216,833`
  - Time Taken: `3m 18.4s`
- 🖼️ **Scanned PDF**
  - Text Length: `1,224,325`
  - Time Taken: `112m 37.4s`

---

## 📊 Summary Table

| Tool / Library             | Unscanned PDF (Text Length) | Time Taken  | Scanned PDF (Text Length) | Time Taken   |
|-----------------------------|-----------------------------|--------------|----------------------------|--------------|
| **PyPDF2**                  | 1,220,915                  | 20.6s        | 0                          | 0.3s         |
| **pdfplumber**              | 1,217,863                  | 1m 11.4s     | 0                          | 0.6s         |
| **pdfminer.six**            | 1,311,791                  | 30.9s        | 484                        | 0.7s         |
| **PyMuPDF + pytesseract**   | 1,235,582                  | 1.5s         | 1,219,432                        | 26m 42.4s          |
| **Unstructured.io**         | 1,216,833                  | 3m 18.4s     | 1,224,325                  | 112m 37.4s   |

---

# Chunking Stratergy

Different options
Character text splitting (Fixed length characters)
