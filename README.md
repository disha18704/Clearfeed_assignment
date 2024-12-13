# ML Intern Assignment: Search System for ClearFeed Documentation

This repository contains the implementation of a search system designed to retrieve the top 5 most relevant URLs from ClearFeed documentation based on user queries. The system combines traditional and vector-based retrieval techniques for accurate and relevant search results.


## 🏗️ Project Structure

```
├── README.md                # Project documentation
├── data
│   ├── clearfeed_kb.json    # ClearFeed knowledge base in JSON format
│   └── clearfeed_qa_pairs.csv # QA pairs for evaluation
├── notebooks
│   ├── rag_pipeline.ipynb   # Hybrid RAG pipeline implementation
│   ├── vector_rag.ipynb     # Vector-based retrieval and evaluation
│   └── vector_store         # Vector store files for document retrieval
│       ├── default__vector_store.json
│       ├── docstore.json
│       ├── graph_store.json
│       ├── image__vector_store.json
│       └── index_store.json
└──  requirements.txt         # Dependencies
```


## 🚀 Key Components

### 1. Data

- **`clearfeed_kb.json`**: Contains ClearFeed documentation in Markdown format, stored as key-value pairs:
  - **Key**: Documentation URL
  - **Value**: Title and content of the URL

- **`clearfeed_qa_pairs.csv`**: Evaluation dataset with:
  - User questions
  - URLs containing the answers
  - Extracted answers

### 2. Notebooks

- **`rag_pipeline.ipynb`**: Implements a Retrieval-Augmented Generation (RAG) pipeline using hybrid search methods:
  - BM25 for term-based retrieval
  - LanceDB for vector-based retrieval

- **`vector_rag.ipynb`**: Focuses on vector-based retrieval and evaluation.

### 3. Vector Store

- Contains data structures and files necessary for vector-based document retrieval, including:
  - **`default__vector_store.json`**: Primary vector store.
  - Other files for managing document indices and metadata.


## 📝 Requirements
- **`Python 3.11.10`**


## 🚦 Getting Started

1. **Clone this repository**:

  ```bash
  git clone https://github.com/disha18704/Clearfeed_assignment
  cd notebooks
  ```

2. **Install dependencies**:

  ```bash
  pip install -r requirements.txt
  ```

3. **Set up environment variables**:

  - Copy the provided .env.template file:
    ```bash
    cp .env.template .env
    ```
  
   - Open the .env file and replace the placeholder values with your actual configuration:
     ```
     hf_api_key=your_hugging_face_api_key
     groq_api_key=your_groq_api_key
     ```

4. **Explore the pipelines in the Jupyter notebooks**:

  - `notebooks/rag_pipeline.ipynb`
  - `notebooks/vector_rag.ipynb`


## Conclusion

The hybrid search pipeline effectively leverages the strengths of both BM25 and LanceDB, resulting in enhanced accuracy and relevance. 

The inclusion of LLM-powered answer generation, which has been implemented as part of the **bonus task** in **`rag_pipeline.ipynb`**, further enriches the user experience.
