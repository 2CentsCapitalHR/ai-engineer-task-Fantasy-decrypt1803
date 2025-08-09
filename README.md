[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/vgbm4cZ0)

# ADGM Corporate Agent – Document Intelligence Prototype

## 📌 Overview
The **ADGM Corporate Agent** is an AI-powered legal assistant that reviews, validates, and checks the completeness of legal documents for **Abu Dhabi Global Market (ADGM)** processes, such as company incorporation.

It:
- Accepts `.docx` files
- Detects document type (e.g., Articles of Association, Memorandum of Association)
- Verifies if all mandatory documents for a process are present
- Flags compliance issues ("red flags")
- Adds contextual review comments to `.docx`
- Generates a structured JSON report
- Uses **RAG** (Retrieval-Augmented Generation) with official ADGM documents for accuracy

---

## 🚀 Features
- **Multiple Document Upload**: Upload several `.docx` files at once
- **Process Detection**: Automatically infers the legal process (e.g., incorporation)
- **Checklist Verification**: Compares uploaded docs to ADGM’s official required documents
- **Red Flag Detection**:
  - Missing jurisdiction clause
  - Incorrect jurisdiction (UAE Federal Courts instead of ADGM)
  - Missing signature section
  - Ambiguous/non-binding clauses
- **Inline Comments**: Adds red italicized review notes to `.docx` files
- **Structured Output**: JSON report with issues, severities, and suggestions
- **RAG Support**: Pulls ADGM guidance text from official references

---

## 📂 Project Structure
ADGM_corporate_agent/
│
├─ app.py # Main Streamlit app
├─ requirements.txt # Python dependencies
├─ reference_files/ # Reference documents for RAG
│ ├─ Data Sources.pdf
│ └─ Task.pdf
└─ README.md # This file


---

## 🛠 Installation

1. **Clone or download** this repository into VS Code *(or create the folder manually)*

2. **Create a virtual environment**  
   Windows:
   ```bash
   python -m venv venv
   venv\Scripts\activate

Install Dependencies
pip install --upgrade pip
pip install -r requirements.txt

Running the file 
streamlit run app.py

