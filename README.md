# 🏆 RAG-Hive: AI Document Analyzer & Chatbot
![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-Framework-FF4B4B?logo=streamlit&logoColor=white)
![LangChain](https://img.shields.io/badge/LangChain-LLM_Orchestration-1c3c3c)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

An advanced, AI-driven web application for processing, analyzing, and interacting with your personal documents. Built with Streamlit, LangChain, and modern local Large Language Models (LLMs).
  
## 📋 Overview

RAG-Hive is a comprehensive Retrieval-Augmented Generation (RAG) platform that processes large text documents and generates detailed, context-aware answers to user queries. It features an intuitive web interface with real-time document embedding, semantic search, and interactive AI chat capability.

## ✨ Key Features

### 📊 Advanced AI Analytics
* **Intelligent Semantic Search** - Uses Hugging Face embeddings to understand the actual meaning behind your questions, not just keyword matching.
* **Local LLM Integration** - Powered by Meta's `Llama-3.2-1B-Instruct` running in FP16 precision for fast, accurate generation.
* **Smart Context Chunking** - Automatically breaks down massive documents with strategic overlap to preserve critical context.

### 🎯 Interactive Chat Interface
* **Real-time AI Responses** - Instant, streaming-style chat functionality.
* **Session Management** - Remembers your chat history securely during your active session.
* **Dynamic Status Indicators** - Visual spinners keep you informed during heavy AI processing.

### 💾 Data Management
* **Multi-Format Support** - Seamlessly accepts and extracts text from PDFs (`.pdf`), Word Documents (`.docx`), and Text files (`.txt`).
* **Temporary File Handling** - Securely processes files and cleans them up automatically to optimize storage.

### 🎨 Modern UI/UX
* **Responsive Design** - Works beautifully on desktop, tablet, and mobile.
* **Custom Styling** - Cyberpunk-inspired glowing headers with a professional orange and white color scheme.
* **Intuitive Navigation** - Clean sidebar for settings and a massive, user-friendly main chat window.

## 🚀 Technology Stack

* **Backend & UI:** Streamlit (Python)
* **AI Orchestration:** LangChain
* **Language Model:** Hugging Face Transformers (`meta-llama/Llama-3.2-1B-Instruct`)
* **Embeddings:** `sentence-transformers/all-MiniLM-L12-v2`
* **Vector Database:** FAISS (CPU)
* **Data Processing:** `pdfplumber`, `python-docx`
* **Cloud Deployment:** Google Colab, PyNgrok

## 📦 Installation

### Prerequisites
* Python 3.8 or higher
* `pip` package manager
* Hugging Face Account (with Access Token)
* Ngrok Account (with Auth Token for Colab tunneling)

### Local Setup
Clone the repository:
```bash
git clone [https://github.com/aliabdullah5485/RAG-Hive.git](https://github.com/aliabdullah5485/RAG-Hive.git)
cd RAG-Hive
```
Install dependencies:

```Bash
pip install -r requirements.txt
```
Set your Hugging Face environment variable:

```Bash
export HF_TOKEN="your_hugging_face_token"
```
Run the application:

```Bash
streamlit run app.py
```
(Note: To run this seamlessly in the cloud with GPU acceleration, use the provided RAG_Hive_Colab.ipynb notebook!)

📖 Usage
Input Data Format
Upload your files directly via the UI upload box. The system currently supports:

PDF (.pdf)

Word (.docx)

Text (.txt)

The RAG Pipeline Process
Document Processing: Extracts raw text and splits it into 256-character chunks with a 50-character overlap.

Vectorization: Converts text chunks into mathematical embeddings using all-MiniLM-L12-v2.

Querying: Matches your natural language question against the FAISS vector database.

Generation: Feeds the most relevant context to the Llama-3.2 model to generate a precise, factual answer.

## 📁 Project Structure
```Plaintext
RAG-Hive/
├── app.py                      # Main Streamlit application entry point
├── requirements.txt            # Python dependencies list
├── RAG_Hive_Colab.ipynb        # Ready-to-run Jupyter Notebook for Colab
├── README.md                   # Project documentation
├── .streamlit/                 
│   └── config.toml             # UI theme configurations
└── utils/                      
    ├── document_processor.py   # PDF/DOCX parsing and FAISS chunking
    ├── rag_pipeline.py         # Llama 3.2 initialization and querying
    └── ui_components.py        # Streamlit chat interface and custom CSS
```
## 🎓 Learning Outcomes
This project demonstrates proficiency in:

Full-Stack AI Development - Integrating Large Language Models with a modern frontend web interface.

Retrieval-Augmented Generation - Building robust vector search pipelines with FAISS and LangChain.

Software Architecture - Decoupling code into clean, maintainable, and modular Python components.

UI/UX Design - Creating an accessible, state-managed Streamlit interface.

Problem Solving - Handling complex document parsing and GPU VRAM management.

## 🔮 Future Enhancements
Integrate OCR capabilities for scanned document analysis.

Add PDF page-number citations directly into the AI's responses.

Historical chat tracking and .csv export capabilities.

Database integration for persistent document storage across sessions.

User authentication for secure, multi-tenant use.

## 👨‍💻 Author
Syed Hamad Ali Raza

GitHub:[ @Hamad Ali](https://github.com/SyedHamadAliRaza714)

Project Link: [RAG-Hive Repository](https://github.com/SyedHamadAliRaza714/RAG-Hive-AI-Document-Chatbot-)

## 📄 License
This project is open source and available under the MIT License.

## 🙏 Acknowledgments
Built as a demonstration of Full-Stack AI development capabilities.

Designed for educational and portfolio purposes to showcase programming proficiency.
