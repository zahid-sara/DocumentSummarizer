
# RAG Summary System

A local, privacy-preserving document summarization pipeline that works 100% offline using open-source models.

## Features
-  Supports PDF, TXT, and Markdown files
-  Intelligent semantic chunking
-  FAISS vector search
-  BART-large-cnn summarization
-  No API calls - fully offline

## Installation

1. Create virtual environment:
```bash
python -m venv rag_env
source rag_env/bin/activate  # Linux/Mac
.\rag_env\Scripts\activate  # Windows
Install dependencies:

bash
pip install -r requirements.txt
Usage
bash
python rag_summary.py path/to/document.pdf
Example:
bash
python rag_summary.py research_paper.pdf
Configuration
Modify these parameters in rag_summary.py:

chunk_size: Adjust token limit (default: 512)

chunk_overlap: Change overlap size (default: 100)

k: Number of chunks to retrieve (default: 5)

Requirements
Python 3.8+

8GB RAM minimum (16GB recommended)

~2GB disk space for models

Supported Models
Embedding: sentence-transformers/all-MiniLM-L6-v2

Summarization: facebook/bart-large-cnn

Limitations
Best for documents <100 pages

English-focused

First run downloads models (~1.5GB)

Troubleshooting
For memory errors: Reduce chunk_size

For PDF issues: Try converting to text first

For CUDA errors: Install GPU-compatible PyTorch
