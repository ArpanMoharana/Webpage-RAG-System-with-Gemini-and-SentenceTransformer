# PDF-RAG-Chatbot-with-Gemini-and-FAISS

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)
![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Environment](https://img.shields.io/badge/Environment-Google%20Colab-orange.svg)
![Embeddings](https://img.shields.io/badge/Embeddings-HuggingFace-yellow.svg)
![VectorDB](https://img.shields.io/badge/VectorDB-FAISS-blue.svg)
![LLM](https://img.shields.io/badge/LLM-Gemini-blueviolet.svg)

## 📌 Project Summary

This repository contains an end-to-end **Retrieval-Augmented Generation (RAG)** system built entirely within a **Google Colab notebook**. It is designed to "chat" with a PDF document by:

-   **Loading** a PDF document from a URL.
-   **Splitting** the text into manageable chunks.
-   **Embedding** those chunks using a **free, local Hugging Face model** (to avoid API rate limits).
-   **Storing** the resulting vectors in **FAISS**, a high-speed, in-memory vector database.
-   **Answering** user questions using **Google's Gemini model** as the "brain," with its answers based *only* on the context retrieved from the document.

This project is fully reproducible, secure (using `getpass` for API keys), and demonstrates the complete 5-step RAG pipeline.

---

## 🚀 Tech Stack

-   **Environment:** Google Colab
-   **Language:** Python
-   **Core AI Framework:** LangChain
-   **LLM (The "Brain"):** Google Gemini (via `langchain-google-genai`)
-   **Embeddings (Local):** Hugging Face Sentence Transformers (via `langchain-community`)
-   **Vector Database:** FAISS (via `faiss-cpu`)
-   **Document Loader:** `PyPDFLoader` (via `pypdf`)

---

## 🏁 Quickstart

The easiest way to run this project is directly in Google Colab.

1.  **Open in Colab:**
    Click the "Open in Colab" badge below. This will open a clean, fresh copy of the notebook from this repository.

    [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR-USERNAME/YOUR-REPO/blob/main/PDF_RAG_Chatbot.ipynb)

    *(**Important:** You must replace `YOUR-USERNAME/YOUR-REPO` in the link above with your actual GitHub username and repository name. Also, make sure your notebook file is named `PDF_RAG_Chatbot.ipynb`.)*

2.  **Set Your API Key:**
    The notebook uses `getpass` to securely ask for your Google AI API key. Your key is **never** saved in the notebook or its outputs.
    * Get your free key from [Google AI Studio](https://aistudio.google.com/app/apikey).

3.  **Run the Cells:**
    Run the notebook cells from top to bottom. The notebook will:
    * Install all required libraries.
    * Ask for your API key.
    * Download the sample PDF.
    * Build the entire RAG pipeline.
    * Provide a final cell for you to ask your questions!

---

#Sample Output


--

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
The Google AI API key is loaded securely using Python's getpass module. This prevents the key from ever being saved in the notebook, printed in an output cell, or stored in the project's version history.
---
## 📜 License
This project is licensed under the MIT License. See the LICENSE file for details.

