# Day 08 - AI Resume Analyzer

## 📌 Project Overview

This project is an AI-powered Resume Analyzer built using n8n and OpenAI.

The user uploads a resume (PDF), the workflow extracts all text from the document and sends it to an AI Agent which performs a complete ATS-style analysis.

The AI generates:

- Resume Score
- ATS Compatibility Score
- Missing Keywords
- Technical Skills
- Soft Skills
- Missing Skills
- Strengths
- Weaknesses
- Resume Improvement Suggestions

---

## 🚀 Tech Stack

- n8n
- OpenAI GPT
- Extract From File Node
- AI Agent
- Respond to Webhook

---

## Workflow

User Upload PDF

↓

Extract From File

↓

AI Agent (OpenAI)

↓

Generate Resume Analysis

↓

Display Result

---

## Nodes Used

### 1. When Chat Message Received

Receives the uploaded resume.

---

### 2. Extract From File

Extracts text from the uploaded PDF.

Output:

- Resume Text

---

### 3. AI Agent

Analyzes the extracted resume.

Prompt includes:

- Resume Score
- ATS Score
- Missing Keywords
- Skills
- Weaknesses
- Strengths
- Improvement Suggestions

---

### 4. Respond to Webhook

Returns the formatted Resume Analysis Report.

---

## AI Prompt

The AI analyzes the resume and returns:

- Candidate Name
- Overall Resume Score (/100)
- ATS Compatibility Score (/100)
- ATS Explanation
- Missing Keywords
- Technical Skills
- Soft Skills
- Missing Skills
- Key Strengths
- Weaknesses
- Resume Improvement Suggestions

Always return the response in clean Markdown format.

---

## Sample Output

Resume Score: 75/100

ATS Score: 68/100

Technical Skills

- WordPress
- PHP
- HTML
- CSS
- JavaScript
- Linux
- MySQL

Missing Skills

- Selenium
- Python
- Cloud Computing
- Agile
- SaaS

Suggestions

- Add measurable achievements
- Improve ATS formatting
- Add cloud skills
- Include automation tools
- Quantify work experience

---

## Learning Outcome

During this project I learned:

- PDF extraction in n8n
- AI Agent workflow
- Prompt Engineering
- Resume parsing
- ATS analysis
- Markdown response formatting

---

## Future Improvements

- DOCX support
- Resume vs Job Description Matching
- ATS Keyword Optimization
- Resume Rewrite
- Export PDF Report
- Email Report Automatically

---

## Folder Structure

Day-08-AI-Resume-Analyzer

├── workflow.json

├── README.md

└── screenshots

---

## Author

Abhishek Kumar

Learning AI Automation using n8n 🚀
