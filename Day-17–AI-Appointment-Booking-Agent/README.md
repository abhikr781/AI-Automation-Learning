# Day 17 – AI Appointment Booking Agent

## 📌 Project Overview

This workflow automatically books a Google Calendar meeting from a user's chat message using AI.

The AI reads the meeting request, extracts the required information, creates a Google Calendar event, and sends a confirmation message on Telegram.

---

## 🎯 Business Problem

Companies receive many meeting requests through chat, email, or contact forms.

Reading every message manually and creating calendar events takes time and increases the chance of mistakes.

This workflow automates the appointment booking process using AI.

---

## 🛠 Technologies Used

- n8n
- OpenAI
- Structured Output Parser
- Google Calendar
- Telegram Bot

---

## 🏗 Workflow Architecture

Chat Trigger

↓

AI Appointment Booking Agent

↓

Structured Output Parser

↓

Google Calendar

↓

Telegram Notification

---

## 🤖 AI Responsibilities

The AI reads the user's message and extracts:

- Name
- Email
- Meeting Topic
- Meeting Date
- Meeting Time
- Meeting Duration

The extracted information is returned in a structured JSON format for the next workflow steps.

---

## 📅 Calendar Event Details

The workflow creates a Google Calendar event using:

- Event Title
- Meeting Date
- Start Time
- End Time
- Description

---

## 📩 Telegram Notification

After the meeting is created successfully, a confirmation message is sent with:

- Meeting Date
- Meeting Time
- Meeting Topic

---

## 📚 What I Learned

- AI Appointment Booking
- Prompt Engineering
- Structured Output Parser
- AI Data Extraction
- JSON Schema Design
- Google Calendar Integration
- Telegram Integration
- Date and Time Formatting

---

## 💡 Challenges Faced

- AI was returning date and time together in one field.
- I updated the JSON schema to return date and time separately.
- I converted the meeting time into a user-friendly 12-hour format before sending the Telegram notification.

---

## 🚀 Future Improvements (V2)

- Check Google Calendar availability before booking.
- Suggest another time if the selected slot is busy.
- Automatically create a Google Meet link.
- Send email confirmation to the user.
- Send reminder notifications before the meeting.
- Allow users to reschedule or cancel appointments.
- Support multiple input sources like Gmail, Website Forms, and WhatsApp.

---

## 📂 Project Status

✅ Version 1 Completed
