

# 🧠 BPSS Agentic AI System

An **AI-powered compliance analysis agent** that answers complex questions over **multi-format enterprise datasets** (PDF, DOCX, CSV, XLSX) using a **tool-augmented reasoning approach**.



## 🚀 Overview

This project simulates a **real-world enterprise screening system** where data is distributed across multiple sources.

The system:

* Understands natural language questions
* Identifies relevant data sources dynamically
* Retrieves information from multiple file formats
* Performs multi-step reasoning across documents
* Produces **accurate, auditable answers with evidence**



## 🏗️ System Architecture

![System Architecture](system_diagram.png)

### 🔄 Flow

```text
User Question
      ↓
BPSS Agent (Gemini LLM)
      ↓
Tool Selection (dynamic)
      ↓
Data Retrieval (PDF / DOCX / CSV / XLSX)
      ↓
Multi-document reasoning
      ↓
Final Answer with Sources




## 🛠️ Features

* ✅ Multi-format support (PDF, DOCX, CSV, XLSX)
* ✅ Tool-based dynamic retrieval
* ✅ Policy-driven reasoning (BPSS rules)
* ✅ Contradiction detection across sources
* ✅ Source-level citations (`[SOURCE:]`)
* ✅ Interactive + batch execution modes
![alt text](<BPSS Agentic AI system architecture.png>)


## 🔧 Tools

| Tool                       | Description                           |
| -------------------------- | ------------------------------------- |
| `read_document`            | Extracts text from PDF and DOCX files |
| `query_structured_data`    | Queries CSV/XLSX with filtering       |
| `check_document_freshness` | Validates 90-day document rule        |
| `list_files`               | Lists available dataset files         |



## 📂 Project Structure


.
├── agent.py
├── data/
│   ├── *.pdf
│   ├── *.docx
│   ├── *.csv
│   └── *.xlsx
├── system_diagram.png
├── requirements.txt
└── README.md


---

## ⚙️ Setup Instructions

### 1. Clone the repository

```bash
git clone <your-repo-url>
cd <repo-folder>
```

---

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

---

### 3. Install Pandoc (required for DOCX parsing)

**Mac:**

```bash
brew install pandoc
```

**Ubuntu:**

```bash
sudo apt install pandoc
```

**Windows:**
Download from: [https://pandoc.org/installing.html](https://pandoc.org/installing.html)

---

### 4. Set API Key

⚠️ Do NOT hardcode API keys in code.

**Linux / Mac:**

```bash
export GEMINI_API_KEY="your_api_key_here"
```

**Windows (PowerShell):**

```bash
setx GEMINI_API_KEY "your_api_key_here"
```

---

### 5. Add Dataset

Place all dataset files inside:

```
./data/
```

Supported formats:

* PDF (policies, reports)
* DOCX (notes, candidate packs)
* CSV / XLSX (structured data)

---

## ▶️ Usage

### 🔹 Interactive Mode

```bash
python agent.py
```

---

### 🔹 Ask a Single Question

```bash
python agent.py --ask "Which candidates are not ready for BPSS closure?"
```

---

### 🔹 Batch Mode (All Evaluation Questions)

```bash
python agent.py --batch
```

Output:

```
bpss_answers.md
```

---

## 💡 Example Questions

* What are the compliance issues for a candidate?
* Which records violate policies?
* Identify missing or incomplete information
* Summarize findings from multiple documents

