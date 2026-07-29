# Day 16 – AI Lead Qualification & CRM Automation (V1)

## 📌 Project Overview

This workflow automatically qualifies new leads using AI.

Instead of manually reading every inquiry, AI analyzes the lead details, gives a lead score, and classifies the lead as Hot, Warm, or Cold.

Hot leads are saved to Google Sheets and a Telegram notification is sent to the sales team.

---

## 🎯 Business Problem

Companies receive many website or email inquiries every day.

Sales teams cannot contact every lead immediately.

This workflow helps by:

- Reading the lead
- Understanding the requirement
- Giving a lead score
- Identifying high-value leads
- Sending instant notifications for Hot leads

---

## 🛠 Technologies Used

- n8n
- OpenAI
- Structured Output Parser
- IF Node
- Google Sheets
- Telegram Bot

---

## 🏗 Workflow Architecture

Chat Trigger
↓
AI Lead Qualification Agent
↓
Structured Output Parser
↓
IF Node
↓
Google Sheets
↓
Telegram Notification

---

## 🤖 AI Responsibilities

The AI evaluates:

- Budget
- Timeline
- Requirement
- Buying Intent

Then returns:

- Lead Score
- Lead Quality
- Priority
- Reason
- Recommended Action

---

## 📊 Lead Classification

| Score | Quality | Priority |
|--------|----------|----------|
| 80+ | Hot | P1 |
| 50–79 | Warm | P2 |
| Below 50 | Cold | P3 |

---

## 📩 Telegram Notification

For Hot Leads:

- Name
- Company
- Budget
- Lead Score
- Timeline
- Requirement
- Recommended Action
- Reason

---

## 📚 What I Learned

- AI Lead Qualification
- Prompt Engineering
- Structured Output Parser
- Business Rules
- IF Conditions
- Google Sheets Integration
- Telegram Integration

---

## 🚀 Future Improvements (V2)

- Website Form Integration
- Gmail Trigger
- CRM Integration
- Better Timeline Detection
- Lead Summary
- Confidence Score
- Email Notification
- Follow-up Automation

---

## 📂 Project Status

✅ Version 1 Completed
