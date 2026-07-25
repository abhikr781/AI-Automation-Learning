# Day 13 - AI Customer Support Agent (RAG)

## 📌 Project Overview

Built an AI-powered Customer Support Agent using n8n and Qdrant Vector Database.

The chatbot answers customer queries using a Knowledge Base instead of making up responses.

This project demonstrates Retrieval-Augmented Generation (RAG), where AI searches relevant information before generating an answer.

---

# 🚀 Project Objective

Build an AI chatbot that:

- Understands customer questions
- Searches company documents
- Retrieves relevant information
- Generates accurate responses
- Avoids hallucinations
- Remembers conversation history

---

# 🛠 Tech Stack

- n8n
- AI Agent
- Groq Chat Model
- OpenAI/FastEmbed Embeddings
- Qdrant Vector Database
- PDF Knowledge Base
- Simple Memory

---

# Workflow Architecture

## Indexing Workflow

PDF

↓

Extract PDF Text

↓

Split into Chunks

↓

Generate Embeddings

↓

Store Vectors in Qdrant

---

## Chat Workflow

User

↓

Chat Trigger

↓

AI Agent

↓

Memory

↓

Qdrant Retriever

↓

Relevant Context

↓

LLM

↓

Customer Response

---

# Features

- AI-powered customer support
- Retrieval-Augmented Generation (RAG)
- PDF-based knowledge base
- Conversation memory
- Hallucination prevention
- Semantic search
- Fast response generation

---

# AI Prompt

You are an AI Customer Support Assistant.

Answer only using the provided knowledge base.

If the information is unavailable, politely respond:

"I couldn't find that information in the knowledge base."

Never create your own answers.

Keep responses short and professional.

---

# Knowledge Base

Example company information:

- Office Timing
- Working Days
- Refund Policy
- Email
- Phone Number
- Services
- Address

---

# Test Cases

Question:

Office timing?

Answer:

9 AM – 6 PM

---

Question:

Refund policy?

Answer:

Refund available within 7 days.

---

Question:

Services?

Answer:

AI Automation, WordPress Development, Cloud Consulting

---

Question:

CEO Name?

Answer:

I couldn't find that information in the knowledge base.

---

# Learning Outcomes

- Retrieval-Augmented Generation (RAG)
- Embedding Generation
- Semantic Search
- Vector Database
- Knowledge Base Design
- Memory Management
- AI Prompt Engineering
- Customer Support Automation

---

# Real World Applications

- Customer Support Chatbots
- Company FAQ Bots
- HR Policy Assistant
- Internal Knowledge Assistant
- University Help Desk
- Healthcare Information Assistant
- Legal Knowledge Assistant

---

# Future Improvements

- Multiple PDF support
- Automatic PDF upload
- Website chatbot
- WhatsApp integration
- Telegram integration
- Google Drive sync
- CRM integration
- Human handoff

---

# Repository Structure

Day-13-AI-Customer-Support-Agent/

│── README.md

│── workflow.json

│── screenshots/

│      workflow.png

│      qdrant.png

│      chat-output.png

│      pdf-upload.png

---

# Skills Gained

- AI Agents
- RAG
- Vector Database
- Embeddings
- Knowledge Retrieval
- Semantic Search
- Prompt Engineering
- AI Workflow Design

---

# Final Result

Successfully built a production-style AI Customer Support Agent capable of answering customer queries using a PDF-based knowledge base.

The chatbot retrieves relevant information from Qdrant Vector Database and generates accurate, context-aware responses while avoiding hallucinations.

This project represents a real-world AI customer support system used by modern SaaS companies and enterprises.
