<div align="center">
  <img src="https://raw.githubusercontent.com/langchain-ai/langchain/master/docs/static/img/langchain_logo.png" alt="LangChain Logo" width="200"/>
  
  # 🚀 LangChain Masterclass: From Basics to Advanced
  
  *A comprehensive, step-by-step repository for mastering Large Language Model (LLM) application development using the LangChain framework.*

  [![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)](https://www.python.org/)
  [![LangChain](https://img.shields.io/badge/LangChain-0.3.x-green.svg)](https://langchain.com/)
  [![OpenAI](https://img.shields.io/badge/OpenAI-Integrated-orange.svg)](https://openai.com/)
  [![Ollama](https://img.shields.io/badge/Ollama-Local_LLMs-lightgrey.svg)](https://ollama.com/)
</div>

<hr/>

## 📖 Table of Contents
- [About the Project](#-about-the-project)
- [Project Architecture & Modules](#-project-architecture--modules)
  - [1. OpenAI Integration](#1-openai-integration-)
  - [2. Local LLMs with Ollama](#2-local-llms-with-ollama-)
  - [3. Data Ingestion](#3-data-ingestion-)
  - [4. Data Transformers](#4-data-transformers-)
  - [5. Embeddings](#5-embeddings-)
  - [6. Vector Stores](#6-vector-stores-)
- [Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Environment Variables](#-environment-variables)
- [Key Technologies & Libraries](#-key-technologies--libraries)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🎯 About the Project

Welcome to the **LangChain Masterclass**! This repository serves as a practical, hands-on guide for building modern AI and LLM applications. Whether you're looking to build simple chat interfaces, Retrieval-Augmented Generation (RAG) pipelines, or complex data processing systems, this repository contains reproducible notebooks and scripts to get you there.

The project is structured modularly, taking you from basic LLM interactions all the way to advanced text splitting, custom embeddings, and robust vector database management.

---

## 🏗 Project Architecture & Modules

The repository is divided into 6 core modules, each focusing on a fundamental pillar of the LangChain ecosystem.

### 1. OpenAI Integration (`/1-Openai`)
Learn how to interface with state-of-the-art closed-source models.
*   **`1.1-GettingStarted.ipynb`**: The Hello World of LangChain. Setting up API keys, basic prompts, and LLM chains.
*   **`1.2-Simpleapp.ipynb`**: Building a basic, functional LLM application with prompt templates and output parsers.

### 2. Local LLMs with Ollama (`/2-Ollama`)
Run LLMs completely locally for privacy and cost-efficiency.
*   **`app.py`**: A complete script demonstrating how to serve and query open-weight models locally using Ollama and LangChain.

### 3. Data Ingestion (`/3-DataIngestion`)
The first step of RAG: Getting your data into the system.
*   **`dataingestion.ipynb`**: Comprehensive examples of using Document Loaders to read from diverse sources:
    *   PDFs (`attention.pdf`)
    *   Raw Text (`speech.txt`)
    *   XML / Structured Data (`records.xml`)

### 4. Data Transformers (`/4-Data Trnasformer`)
Prepare your ingested documents for embedding by chunking them optimally.
*   **`4.1-RecuriveCharactertextsplitter.ipynb`**: The industry standard for chunking natural language text.
*   **`4.2-CharacterTextsplitter.ipynb`**: Basic, rigid character-based splitting.
*   **`4.3-HTMLtextsplitter.ipynb`**: Preserving semantic structure when scraping websites.
*   **`4.4-RecursiveJSONsplitter.ipynb`**: Intelligently parsing and chunking complex nested JSON objects.

### 5. Embeddings (`/5-Embeddings`)
Convert text into dense vector representations to capture semantic meaning.
*   **`5.1-OpenAiEmbedding.ipynb`**: High-quality, cloud-based embeddings (e.g., `text-embedding-3-small`).
*   **`5.2-Ollamaembeddings.ipynb`**: Local, privacy-preserving embeddings.
*   **`5.3-huggingface.ipynb`**: Leveraging open-source sentence-transformers directly from the Hugging Face Hub.

### 6. Vector Stores (`/6-VectorStore`)
Store your embeddings and perform blazing-fast semantic similarity searches.
*   **`6.1-Faiss.ipynb`**: Using Meta's FAISS (Facebook AI Similarity Search) for efficient local, in-memory vector storage.
*   **`6.2-Chroma.ipynb`**: Setting up and querying ChromaDB, a highly popular AI-native open-source vector database.

---

## 🚀 Getting Started

Follow these instructions to set up your local development environment.

### Prerequisites
*   Python 3.10 or higher
*   An [OpenAI API Key](https://platform.openai.com/api-keys) (for OpenAI modules)
*   [Ollama installed locally](https://ollama.com/download) (for Local LLM modules)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/Langchain.git
   cd Langchain
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   # On Windows:
   .\venv\Scripts\activate
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

---

## 🔐 Environment Variables

You need to provide your API keys to interact with external providers. 
Create a `.env` file in the root directory and add the following keys:

```env
OPENAI_API_KEY="your_openai_api_key_here"
HUGGINGFACEHUB_API_TOKEN="your_huggingface_token_here"
LANGCHAIN_TRACING_V2="true"  # Optional: For LangSmith observability
LANGCHAIN_API_KEY="your_langsmith_key_here"
```

---

## 🛠 Key Technologies & Libraries

This project leverages a powerful stack of modern AI tools (as defined in `requirements.txt`):

| Category | Libraries |
| :--- | :--- |
| **Core Framework** | `langchain`, `langchain-core`, `langchain-community` |
| **Model Providers** | `langchain-openai`, `langchain-huggingface`, `langchain-groq`, `openai` |
| **Vector Databases** | `chromadb`, `faiss-cpu`, `langchain-chroma` |
| **Document Parsing** | `pypdf`, `pymupdf`, `beautifulsoup4`, `unstructured`, `youtube-transcript-api` |
| **Data Processing** | `pandas`, `duckdb`, `SQLAlchemy` |

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! 
Feel free to check the [issues page](../../issues) if you want to contribute.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---
<div align="center">
  <i>Built with ⚡ by an AI enthusiast.</i>
</div>
