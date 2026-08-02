# Day 18 – AI CRM Follow-up Agent

## 📌 Project Overview

This workflow automatically checks CRM leads and identifies which clients need a follow-up.

Instead of manually reviewing every lead, AI analyzes the CRM data, updates the lead status, and records the latest activity.

---

## 🎯 Business Problem

Sales teams often forget to follow up with leads on time.

This can result in missed opportunities and lost revenue.

This workflow helps by:

- Reading CRM data from Google Sheets
- Identifying leads that need follow-up
- Updating the lead status
- Recording follow-up activity
- Maintaining CRM automatically

---

## 🛠 Technologies Used

- n8n
- Google Sheets
- IF Node
- Edit Fields
- Date & Time

---

## 🏗 Workflow Architecture

Google Sheets
↓
Read Leads
↓
IF Condition
↓
Update CRM Status
↓
Update Last Activity
↓
Save Back to Google Sheets

---

## 🤖 Workflow Responsibilities

The workflow checks:

- Lead Quality
- Last Contact
- Current Status

Then it decides:

- Follow-up Required
- Update Status
- Update Last Activity
- Increase Follow-up Count

---

## 📊 CRM Fields

- Lead ID
- Client Name
- Email
- Lead Quality
- Status
- Last Contact
- Follow-up Count
- Last Activity

---

## 📚 What I Learned

- CRM Automation
- Google Sheets Update
- Business Rules
- Conditional Logic
- Sales Workflow Automation

---

## 📂 Project Status

✅ Version 1 Completed
