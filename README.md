# RAG-Based Customer Support Chatbot

A beginner-friendly RAG (Retrieval-Augmented Generation) project for answering customer questions from company PDF documents.

## Features

- Upload a company PDF
- Extract text from the PDF
- Split text into chunks
- Create embeddings
- Retrieve the most relevant chunks
- Ask an LLM to answer using only retrieved context
- Show source PDF and page numbers
- Refuse to guess when information is not available
- Simple Flask web interface

## Technology

- Python
- Flask
- Sentence Transformers
- Scikit-learn
- PyPDF
- Ollama
- HTML/CSS/JavaScript

## Setup

### 1. Create a virtual environment

Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

### 2. Install packages

```bash
pip install -r requirements.txt
```

### 3. Install Ollama

Install Ollama and download a small model:

```bash
ollama pull llama3.2:3b
```

Make sure Ollama is running.

### 4. Run the Flask application

```bash
python app.py
```

Open:

http://127.0.0.1:5000

### 5. Test

Upload a company FAQ/policy PDF and ask questions such as:

- What is the refund policy?
- What are your working hours?
- How can I contact support?
- What documents are required?

Ask something unrelated to the PDF. The chatbot should respond that it does not know based on the provided documents.

## Project Flow

PDF
→ Text Extraction
→ Chunking
→ Embeddings
→ Similarity Search
→ Relevant Context
→ LLM
→ Answer + Sources

## Resume Description

RAG-Based Customer Support Chatbot | Python, Flask, NLP, LLM

- Developed a RAG chatbot that retrieves relevant information from company PDF documents and generates grounded customer-support responses.
- Implemented PDF text extraction, chunking, semantic embeddings, similarity-based retrieval, and source/page citations.
- Added a fallback mechanism that avoids unsupported answers when information is not available in the uploaded documents.

## Interview Explanation

"I developed a RAG-based customer support chatbot using Python and Flask. The user uploads company documents such as FAQs or policies. The system extracts and chunks the text, converts the chunks into embeddings, retrieves the most relevant sections for a question, and passes those sections to an LLM. The LLM generates an answer only from the retrieved context, and the application displays the source document and page number. If the information is not available, the chatbot says it does not know instead of guessing."
