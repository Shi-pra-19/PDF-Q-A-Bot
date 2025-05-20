# 📄 PDF Question Answering Bot with FAISS + Sentence Transformers + FLAN-T5 🤖

Ask questions from any PDF and get smart, context-aware answers using semantic search and large language models. 

## Features

- Upload any **PDF**
- Extracts and splits the text intelligently
- Embeds chunks using **Sentence Transformers**
- Indexes using **FAISS** for fast semantic search
- Answers questions using **FLAN-T5** (`google/flan-t5-base`)

---

## How It Works

1. **Extract Text**  
   Parses your PDF using `PyMuPDF`.

2. **Chunking**  
   Splits the document into ~250-character chunks using `nltk`.

3. **Semantic Embeddings**  
   Embeds each chunk with `all-MiniLM-L6-v2` from `sentence-transformers`.

4. **FAISS Index**  
   Indexes embeddings for fast similarity-based retrieval.

5. **Answer Generation**  
   Retrieves top-k most relevant chunks and sends them to `FLAN-T5` to generate the answer.

---

##  Example Questions

- “What is the document about?”  
- “Summarize the introduction.”  
- “List key findings.”  
- “What’s the conclusion?”  

---

## Dependencies

Install all required packages:

```bash
pip install faiss-cpu sentence-transformers transformers PyMuPDF nltk
