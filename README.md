# RAG From Zero

![LangChain](https://img.shields.io/badge/LangChain-0.1-blue?logo=chainlink)
![ChromaDB](https://img.shields.io/badge/ChromaDB-0.4-orange)
![Groq](https://img.shields.io/badge/Groq-LLaMA3-purple)
![HuggingFace](https://img.shields.io/badge/HuggingFace-SentenceTransformers-yellow?logo=huggingface)
![LlamaParse](https://img.shields.io/badge/LlamaParse-PDF%20Parsing-red)
![Python](https://img.shields.io/badge/Python-3.10+-green?logo=python)
![Colab](https://img.shields.io/badge/Google%20Colab-Notebook-orange?logo=googlecolab)

Learning Retrieval-Augmented Generation by building every component
from scratch — no shortcuts, no copy-paste.

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

### `PDFs are Hard LlamaParse Isn't.ipynb`
Rebuilt the chain specifically for PDFs using LlamaParse:
- `LlamaParse` for clean, structured PDF parsing
- Handles multi-column layouts, tables, and citations properly
- Converts LlamaIndex documents to LangChain format
- `RecursiveCharacterTextSplitter` for chunking clean markdown
- `Chroma` vector store with `HuggingFaceEmbeddings`
- Tested on a real NLP research paper (PsyDef Dataset Paper)
- Learned why table reasoning is hard for small LLMs

---

## Stack

| Component | Tool |
|-----------|------|
| Embeddings | `all-MiniLM-L6-v2` via SentenceTransformers |
| Vector DB | ChromaDB |
| LLM | LLaMA 3 via Groq |
| Framework | LangChain |
| PDF Loader | LlamaParse |
| Web Loader | LangChain WebBaseLoader |
| Environment | Google Colab |

---

## What I Learned
- Embeddings capture **meaning**, not just keywords — semantically 
  similar sentences produce similar vectors even with different words
- Chunking strategy directly affects retrieval quality — too small 
  loses context, too large loses precision
- Cosine similarity is the math powering semantic search under the hood
- LangChain abstracts every component I built manually — knowing 
  the internals makes debugging infinitely easier
- Prompt engineering significantly affects answer quality — 
  telling the LLM *how* to reason matters as much as giving it context
- PDFs are a display format, not a text format — they're designed 
  to look good, not to be machine-readable. Basic parsers get confused 
  by tables, multi-column layouts and figures because they read 
  left-to-right across everything. LlamaParse uses an LLM to 
  understand layout before extracting, which is why it works so much better

---

## Status
🔨 Work in progress — adding notebooks as I learn
