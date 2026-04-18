# 📌 RAG Pipeline & AI Chatbot using n8n

This project implements an end-to-end Retrieval-Augmented Generation (RAG) pipeline integrated with an AI chatbot for intelligent document querying. 🤖📄

## 🚀 Features

- 📥 Automated document ingestion from Google Drive
- ✂️ Text preprocessing and chunking
- 🧠 Embedding generation using HuggingFace
- 🗄️ Vector storage using Pinecone
- 💬 AI Agent powered chatbot using Groq LLM
- 🔄 Workflow orchestration via n8n

## 🏗️ Architecture

```text
Google Drive → File Download → Text Splitter → Embeddings → Pinecone
                                                        ↓
User Query → AI Agent → Vector Retrieval → Context → Response
```

## ⚙️ Tech Stack

- **Automation:** n8n 🔧
- **Vector DB:** Pinecone 🌲
- **Embeddings:** HuggingFace 🤗
- **LLM:** Groq ⚡
- **Text Processing:** Recursive Character Text Splitter ✂️

## 🔄 Workflow

- Google Drive trigger detects new files 📂
- Files are downloaded and processed 📥
- Text is split into smaller chunks ✂️
- Embeddings are generated 🧠
- Data is stored in Pinecone vector store 🗃️
- AI agent retrieves relevant context 🔎
- Chatbot generates accurate responses 💬

## 📷 Workflow Screenshot

_Add your screenshot here._

## 💡 Use Cases

- AI-powered document search 🔍
- Knowledge base chatbot 📚
- Business process automation ⚙️
- Enterprise Q&A systems 🏢

## 🔮 Future Improvements

- Multi-document querying 📑
- Streaming responses 🌊
- Multi-agent orchestration 🤝
- UI dashboard integration 📊

## 🤝 Contributing

Feel free to fork this repo and improve the pipeline! 🚀
