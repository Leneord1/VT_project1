# VT Project 1 — RAG Pipeline

PDF chunking, Azure OpenAI embeddings, FAISS retrieval.

## Layout

```
data/pdfs/           # place 2-3 PDFs here
data/faiss_index/    # optional saved FAISS index
notebooks/           # rag_pipeline.ipynb
report/              # project report
requirements.txt
.env                 # local secrets (gitignored)
.env.example         # template for keys
```

## Setup

1. Create venv and install deps:
   ```
   python -m venv .venv
   .venv\Scripts\activate
   pip install -r requirements.txt
   ```
2. Copy keys into `.env` (see `.env.example`).
3. Drop 2-3 PDFs into `data/pdfs/`.
4. Run `notebooks/rag_pipeline.ipynb`.

## Env vars

| Variable | Purpose |
| --- | --- |
| `AZURE_OPENAI_API_KEY` | Azure key |
| `AZURE_OPENAI_ENDPOINT` | Azure endpoint URL |
| `AZURE_OPENAI_API_VERSION` | API version |
| `AZURE_OPENAI_EMBEDDING_DEPLOYMENT` | Embedding deployment name |
| `AZURE_OPENAI_CHAT_DEPLOYMENT` | Chat/GPT deployment name |
| `OPENAI_API_KEY` | Optional OpenAI platform key |
