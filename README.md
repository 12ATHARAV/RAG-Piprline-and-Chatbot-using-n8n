# RAG Pipeline & Chatbot using n8n

A Retrieval-Augmented Generation (RAG) chatbot built with **n8n**, **Pinecone**, **Hugging Face embeddings**, and **Groq LLM**.  
This project automates document ingestion from Google Drive, splits and embeds the text, stores it in a vector database, and answers user queries through a chat interface using retrieved context.

---

## Overview

This project demonstrates a complete RAG workflow:

- Documents are picked up automatically from **Google Drive**.
- Files are downloaded and processed using a text loader and recursive character splitter.
- Document chunks are converted into embeddings using **Hugging Face**.
- Embeddings are stored in **Pinecone Vector Store** for semantic search.
- A chat message triggers the **AI Agent**.
- The agent uses **Groq Chat Model** along with the vector store to generate context-aware answers.

---

## Features

- Automated document ingestion from Google Drive.
- Text chunking for better retrieval quality.
- Vector storage using Pinecone.
- Semantic retrieval powered by embeddings.
- AI chatbot interface using n8n chat workflow.
- Context-aware responses based on retrieved documents.
- Modular workflow design that is easy to extend.

---

## Architecture

The workflow is divided into two main parts:

### 1. Document Ingestion Pipeline
- **Google Drive Trigger** detects new files.
- **Download File** retrieves the document.
- **Default Data Loader** loads the file content.
- **Recursive Character Text Splitter** splits text into chunks.
- **Hugging Face Embeddings** converts chunks into vector representations.
- **Pinecone Vector Store** stores embeddings for future retrieval.

### 2. Chatbot Query Pipeline
- **When Chat Message Received** triggers the chatbot.
- **AI Agent** handles the user query.
- **Groq Chat Model** generates responses.
- **Pinecone Vector Store Tool** retrieves relevant chunks from the knowledge base.
- The chatbot returns an answer based on retrieved context.

---

## Tech Stack

- **n8n** – Workflow automation and orchestration.
- **Google Drive** – Document source.
- **Pinecone** – Vector database.
- **Hugging Face Embeddings** – Text embeddings.
- **Groq** – LLM inference.
- **AI Agent / Chat Workflow** – Chat-based user interaction.

---

## Workflow Diagram

### RAG Pipeline
![RAG Pipeline](ragn8n_architect-2.jpg)

### Chatbot Output
![Chatbot Output](ragn8n_output.jpg)

---

## How It Works

1. Upload a document to Google Drive.
2. n8n detects the new file using the trigger.
3. The file is downloaded and split into smaller chunks.
4. Each chunk is embedded and stored in Pinecone.
5. When a user sends a chat message, the AI agent searches Pinecone for relevant context.
6. Groq generates a response using the retrieved context.
7. The chatbot returns a helpful and context-aware answer.

---

## Setup Instructions

### Prerequisites
- An **n8n** instance.
- A **Pinecone** account and index.
- A **Groq API key**.
- A **Hugging Face API key**.
- A connected **Google Drive** account.

### Configuration Steps
1. Import the workflow into n8n.
2. Configure Google Drive credentials.
3. Set up Pinecone credentials and index details.
4. Configure Hugging Face embeddings.
5. Add Groq API credentials.
6. Test the ingestion pipeline by uploading a file to Google Drive.
7. Open the chat interface and ask a question based on the uploaded document.

---

## Example Use Case

This chatbot can be used for:
- Internal knowledge base assistants.
- Document Q&A systems.
- Policy or legal document search.
- Educational assistants.
- Customer support automation.

---

## Future Improvements

- Add support for multiple file formats.
- Include metadata-based filtering in retrieval.
- Improve chunking strategy for better recall.
- Add conversation memory for multi-turn chat.
- Deploy the chatbot as a public web app.

---

## Project Status

This project is currently functional and demonstrates a full end-to-end RAG workflow built with n8n.

---

## License

This project is open for personal and educational use.
