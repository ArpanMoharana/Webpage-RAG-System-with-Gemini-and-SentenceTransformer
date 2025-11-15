# Webpage-RAG-System-with-Gemini-and-SentenceTransformer

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Environment](https://img.shields.io/badge/Environment-Google%20Colab%20%2F%20Jupyter-orange.svg)
![Embeddings](https://img.shields.io/badge/Embeddings-SentenceTransformers-yellow.svg)
![VectorDB](https://img.shields.io/badge/VectorDB-ChromaDB-blue.svg)
![LLM](https://img.shields.io/badge/LLM-Gemini%202.5%20Flash-blueviolet.svg)

## 📌 Project Summary

This repository contains an end-to-end **Retrieval-Augmented Generation (RAG)** system built in a Jupyter/Colab notebook.  
The system takes a **webpage URL**, processes the content, and allows you to **chat with that webpage** using Google’s **Gemini 2.5 Flash**.

The pipeline performs:

- **Loading** webpage content via `WebBaseLoader`
- **Splitting** the text into chunks using `RecursiveCharacterTextSplitter`
- **Embedding** the chunks using a **local HuggingFace SentenceTransformer** model (`all-MiniLM-L6-v2`)
- **Storing** embeddings in **ChromaDB**, a local persistent vector store
- **Retrieving** the top relevant chunks using semantic search
- **Answering** questions using **Gemini 2.5 Flash**, grounded strictly in the retrieved text

This project avoids API embedding limits completely by using **local embeddings**.

---

## 🚀 Tech Stack

- **Environment:** Google Colab / Jupyter Notebook  
- **Language:** Python  
- **Core Framework:** LangChain  
- **LLM:** Google Gemini 2.5 Flash (`langchain-google-genai`)  
- **Embeddings:** Sentence Transformers (`all-MiniLM-L6-v2`)  
- **Vector Database:** ChromaDB (`chromadb`)  
- **Document Loader:** `WebBaseLoader` from LangChain community  
- **Text Splitter:** `RecursiveCharacterTextSplitter`  

---

## 🏁 Quickstart

### 1️⃣ Set Up the Notebook  
Run this project directly in Google Colab or Jupyter.

### 2️⃣ Install Required Libraries  
The notebook installs all dependencies automatically.

### 3️⃣ Set Your Gemini API Key
```python
import getpass, os
os.environ["GOOGLE_API_KEY"] = getpass.getpass("Enter your Gemini API key: ")
```

---

## 📸Sample Output

**1 — Webpage Loaded Successfully**
![Webpage Loaded](https://raw.githubusercontent.com/ArpanMoharana/Webpage-RAG-System-with-Gemini-and-SentenceTransformer/c8a9c6560695ca198a2978dd5f01bb5fa7ddf01d/Random%20Webpage%20Loaded.png)
<br>
<br>
**2 — Chatbot(gemini) Answers Using RAG**
![AI System Doc View](https://raw.githubusercontent.com/ArpanMoharana/Webpage-RAG-System-with-Gemini-and-SentenceTransformer/c8a9c6560695ca198a2978dd5f01bb5fa7ddf01d/Doc%20viewed%20by%20AI%20system.png)

---

## 📦 Key Packages Used

This project uses the following core libraries:

- **langchain** — Framework for building LLM-powered pipelines  
- **langchain-community** — Community loaders, retrievers, and integrations  
- **langchain-google-genai** — Gemini 2.5 Flash integration for LLM reasoning  
- **google-generativeai** — Native Google Gemini API Python client  
- **sentence-transformers** — Local embedding model (`all-MiniLM-L6-v2`)  
- **chromadb** — Local persistent vector database for fast similarity search  
- **langchain-text-splitters** — Text chunking utilities for RAG preprocessing  
- **jupyterlab** — Interactive notebook environment for development
  
  ---
  
## 🔒 Security
  
The Google AI API key is loaded securely using Python's getpass module. This prevents the key from ever being saved in the notebook,
printed in an output cell, or stored in the project's version history.

---

## 📜 License

This project is licensed under the MIT License. See the LICENSE file for details.

