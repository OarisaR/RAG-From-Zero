# RAG From Zero 

![LangChain](https://img.shields.io/badge/LangChain-0.1-blue?logo=chainlink)
![ChromaDB](https://img.shields.io/badge/ChromaDB-0.4-orange)
![Groq](https://img.shields.io/badge/Groq-LLaMA3-purple)
![HuggingFace](https://img.shields.io/badge/HuggingFace-SentenceTransformers-yellow?logo=huggingface)
![Python](https://img.shields.io/badge/Python-3.10+-green?logo=python)
![Colab](https://img.shields.io/badge/Google%20Colab-Notebook-orange?logo=googlecolab)

Learning Retrieval-Augmented Generation by building every component 


---

## What's Inside

### `learning_rag_from_scratch.ipynb`
Built every RAG component manually without any frameworks:
- Text embeddings using `sentence-transformers`
- Manual chunking with custom functions
- Cosine similarity based retriever from scratch
- ChromaDB vector store integration
- Full RAG pipeline connected to Groq (LLaMA3)

### `rag_but_make_it_lazy.ipynb`
Rebuilt the same pipeline using LangChain:
- `RecursiveCharacterTextSplitter` for chunking
- `HuggingFaceEmbeddings` for encoding
- `Chroma` vector store
- `ChatGroq` as the LLM
- LangChain LCEL chain connecting everything
- Tested on real documents — Wikipedia pages and PDFs

---

## Stack

| Component | Tool |
|-----------|------|
| Embeddings | `all-MiniLM-L6-v2` via SentenceTransformers |
| Vector DB | ChromaDB |
| LLM | LLaMA 3 via Groq |
| Framework | LangChain |
| PDF Loader | PyPDF |
| Web Loader | LangChain WebBaseLoader |
| Environment | Google Colab |

---

## What I Learned
- How embeddings capture meaning, not just keywords
- Why chunking strategy affects retrieval quality
- How cosine similarity powers semantic search
- Why PDF parsing is harder than it looks in production
- How LangChain abstracts the same components I built manually

---

