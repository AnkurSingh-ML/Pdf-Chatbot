# 📑 PDF Text Extraction Benchmark

This project compares multiple Python libraries and tools for extracting text from a **PDF with over 500 pages**.  
The goal is to evaluate **which tool provides the maximum information** while balancing **speed and accuracy** for both **unscanned (text-based) PDFs** and **scanned (image-based) PDFs**.

---

## 📂 Data
- One Scanned PDF `scanned_484.pdf` with 484 pages and an unscanned PDF `unscanned_360` with 360 pages.
---

## ⚙️ Extraction Methods Tested

### 1. PyPDF2
- 📄 **Unscanned PDF**
  - Text Length: `1220915`
  - Time Taken: *20.6s*
- 🖼️ **Scanned PDF**
  - Text Length: `0`
  - Time Taken: *0.3*

---

### 2. pdfplumber
- 📄 **Unscanned PDF**
  - Text Length: *1217863*
  - Time Taken: *1m 11.4s*
- 🖼️ **Scanned PDF**
  - Text Length: *0*
  - Time Taken: *0.6s*

---

### 3. pdfminer.six
- 📄 **Unscanned PDF**
  - Text Length: *1311791*
  - Time Taken: *30.9s*
- 🖼️ **Scanned PDF**
  - Text Length: *484*
  - Time Taken: *0.7s*

---

### 4. PyMuPDF (fitz)
- 📄 **Unscanned PDF**
  - Text Length: *N/A*
  - Time Taken: *N/A*
- 🖼️ **Scanned PDF**
  - Text Length: *N/A*
  - Time Taken: *N/A*

---

### 5. Apache Tika
- 📄 **Unscanned PDF**
  - Text Length: *N/A*
  - Time Taken: *N/A*
- 🖼️ **Scanned PDF**
  - Text Length: *N/A*
  - Time Taken: *N/A*

---

### 6. pdf2image + pytesseract (OCR)
- 📄 **Unscanned PDF**
  - Text Length: *N/A*
  - Time Taken: *N/A*
- 🖼️ **Scanned PDF**
  - Text Length: *N/A*
  - Time Taken: *N/A*

---

### 7. PyMuPDF + pytesseract (Hybrid OCR)
- 📄 **Unscanned PDF**
  - Text Length: *N/A*
  - Time Taken: *N/A*
- 🖼️ **Scanned PDF**
  - Text Length: *N/A*
  - Time Taken: *N/A*

---

### 8. Camelot / Tabula-py (Tables)
- 📄 **Unscanned PDF**
  - Text Length: *N/A*
  - Time Taken: *N/A*
- 🖼️ **Scanned PDF**
  - Text Length: *N/A*
  - Time Taken: *N/A*

---

### 9. Unstructured (by Unstructured.io)
- 📄 **Unscanned PDF**
  - Text Length: `1,216,833`
  - Time Taken: `3m 18.4s`
- 🖼️ **Scanned PDF**
  - Text Length: `1,224,325`
  - Time Taken: `112m 37.4s`

---

### 10. Textract (AWS) / Azure Form Recognizer
- 📄 **Unscanned PDF**
  - Text Length: *N/A*
  - Time Taken: *N/A*
- 🖼️ **Scanned PDF**
  - Text Length: *N/A*
  - Time Taken: *N/A*

---

## 📊 Summary Table

| Tool / Library            | Unscanned PDF (Text Length) | Time Taken  | Scanned PDF (Text Length) | Time Taken   |
|----------------------------|-----------------------------|-------------|----------------------------|--------------|
| **PyPDF2**                 | 1,220,915                  | N/A         | 0                          | N/A          |
| **pdfplumber**             | N/A                         | N/A         | N/A                        | N/A          |
| **pdfminer.six**           | N/A                         | N/A         | N/A                        | N/A          |
| **PyMuPDF (fitz)**         | N/A                         | N/A         | N/A                        | N/A          |
| **Apache Tika**            | N/A                         | N/A         | N/A                        | N/A          |
| **pdf2image + pytesseract**| N/A                         | N/A         | N/A                        | N/A          |
| **PyMuPDF + pytesseract**  | N/A                         | N/A         | N/A                        | N/A          |
| **Camelot / Tabula-py**    | N/A                         | N/A         | N/A                        | N/A          |
| **Unstructured.io**        | 1,216,833                  | 3m 18.4s    | 1,224,325                  | 112m 37.4s   |
| **AWS Textract / Azure**   | N/A                         | N/A         | N/A                        | N/A          |

---

✅ **Next Steps:**  
- Fill missing benchmarks for each library.  
- Add qualitative notes (accuracy, formatting quality, table handling, etc.).  
- Consider GPU acceleration for OCR methods (Tesseract, AWS Textract).  

