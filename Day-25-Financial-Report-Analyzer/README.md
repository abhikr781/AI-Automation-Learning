# 📊 Day 25 — AI Financial Report Analyzer

An AI-powered financial analysis workflow that converts structured financial data into an executive-level financial brief.

The system combines deterministic financial calculations, rule-based risk detection, and AI-generated financial commentary.

---

## 🎯 Objective

Automatically answer:

- What changed financially?
- Is the company improving or deteriorating?
- What are the major financial risks?
- What areas require management attention?

---

## ⚙️ Workflow

Financial Report
      ↓
Data Extraction
      ↓
Financial Calculations
      ↓
Trend Analysis
      ↓
Risk Engine
      ↓
AI Financial Analyst
      ↓
Executive Brief
      ↓
Telegram

---

## 🚀 Key Features

- Revenue and profitability analysis
- YoY growth calculations
- Free Cash Flow analysis
- Debt and liquidity analysis
- Deterministic risk detection
- Missing-data protection
- AI-generated executive summary
- Management attention areas
- Automated Telegram reporting

---

## 🧮 Deterministic Analysis

The calculation layer handles financial logic before the data reaches the AI.

Examples:

Free Cash Flow = Operating Cash Flow - CapEx

Growth % =
(Current - Prior) / |Prior| × 100

Risk signals include:

- High Debt-to-Equity
- Rising debt
- Declining operating cash flow
- Negative/declining FCF
- Cash depletion
- Low Current Ratio
- Margin compression

Risk levels:

Low
Medium
High

---

## 🤖 AI Financial Analyst

The AI receives the structured financial results and generates:

- Executive Summary
- Key Strengths
- Key Concerns
- Management Attention Areas
- "What Changed?" narrative

The AI is instructed to use only the provided financial values and avoid inventing missing data.

---

## 🛡️ Missing Data Handling

Unavailable financial information remains unavailable.

For example:

Debt → N/A
Current Ratio → N/A
CapEx → N/A
Free Cash Flow → N/A

The system does not automatically convert missing values into `0`.

---

## 🧪 Tested Scenarios

The workflow was tested against:

- ✅ Mixed financial performance
- ✅ Strong/healthy company
- ✅ Severe financial distress
- ✅ Missing/incomplete financial data

---

## 🛠️ Tech Stack

- **n8n** — Workflow automation
- **JavaScript** — Financial calculations & risk engine
- **LLM** — Financial analysis and commentary
- **JSON** — Structured financial data
- **Telegram** — Automated reporting

---

## 🔮 Future Improvements

Possible future upgrades:

- Historical multi-year analysis
- Financial dashboards
- Industry benchmarking
- Anomaly detection
- Scheduled reporting
- Database storage
- Human approval workflow
- Production monitoring

---

## 📌 Status

**Core Version — Complete ✅**

The workflow successfully combines deterministic financial analysis with AI-generated executive reporting and automated delivery.
