# AI Internship Applier

## Overview

Applying to multiple internships can be repetitive and time-consuming. Candidates often need to manually draft personalized emails for each opportunity, which reduces productivity and can lead to inconsistent communication.

The AI Internship Applier automates this process using n8n, Google Gemini, Google Sheets, and Gmail.

When a new internship application entry is added to Google Sheets, the workflow automatically generates a professional internship application email using AI and sends it to the hiring manager.

---

## Problem Statement

Students and job seekers often spend significant time:

* Writing similar application emails repeatedly
* Customizing emails for different internship roles
* Managing large numbers of internship applications
* Ensuring professional communication

This workflow automates these repetitive tasks while maintaining personalization.

---

## Solution

The workflow monitors a Google Sheet for new application records.

When a new row is added:

1. Candidate details are fetched.
2. Google Gemini analyzes the information.
3. A professional internship application email is generated.
4. Subject and email body are structured automatically.
5. Gmail sends the email to the hiring manager.

This enables one-click internship outreach.

---

## Workflow Architecture

Google Sheets Trigger
↓
Fetch Candidate Details
↓
Google Gemini
↓
Generate Personalized Email
↓
Structured Output Parser
↓
Gmail
↓
Send Email

---

## Technologies Used

* n8n
* Google Gemini AI
* Google Sheets
* Gmail API
* Prompt Engineering

---

## Input Fields

The workflow expects the following columns inside Google Sheets:

| Column Name        | Description            |
| ------------------ | ---------------------- |
| Full Name          | Applicant Name         |
| Email              | Applicant Email        |
| HiringManagerEmail | Recipient Email        |
| Position Applied   | Internship Role        |
| Details            | Additional Information |
| Experience(Years)  | Relevant Experience    |
| Skills             | Technical Skills       |

---

## How It Works

### Step 1: Google Sheets Trigger

The workflow continuously monitors a Google Sheet.

Whenever a new internship application entry is added, the workflow automatically starts.

### Step 2: AI Email Generation

Google Gemini receives:

* Applicant information
* Internship role
* Skills
* Experience
* Additional details

Using prompt engineering, Gemini generates:

* Professional subject line
* Personalized email body
* Formal closing message

### Step 3: Structured Output

The generated response is converted into a structured format:

* To
* Subject
* Body

This ensures reliable email delivery.

### Step 4: Gmail Automation

The workflow automatically sends the generated email through Gmail to the specified hiring manager.

---

## Example Workflow

Input:

Position Applied: AI Intern

Skills:
Python, Machine Learning, Generative AI

Experience:
1 Year

Output:

Subject:
Application for AI Internship

Email:
A professionally generated internship application email tailored to the role.

---

## Use Cases

* Internship Applications
* Job Applications
* Campus Placements
* Startup Outreach
* Recruitment Campaigns

---

## Setup Instructions

### Import Workflow

1. Download AI-Internship-Applier.json
2. Open n8n
3. Click Import Workflow
4. Upload the JSON file

### Configure Credentials

Connect:

* Google Sheets
* Google Gemini
* Gmail

### Update Sheet

Create the required columns and add applicant information.

### Activate Workflow

Enable the workflow and start adding entries.

---

## Future Improvements

* Resume attachment support
* ATS optimization
* Company-specific personalization
* Multi-language emails
* Email tracking dashboard
* Follow-up email automation

---

## Demo

A complete screencast demonstrating the workflow is available in the demo folder.

---

## Author

Pranav Mahesh Palled

Computer Science & Engineering Student

Interested in Artificial Intelligence, Generative AI, Workflow Automation, and Emerging Technologies.
