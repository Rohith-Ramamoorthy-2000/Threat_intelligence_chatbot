# Threat_intelligence_chatbot

# Gen AI-Lab:3
# Team member:
Rohith, Vishruta, Bertilla

# Threat Intelligence Chatbot using RAG

## Overview

This project is an AI-powered Threat Intelligence Chatbot developed using Retrieval-Augmented Generation (RAG). The chatbot uses the MITRE ATT&CK Enterprise dataset as a cybersecurity knowledge base and provides intelligent responses to cybersecurity-related questions.

The system combines semantic search, vector databases, and Large Language Models (LLMs) to generate contextual threat intelligence responses.

---

## Features

* Retrieval-Augmented Generation (RAG) architecture
* MITRE ATT&CK Enterprise knowledge integration
* Semantic search using MiniLM embeddings
* FAISS vector database for fast retrieval
* FLAN-T5 for response generation
* Interactive Gradio chatbot interface
* Google Drive storage support for persistent vector database
* Lightweight and Colab-friendly implementation

---

## Technologies Used

| Technology            | Purpose                     |
| --------------------- | --------------------------- |
| Python                | Core development            |
| Google Colab          | Development environment     |
| MITRE ATT&CK          | Threat intelligence dataset |
| Sentence Transformers | Embedding generation        |
| FAISS                 | Vector similarity search    |
| FLAN-T5               | Language model              |
| Gradio                | Web interface               |
| Pandas                | Data processing             |

---

## Project Architecture

```text
User Query
    ↓
MiniLM Embedding
    ↓
FAISS Vector Search
    ↓
Top-K Relevant Chunks
    ↓
FLAN-T5 LLM
    ↓
Generated Response
    ↓
Gradio Interface
```

---

## Dataset

This project uses the Enterprise ATT&CK dataset from MITRE ATT&CK.

### Official Dataset Link

```text
https://raw.githubusercontent.com/mitre/cti/master/enterprise-attack/enterprise-attack.json
```

---

## Installation

### Clone Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_LINK
cd YOUR_PROJECT_FOLDER
```

---

### Install Dependencies

```bash
pip install transformers
pip install sentence-transformers
pip install faiss-cpu
pip install gradio
pip install pandas
```

---

## Google Colab Setup

Mount Google Drive:

```python
from google.colab import drive
drive.mount('/content/drive')
```

---

## Folder Structure

```text
threat_chatbot/
│
├── data/
│   ├── enterprise-attack.json
│   └── mitre_data.csv
│
├── faiss_index/
│   ├── index.faiss
│   └── chunks.pkl
│
├── notebook/
│   └── threat_chatbot.ipynb
│
└── README.md
```

---

## Workflow

1. Download MITRE ATT&CK dataset
2. Convert JSON to CSV
3. Chunk the text data
4. Generate embeddings using MiniLM
5. Store embeddings in FAISS
6. Retrieve relevant chunks using semantic similarity
7. Generate contextual responses using FLAN-T5
8. Display results through Gradio UI

---

## Example Questions

* What is T1059?
* Explain privilege escalation techniques
* How do attackers use PowerShell?
* What techniques are used for persistence?
* Explain phishing-related attack techniques
* What is credential dumping?
* How can lateral movement be detected?

---

## Models Used

### Embedding Model

```text
all-MiniLM-L6-v2
```

### LLM

```text
google/flan-t5-base
```

---

## Vector Database

This project uses FAISS for efficient similarity search and retrieval.

---

## User Interface

The chatbot interface is built using Gradio.

Features:

* Interactive chat UI
* Large readable response area
* Easy deployment in Colab

---

## Future Improvements

* CVE integration
* Threat actor intelligence
* Real-time threat feeds
* LangChain integration
* Memory-enabled chatbot
* Multi-source RAG
* Deployment using Docker or Hugging Face Spaces

---

## Advantages

* Fast retrieval of cybersecurity knowledge
* Context-aware responses
* Reduced hallucination compared to standalone LLMs
* Lightweight and scalable
* Beginner-friendly implementation

---

## Conclusion

This project demonstrates how Retrieval-Augmented Generation (RAG) can improve cybersecurity intelligence systems by combining semantic retrieval with Large Language Models. The chatbot provides accurate and contextual answers using the MITRE ATT&CK knowledge base and can support SOC analysts, researchers, and cybersecurity learners.

---

## References

* [MITRE ATT&CK](https://attack.mitre.org?utm_source=chatgpt.com)
* [FAISS Documentation](https://faiss.ai?utm_source=chatgpt.com)
* [Sentence Transformers](https://www.sbert.net?utm_source=chatgpt.com)
* [Hugging Face Transformers](https://huggingface.co/docs/transformers/index?utm_source=chatgpt.com)
* [Gradio Documentation](https://www.gradio.app?utm_source=chatgpt.com)

