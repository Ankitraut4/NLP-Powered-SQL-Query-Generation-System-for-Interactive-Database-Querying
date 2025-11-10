# 🧠 NLP Powered SQL Query Generation System for Interactive Database Querying

A **Gradio-powered chatbot** that transforms natural language questions into SQL queries — enabling users to explore and analyze their uploaded CSV data interactively.

---

## 📄 Project Summary
**NLP-SQL Transformer** is an intelligent question-answering system that lets users upload one or more CSV files and ask data-related questions in plain English (e.g., “How many users are over 25?”).  
Powered by a **fine-tuned BART Transformer model**, it dynamically generates and executes SQL queries on the uploaded data, returning both the generated query and the result.

<h2 align="center">🚀 Live Demo</h2>

<p align="center">
  <a href="https://huggingface.co/spaces/Rushikesh-S-Ware/NLP-SQL-Transformer">
    ➡️ <b>Live Demo on Hugging Face Spaces</b>
  </a>
</p>

<p align="center">
  <a href="https://huggingface.co/spaces/Rushikesh-S-Ware/NLP-SQL-Transformer">
    <img src="https://img.shields.io/badge/🤗%20Hugging%20Face-Spaces-blue" alt="Hugging Face Spaces">
  </a>
</p>


---

## 🚀 Features
- 📂 Upload one or more CSV files  
- 🧠 Ask natural language questions  
- 🧾 Automatically generates executable SQL queries  
- 📊 Returns tabular results  
- 🧩 Handles fuzzy matching, `LIKE` queries, and ambiguous schemas  
- ⚡ Optimized inference with sub-200 ms response times  

---

## 🗂️ Project Structure

| File/Folder | Description |
|--------------|-------------|
| `app.py` | Main application logic for Gradio interface and model inference |
| `Model_Training.ipynb` | Notebook for fine-tuning and evaluating the Transformer model |
| `Demo_Notebook.ipynb` | Demonstration notebook with usage examples |
| `Project_Overview.txt` | Project notes and experiment logs |
| `Model_Checkpoint.zip` | Fine-tuned BART model weights and configs |
| `requirements.txt` | Python dependencies for deployment |

---

## 🧠 How It Works
1. **Upload CSV Files** → Loaded into an in-memory SQLite database.  
2. **Ask a Question** → The system constructs a schema-aware prompt for the model.  
3. **Generate SQL** → The fine-tuned BART model predicts the SQL query.  
4. **Post-process Query** → Regex and fuzzy logic corrections are applied if needed.  
5. **Display Results** → Executes the SQL and shows the result in a data table.

---

## 💻 Installation (Local)

```bash
git clone https://github.com/Ankitraut4/NLP-Powered-SQL-Query-Generation-System-for-Interactive-Database-Querying.git
cd NLP-Powered-SQL-Query-Generation-System-for-Interactive-Database-Querying
pip install -r requirements.txt
python app.py
