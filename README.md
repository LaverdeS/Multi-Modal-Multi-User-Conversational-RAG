# Multi-Modal-Multi-User-Conversational-RAG
Unstructured.io, LangChain, Redis. Multi-modal and Multi-user RAG system for QA on rich PDFs.

![](https://i.imgur.com/wcCDT38.gif)

### RAG-Based Question Answering System for AI Research Papers

The notebook [Multimodal_Multi-User_RAG_System.ipynb](Multimodal_Multi-User_RAG_System.ipynb) contains an implementation of a a **Multimodal, Multi-User Retrieval-Augmented Generation (RAG)** system to support **Question Answering (QA)** on a small collection of AI research papers. Users can interact with the system using **text or uploaded documents/images**, and get **accurate, source-grounded answers** with citations to the original research content.

---

### 📌 Key Features

#### 1. 👥 Multi-User Support
- Session-based interaction with isolated memory per user.
- Scalable backend to handle multiple concurrent users.

#### 2. 🧠 Multimodal Input Support
- Accepts text, PDFs, and images (e.g., charts, figures) as input.
- Uses OCR (for images) and document parsers (PDF/text extractors) to ingest content.

#### 3. 🔍 Intelligent Retrieval
- Chunking and vectorization of multimodal data.
- Embedding-based semantic search via vector DBs (Chroma, FAISS).
- Custom retrievers per user session to ensure relevant context.

#### 4. 🤖 Answer Generation
- Uses LLMs to generate detailed, well-structured responses.
- Combines retrieved context with the user query for grounded output.

#### 5. 📚 Source Attribution
- Each answer includes citations or links to document chunks or image regions.
- Supports PDF page numbers, section headings, or bounding boxes for visual content.

---

### 🎯 Example Use Cases

- A researcher uploads 3–4 AI papers and asks domain-specific questions.
- A student uploads a lecture slide image and queries a related paper.
- Multiple users interact with the system simultaneously in a shared environment (e.g., lab, classroom).

---

### 🧪 Sample Questions to Test the System

1. What are the main components of a RAG model, and how do they interact?
2. What are the two sub-layers in each encoder layer of the Transformer model?
3. Explain how positional encoding is implemented in Transformers and why it is necessary.
4. Describe the concept of multi-head attention in the Transformer architecture. Why is it beneficial?
5. What is few-shot learning, and how does GPT-3 implement it during inference?

---

### 🛠️ Tech Stack

- Python
- LangChain
- OpenAI GPT4o
- Unstructured for rich PDF extraction (text, images, tables)
- Redis/PostgreSQL for user session management

---

### 🚀 Running the Project

1. Clone the repo.
2. Set up environment:
   ```bash
   python -m venv .venv
   source .venv/bin/activate
   pip install -r requirements.txt
    ```
3.  Install unstructured[pdf] dependencies (follow official install instructions for [poppler](https://pdf2image.readthedocs.io/en/latest/installation.html) and [tesseract](https://tesseract-ocr.github.io/tessdoc/Installation.html)):

   ```bash
   # For Ubuntu/Debian
   sudo apt install tesseract-ocr
   sudo apt install poppler-utils
   ```
   
4. Follow the instructions in the notebook: [Multimodal_Multi-User_RAG_System.ipynb](Multimodal_Multi-User_RAG_System.ipynb)