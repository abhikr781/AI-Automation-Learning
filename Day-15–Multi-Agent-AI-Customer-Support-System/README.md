# Day 15 - Multi-Agent AI Customer Support System

## 📌 Project Overview

Built a Multi-Agent AI Customer Support System using n8n and OpenAI.

Unlike a traditional AI workflow where a single AI model performs every task, this project uses multiple specialized AI Agents working together. Each agent has a dedicated responsibility, making the workflow modular, scalable, and easier to maintain.

This architecture closely resembles how modern AI systems are designed in production environments.

---

# 🚀 Project Objective

Build an intelligent customer support system where multiple AI agents collaborate to:

- Classify incoming customer emails
- Extract structured customer information
- Generate professional email replies
- Automatically send responses through Gmail

---

# 🛠 Tech Stack

- n8n
- Gmail Trigger
- AI Agent
- OpenAI Chat Model
- Structured Output Parser
- Switch Node
- Gmail Send Message

---

# Multi-Agent Architecture

Incoming Email

↓

Gmail Trigger

↓

AI Agent 1 – Email Classifier

↓

Structured Output Parser

↓

Switch Node

↓

AI Agent 2 – Information Extractor

↓

Structured Output Parser

↓

AI Agent 3 – Reply Generator

↓

Gmail Send Message

---

# Agent Responsibilities

## 🤖 Agent 1 – Email Classification Agent

### Responsibility

Analyze the incoming email and classify it.

Extracts:

- Category
- Priority
- Sentiment

Example Output

```json
{
  "category": "Sales",
  "priority": "High",
  "sentiment": "Positive"
}
```

---

## 🤖 Agent 2 – Information Extraction Agent

### Responsibility

Extract structured customer information.

Extracts:

- Customer Name
- Company
- Phone
- Email
- Main Issue
- Summary

Example Output

```json
{
  "customer_name": "Amit",
  "company": null,
  "phone": null,
  "email": "amit@gmail.com",
  "main_issue": "Trading Website Development",
  "summary": "Customer requires an urgent trading website."
}
```

---

## 🤖 Agent 3 – Reply Generation Agent

### Responsibility

Generate a professional customer support email.

Rules followed:

- Professional tone
- Friendly response
- No Subject line
- Maximum 120 words
- Proper email formatting
- Personalized greeting
- Professional signature

---

# Workflow Explanation

## Step 1

The Gmail Trigger monitors the inbox for new emails.

---

## Step 2

The email is sent to the Email Classification Agent.

The agent identifies:

- Category
- Priority
- Sentiment

---

## Step 3

The Structured Output Parser converts the AI response into valid JSON.

---

## Step 4

The Switch Node routes the workflow based on the detected category.

For this project, the Support flow was implemented while keeping the workflow ready for additional categories such as Sales, HR, General, and Spam.

---

## Step 5

The Information Extraction Agent reads the email and extracts important customer details.

---

## Step 6

Another Structured Output Parser converts the extracted information into clean JSON.

---

## Step 7

The Reply Generation Agent creates a professional email reply using the extracted information.

The reply includes:

- Personalized greeting
- Acknowledgement of the customer's request
- Professional response
- Closing signature

---

## Step 8

The Gmail Send Message node automatically sends the generated email back to the customer.

---

# Features

- Multi-Agent AI Architecture
- Automatic Email Classification
- Structured Data Extraction
- AI-powered Email Replies
- Professional Email Formatting
- Conditional Routing
- Fully Automated Workflow

---

# Sample Outputs

## Agent 1

```json
{
  "category": "Support",
  "priority": "Medium",
  "sentiment": "Neutral"
}
```

---

## Agent 2

```json
{
  "customer_name": "Amit",
  "company": null,
  "phone": null,
  "email": "amit@gmail.com",
  "main_issue": "Trading Website Development",
  "summary": "Customer needs an urgent trading website."
}
```

---

## Agent 3

```text
Hello Amit,

Thank you for contacting ABC Technologies regarding your trading website requirement.

We have received your request and our team is reviewing the details. We will get back to you shortly.

If you have any additional information, please reply to this email.

Best Regards,

ABC Technologies
```

---

# What I Learned

- Multi-Agent Architecture
- AI Agent Specialization
- Prompt Engineering
- Structured Output Parsing
- Conditional Workflow Routing
- JSON-based AI Communication
- Gmail Automation
- Professional Email Generation

---

# Real-World Applications

- Customer Support Automation
- Help Desk Systems
- Sales Inquiry Automation
- HR Email Processing
- Business Email Management
- AI Customer Service Platforms

---

# Challenges Faced

During development, several challenges were encountered and resolved:

- Prompt variable mapping
- AI Agent configuration
- Structured Output formatting
- Switch node routing
- Email formatting improvements
- Prompt optimization
- Professional email generation

These challenges helped improve understanding of AI workflow architecture and prompt engineering.

---

# Future Improvements (Version 2)

- Google Sheets Logging
- Telegram Alerts for High Priority Emails
- Spam Detection
- Confidence Score
- Email Templates
- Customer Memory
- Knowledge Base (RAG)
- CRM Integration
- Attachment Processing
- Analytics Dashboard

---

# Repository Structure

Day-15-Multi-Agent-AI-Customer-Support/

│── README.md

│── workflow.json

│── screenshots/

│      workflow.png

│      agent-1-classifier.png

│      agent-2-extractor.png

│      agent-3-reply.png

│      output.png

---

# Concepts Learned

- Multi-Agent Systems
- AI Agent Collaboration
- Prompt Engineering
- Structured Output Parser
- Workflow Orchestration
- Conditional Routing
- Automated Email Processing
- AI-based Customer Support

---

# Interview Questions

1. What is a Multi-Agent AI System?
2. Why use multiple AI agents instead of a single agent?
3. What is the role of a Structured Output Parser?
4. Why is structured JSON important in AI workflows?
5. How does a Switch Node improve workflow scalability?
6. How do AI agents communicate with each other?
7. What are the advantages of modular AI architecture?
8. How would you scale this workflow for thousands of emails per day?

---

# Final Result

Successfully built a Multi-Agent AI Customer Support System capable of automatically receiving customer emails, classifying requests, extracting structured information, generating professional responses, and sending replies through Gmail.

This project demonstrates how specialized AI agents can collaborate to solve business problems efficiently while following a modular and scalable architecture used in real-world AI automation systems.
