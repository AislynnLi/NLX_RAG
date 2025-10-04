# NLX\_RAG

This repository contains a Retrieval-Augmented Generation (RAG) system built with Hugging Face, SentenceTransformers, and Milvus Lite. The project implements naive and enhanced RAG pipelines, evaluates them using industry-standard metrics, and explores strategies for improving retrieval and answer generation.

-----

## Implementation Instruction

### Configuration

```yaml
embedding_model: "all-MiniLM-L6-v2"
vector_db: "milvus-lite"
top_k: 1
index_params:
  metric: "COSINE"
  nlist: 128
generation_model: "google/flan-t5-small"
```

-----

### Tool Inventory

  * **LLM & Embedding:**
      * HuggingFace Transformers (`flan-t5-small`)
      * SentenceTransformers (`all-MiniLM-L6-v2`, `distiluse-base-multilingual-cased-v1`)
  * **Vector Database:**
      * Milvus Lite
      * FAISS
  * **Evaluation:**
      * Ragas
      * HuggingFace `evaluate`
      * `tiktoken`
  * **Core Libraries:**
      * `pandas`, `numpy`, `torch`
      * `pymilvus`
      * `tqdm`, `logging`, `os`, `sys`, `re`, `time`, `random`

-----

### Technical Specifications

  * **Language:** Python 3.10+
  * **Frameworks:** HuggingFace Transformers, SentenceTransformers
  * **Evaluation Metrics:**
      * HuggingFace `evaluate`: F1 Score, Exact Match (EM)
      * RAGAs: Faithfulness, Precision, Recall, Relevancy
  * **Hardware:** CPU / GPU (Google Colab supported)
