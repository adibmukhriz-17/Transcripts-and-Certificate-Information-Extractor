# Transcripts-and-Certificate-Information-Extractor
A prototype tool for extracting student's name, programme, institution, CGPA and grade from varied transcript/certificate formats, with manual review flags for uncertain cases

## Dataset

Due to copyright considerations, the sample transcripts and certificates used during development are not included in this repository.
To test the project, place your own sample documents inside.
For this project, I am using 15 variations of transcripts/certificates that are downloadable online. The formats of each transcripts/certificates are also differents because universities might accept them in different formats like pdf, png or jpeg.

### Phase 1 - OCR Pipeline Development

The first stage of this project focuses on building a robust Optical Character Recognition (OCR) pipeline capable of processing university transcripts and certificates in different formats.

The pipeline currently supports:
- PDF documents (both digital and scanned)
- Image files (JPG, JPEG, and PNG)

The OCR system automatically determines the appropriate extraction method:
- Digital PDFs are processed using PyMuPDF's native text extraction.
- Scanned PDFs are converted into high-resolution images before applying Tesseract OCR.
- Image files are processed directly using Tesseract OCR.

To improve readability and maintainability, the project is organised into modular functions with detailed documentation and comments. At this stage, the system is able to extract the complete raw text from a document, providing the foundation for the next phase, where structured information such as student name, institution, programme, CGPA, and final grade will be extracted.

## Example results:
### Image file ("ASHWORTH COLLEGE.jpg")
<img width="894" height="718" alt="image" src="https://github.com/user-attachments/assets/0483b7d2-e134-4519-b2ee-6b4e52ed7164" />

### Scanned Pdf file ("Kumasi Technical University.pdf")
<img width="1086" height="742" alt="image" src="https://github.com/user-attachments/assets/46cb819c-b222-42b6-8cf4-2f54fb96ecb9" />

### Phase 2 - Cleaning Extracted Texts




