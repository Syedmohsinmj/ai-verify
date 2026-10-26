AI VERIFY expanded demonstration prototype

WHAT IT DEMONSTRATES
- PDF, DOCX, XLSX/XLSM, CSV and text extraction.
- Image OCR when Tesseract is installed and configured.
- Video evidence intake as a manual-review item only (no video analysis).
- Document classification by reviewer, field correction, required-document checks,
  cross-document comparisons, synthetic-record comparisons and report export.
- Infrastructure evidence checklist and reviewer-entered source verification log.
- Reviewer decisions and a local SQLite audit trail.

IMPORTANT LIMITS
- This is a student/demo prototype, not an AICTE-approved system.
- The bundled institution records are fictional; they are not live AICTE data.
- No AICTE or issuing-authority API, portal, QR validation service or signature
  verification service is connected. The source-check form only records what a
  human reviewer says they checked.
- Photos, floor plans, certificates and videos are not automatically assessed for
  engineering or regulatory compliance. A person must review them. Video analysis
  and computer vision are not implemented.
- Rules are illustrative. Confirm all requirements against current authorized
  AICTE handbooks and instructions before operational use.
- Do not upload confidential or personal documents to this prototype. Uploaded
  files are processed by the local Streamlit session and are not securely stored
  as an institutional case-management system.

RUN
1. Put app.py, compliance_rules.json, demo_institution_records.json and
   requirements.txt in the same folder.
2. In that folder, install dependencies with: py -m pip install -r requirements.txt
3. Start with: py -m streamlit run app.py
4. Use synthetic or anonymized sample files.

IMAGE OCR NOTE
Pytesseract also requires the Tesseract OCR application installed locally.
If it is missing, images remain available for human review and the app explains
that OCR was unavailable. PDF OCR also depends on the local Tesseract installation.