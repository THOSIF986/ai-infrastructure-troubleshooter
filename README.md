# 🤖 AI Infrastructure Troubleshooting Assistant

An AI-powered infrastructure troubleshooting assistant designed to help users diagnose common **Linux, networking, cloud, security, and enterprise IT issues** using Retrieval-Augmented Generation (RAG) and multi-agent AI workflows.

The application combines **FastAPI, LangGraph, ChromaDB, Sentence Transformers, and Streamlit** to provide an interactive platform for intelligent technical troubleshooting.

---

## 🚀 Project Overview

Infrastructure teams frequently deal with issues such as:

- Server connectivity problems
- Network configuration errors
- VPN issues
- Operating system errors
- Security-related incidents
- Application failures
- Infrastructure configuration problems

This project provides an AI-assisted troubleshooting workflow where users can describe an infrastructure problem and receive relevant diagnostic guidance based on a knowledge base.

The system uses **Retrieval-Augmented Generation (RAG)** to retrieve relevant technical information before generating a response.

---

## ✨ Key Features

### 🤖 Multi-Agent AI Architecture

Uses **LangGraph** to coordinate specialized AI agents for different technical support scenarios.

The architecture is designed to route user problems to the most relevant troubleshooting specialist.

### 📚 RAG Knowledge Base

The system supports:

- Document ingestion
- PDF processing
- Document chunking
- Embedding generation
- Vector similarity search
- Context retrieval
- AI-generated responses using retrieved knowledge

Vector search is implemented using **ChromaDB** and embeddings.

### 🖥️ Infrastructure Troubleshooting

The system can be used as a foundation for troubleshooting:

- Linux
- Networking
- Windows
- VPN
- Security
- Enterprise IT
- General infrastructure issues

### 📸 Screenshot Error Diagnosis

Users can upload screenshots containing technical errors.

The application uses OCR to extract information from screenshots and assist with error diagnosis.

### 🎫 IT Ticket Management

The platform includes ticket-management functionality for:

- Creating tickets
- Tracking tickets
- Managing ticket status
- Viewing ticket information
- Maintaining troubleshooting history

### 🔐 Authentication & Security

The backend includes:

- JWT authentication
- API authentication
- Rate limiting
- Prompt-injection protection
- Role-based application workflows

### 🌐 REST API

The backend is developed using **FastAPI** and provides APIs for:

- Chat
- Authentication
- Knowledge base
- Tickets
- OCR diagnosis

### 📊 Interactive Dashboard

The Streamlit frontend provides an interactive interface for:

- AI troubleshooting
- Ticket management
- Knowledge-base management
- Screenshot diagnosis
- Dashboard analytics

---

## 🏗️ System Architecture

```text
                    ┌─────────────────────┐
                    │        User         │
                    │ Infrastructure     │
                    │      Problem        │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   Streamlit UI      │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │     FastAPI         │
                    │      Backend        │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │   LangGraph         │
                    │ Multi-Agent Workflow│
                    └──────────┬──────────┘
                               │
                    ┌──────────┴──────────┐
                    ▼                     ▼
             Specialist Agents       RAG Pipeline
                                          │
                                          ▼
                                  ┌───────────────┐
                                  │   ChromaDB    │
                                  │ Vector Store  │
                                  └───────┬───────┘
                                          │
                                          ▼
                                  Retrieved Context
                                          │
                                          ▼
                                  ┌───────────────┐
                                  │      LLM      │
                                  └───────┬───────┘
                                          │
                                          ▼
                              Troubleshooting Response
