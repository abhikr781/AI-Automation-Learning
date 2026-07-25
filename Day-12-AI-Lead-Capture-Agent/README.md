# Day 12 - AI Lead Capture Agent

## 📌 Project Overview

Built an AI-powered Lead Capture Agent using n8n that collects user information, validates it using AI, stores the data in Google Sheets, and responds with a professional confirmation message.

This project simulates a real business lead collection workflow used by agencies, SaaS products, consultants, and marketing teams.

---

# 🚀 Project Objective

Create an AI Agent that can:

- Receive lead details
- Understand user input
- Extract required information
- Save leads automatically
- Send a confirmation response

---

# 🛠 Tech Stack

- n8n
- OpenAI Chat Model / Groq
- AI Agent
- Google Sheets
- Structured Output Parser
- Google OAuth
- JSON

---

# 📂 Workflow

User
   ↓
Chat Trigger
   ↓
AI Agent
   ↓
Structured Output
   ↓
Google Sheets
   ↓
AI Confirmation Response

---

# Workflow Nodes

## 1. Chat Trigger

Starts the workflow whenever a user sends a message.

Example:

Hi, my name is Abhishek.
Email: abc@gmail.com
Phone: 9876543210

---

## 2. AI Agent

The AI Agent extracts structured information from natural language.

Prompt Example:

You are a Lead Capture Assistant.

Extract:

- Name
- Email
- Phone
- Company
- Interest

Return only valid JSON.

---

## 3. Structured Output Parser

Converts AI output into proper JSON.

Example Output

{
  "name": "Abhishek Kumar",
  "email": "abc@gmail.com",
  "phone": "9876543210",
  "company": "ABC Pvt Ltd",
  "interest": "AI Automation"
}

---

## 4. Google Sheets

Automatically stores all lead information.

Columns

| Name | Email | Phone | Company | Interest | Date |
|------|-------|-------|----------|----------|------|

---

## 5. AI Response

After saving the data, AI replies naturally.

Example

Thanks Abhishek!

Your details have been successfully recorded.

We'll contact you soon.

Have a wonderful day!

---

# Features

✅ AI extracts information

✅ Works with natural language

✅ Saves data automatically

✅ No manual entry required

✅ Business-ready workflow

---

# Problems Faced

## Invalid JSON

Issue

AI was returning text instead of proper JSON.

Solution

Used Structured Output Parser.

---

## Google Sheets Error

Issue

Incorrect JSON mapping.

Solution

Mapped each field individually.

---

## Expression Errors

Issue

Wrong expression syntax.

Solution

Verified all mapped fields.

---

# Learning

During this project I learned:

- AI Agent workflows
- Structured Output Parsing
- JSON formatting
- Google Sheets integration
- Data mapping
- Prompt Engineering
- Error debugging
- Workflow automation

---

# Real World Use Cases

- Lead Generation
- Contact Forms
- CRM Automation
- Client Onboarding
- Marketing Campaigns
- Agency Automation
- Sales Automation

---

# Future Improvements

- Email notification
- WhatsApp notification
- Airtable integration
- HubSpot CRM
- Notion Database
- Duplicate lead detection
- Lead scoring
- Auto follow-up

---

# Skills Gained

- n8n Automation
- AI Agents
- Google Sheets API
- Structured Output
- Prompt Engineering
- JSON
- Workflow Design
- Business Automation

---

# Final Result

Successfully built an AI Lead Capture Agent capable of collecting user information, extracting structured data using AI, storing it automatically in Google Sheets, and providing a natural confirmation response.

This project demonstrates how AI can automate manual lead collection processes and is a strong portfolio project for AI Automation Engineer roles.

---

# Repository Structure

Day-12-AI-Lead-Capture-Agent/

│── README.md

│── workflow.json

│── screenshots/

│      workflow.png

│      google-sheet.png

│      output.png

---

Author

Abhishek Kumar

Learning AI Automation with n8n 🚀
