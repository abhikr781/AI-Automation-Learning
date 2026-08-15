Bilkul bhai. **Same content ko ek single copy-paste block mein** de raha hoon. Isko direct `README.md` mein paste kar sakte ho.

````markdown
# Day 24 – AI Resume Screening & Candidate Evaluation Agent

## Overview

An AI-powered resume screening workflow built in n8n.

The workflow analyzes a Job Description (JD), extracts structured hiring requirements, analyzes uploaded resumes against those requirements, calculates a deterministic candidate score, generates a hiring recommendation, and stores the final evaluation in Google Sheets.

The current workflow is designed to separate:

- AI-based information/evidence extraction
- deterministic scoring and decision logic
- structured final output

---

## Workflow

```text
When chat message received
        ↓
Extract from File
        ↓
AI JD Analyzer
        ↓
Resume Analyzer Agent
        ↓
Code in JavaScript
        ↓
Append row in sheet
````

### AI JD Analyzer Sub-nodes

```text
AI JD Analyzer
├── JD Auditor (Chat Model)
└── Structured JD Requirements (Output Parser)
```

### Resume Analyzer Agent Sub-nodes

```text
Resume Analyzer Agent
├── Resume Analyzer Chat Model
└── Structured Resume Analyzer (Output Parser)
```

---

## 1. Input

The workflow accepts:

* Job Description
* Resume file (PDF)

The PDF is processed through the **Extract from File** node.

The extracted resume text is then supplied to the Resume Analyzer Agent.

---

## 2. Job Description Analysis

### AI JD Analyzer

The JD Analyzer extracts structured hiring requirements from the job description.

Current extracted fields include:

* `role`
* `minimum_experience_years`
* `required_skills`
* `preferred_skills`
* `critical_skills`
* `education_requirements`
* `certification_requirements`

### Requirement Categories

#### Required Skills

Skills explicitly required by the JD.

Examples:

* Python
* FastAPI
* SQL
* REST APIs
* Docker
* AWS
* Git

#### Preferred Skills

Skills described as preferred, bonus, nice-to-have, desirable, etc.

#### Critical Skills

Skills explicitly identified as mandatory, essential, core, or critical.

Critical skills are also expected to be present in the required-skills set.

---

## 3. Resume Analysis

### Resume Analyzer Agent

The Resume Analyzer extracts factual information from the resume and compares the resume evidence against the JD requirements.

The analyzer is instructed not to invent:

* experience
* skills
* projects
* education
* certifications
* email
* phone
* proficiency

It also does not perform the final score/risk/hiring decision.

### Candidate Information Extracted

The workflow can extract:

* Candidate name
* Email
* Phone
* Relevant experience
* Education
* Certifications
* Python proficiency
* Primary background
* Alternative role fit

---

## 4. Skill Evidence Audit

The Resume Analyzer creates a `skill_audit` entry for each required and preferred skill.

Each entry contains:

```text
{
  "skill": "Python",
  "status": "MATCHED",
  "evidence": "Python is explicitly listed in the candidate's technical skills."
}
```

### Supported Statuses

* `MATCHED`
* `PARTIAL`
* `MISSING`

### MATCHED

Used when the resume provides explicit evidence of the skill.

### PARTIAL

Used for limited, basic, short-term, or clearly incomplete exposure.

### MISSING

Used when there is no meaningful evidence of the skill in the resume.

The workflow does not infer one technology from another.

Examples:

* Node.js does not mean Python
* Express does not mean FastAPI
* Docker does not mean Kubernetes
* AWS does not mean Azure
* PostgreSQL does not automatically mean SQL without supporting database/SQL evidence

---

## 5. Deterministic Scoring

The final score is calculated in the JavaScript Code node rather than relying on the AI model to calculate it.

### Current Scoring Weights

| Metric           |  Weight |
| ---------------- | ------: |
| Required Skills  |      50 |
| Experience       |      25 |
| Critical Skills  |      15 |
| Preferred Skills |      10 |
| **Total**        | **100** |

### Required Skill Score

* MATCHED = 1 point
* PARTIAL = 0.5 point
* MISSING = 0 points

The resulting score is normalized against the total required skills and weighted to 50 points.

### Experience Score

Experience is compared against the minimum experience requirement from the JD.

The score is capped at the maximum experience weight.

### Critical Skill Score

* MATCHED = 1 point
* PARTIAL = 0.5 point
* MISSING = 0 points

The result is weighted to 15 points.

### Preferred Skill Score

* MATCHED = 1 point
* PARTIAL = 0.5 point
* MISSING = 0 points

The result is weighted to 10 points.

If no preferred skills are specified, the preferred bucket receives its full weight.

---

## 6. Recommendation Logic

The workflow currently uses the following decision thresholds:

| Overall Score | Recommendation |
| ------------: | -------------- |
|           85+ | Strong Hire    |
|         70–84 | Interview      |
|         55–69 | Hold           |
|      Below 55 | Reject         |

Critical skill gaps have additional impact.

Current logic:

* 2 or more critical skills missing → Reject / High Risk
* 1 critical skill missing:

  * score >= 65 → Interview / Medium Risk
  * score < 65 → Reject / High Risk
* No critical gaps:

  * 85+ → Strong Hire / Low Risk
  * 70–84 → Interview / Medium Risk
  * 55–69 → Hold / Medium Risk
  * below 55 → Reject / High Risk

---

## 7. HR Decision Summary

The workflow automatically generates a concise HR-oriented summary using:

* matched skills
* partial skills
* missing skills
* experience vs. requirement
* overall score
* recommendation
* critical skill gaps

Example:

```text
Strong evidence in Python, FastAPI, SQL, REST APIs, Docker, AWS.
Key gaps include Git.
5 years of relevant experience against a 5-year requirement.
Overall alignment score is 88%.
The candidate shows strong alignment with core requirements.
```

---

## 8. Interview Questions

The Resume Analyzer generates up to 5 interview questions.

Questions focus on:

* real project experience
* technical depth
* important skill gaps
* practical implementation
* troubleshooting
* architecture

The final JavaScript node formats the questions for the final output.

---

## 9. Final Output

The current Google Sheets output contains the main candidate evaluation fields:

| Field               |
| ------------------- |
| Candidate           |
| Email               |
| Phone               |
| Experience          |
| Education           |
| Matched Skills      |
| Missing Skills      |
| Match %             |
| Overall Score       |
| Risk                |
| Recommendation      |
| HR Summary          |
| Interview Questions |
| Status              |
| Reviewed On         |

Additional internal evaluation fields are generated before the final sheet append step.

---

## 10. Example Evaluation

A candidate with:

* 5 years of relevant experience
* Python
* FastAPI
* SQL
* REST APIs
* Docker
* AWS
* missing Git

can receive an evaluation similar to:

```text
Matched Skills:
Python, FastAPI, SQL, REST APIs, Docker, AWS

Missing Skills:
Git

Experience:
5 Years

Overall Score:
88

Risk:
Low

Recommendation:
Strong Hire
```

The exact score depends on the configured JD requirements and evidence returned by the Resume Analyzer.

---

## 11. Current Architecture Principle

The project intentionally separates AI extraction from deterministic business logic.

```text
AI
↓
Extract facts + evidence
↓
JavaScript
↓
Calculate score + risk + recommendation
↓
Google Sheets
```

This makes the scoring logic more predictable and easier to modify without asking the AI model to make numerical decisions.

---

## 12. Current Status

**Status: Working / In Progress**

The core resume screening workflow is operational and has been tested with multiple candidate profiles.

The current implementation includes:

* JD requirement extraction
* resume evidence extraction
* required/preferred/critical skill evaluation
* deterministic scoring
* experience scoring
* risk assessment
* hiring recommendation
* HR summary
* interview questions
* Google Sheets output

Further polishing, edge-case testing, and future production improvements can be added separately without changing the core workflow.

---

## Tech Stack

* n8n
* OpenAI Chat Model
* n8n AI Agent
* Structured Output Parser
* JavaScript
* PDF extraction
* Google Sheets

---

## Project Goal

Build a practical AI-powered recruitment automation that can reduce manual resume screening effort while keeping the final scoring and decision logic deterministic and transparent.

```
```
