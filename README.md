# 🤖 n8n AI Resume Screening & Shortlisting Agent

An automated end-to-end recruitment pipeline built using **n8n**, **Google Gemini**, and **Google Drive/Sheets APIs**. This system automatically extracts candidate data from incoming resume attachments (`.docx` / `.pdf`), evaluates candidate qualifications using AI, dynamically sends conditional email notifications (Shortlisted vs Rejected), and logs structured records into Google Sheets.

## 🚀 Features

- **Automated Resume Ingestion:** Triggers automatically on incoming emails with attached resumes via Gmail API.
- **Dynamic File Conversion:** Handles `.docx` files via Google Drive REST API conversion (`files.copy`) to ensure error-free text extraction.
- **AI-Powered Candidate Evaluation:** Uses Google Gemini Chat Model with Structured Output Parsers to extract candidate metrics (Name, Email, Skills, Experience, Candidate Score).
- **Conditional Email Routing:** 
  - **Shortlisted Candidates:** Receives a personalized congratulatory email.
  - **Rejected Candidates:** Receives a polite application status update.
- **Centralized Record Keeping:** Appends evaluation metrics directly into Google Sheets.

## 🛠️ Tech Stack

- **Automation:** n8n (Self-Hosted)
- **AI Models:** Google Gemini Chat Model & Structured Output Parser
- **Integrations:** Gmail API, Google Drive API, Google Sheets API
- **Logic Nodes:** IF Node, Switch Node, HTTP Request Node

## 📦 How to Use / Setup

1. **Clone/Import Workflow:** Download the `workflow.json` file from this repository and import it into your n8n instance.
2. **Credentials:** Set up OAuth2 credentials for:
   - Gmail API
   - Google Drive OAuth2 API
   - Google Sheets API
   - Google Gemini API Key
3. **Configure Sheets & Email:** Map your Google Sheet ID and update the email templates inside the Gmail nodes.
4. **Activate:** Toggle the workflow to **Active** to begin processing live applications automatically!
