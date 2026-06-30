# AI-Powered SQL Interview Question Generator

## Overview

This project is an AI-powered automation workflow built with Zapier, Google Forms, Google Sheets, Google AI Studio Gemini, and Gmail.

The automation allows users to submit a SQL topic and difficulty level through a form. Once submitted, the workflow generates a customized SQL interview question, answer, explanation, and common mistake using Gemini. The result is saved back into Google Sheets and emailed automatically to the user.

Form link: https://forms.gle/GKusAt1gRUTHYJRB9 

<img width="1536" height="1024" alt="AI-Powered SQL Interview Question Generator" src="https://github.com/user-attachments/assets/2e704dcc-1689-40da-8077-4897769b7170" />


---

## Problem Statement

Many job seekers struggle to practice SQL consistently. They often need interview-style questions that are tailored to specific topics and difficulty levels.

This automation solves that problem by generating SQL practice questions on demand and delivering them instantly by email.

---

## Tools Used

- Google Forms
- Google Sheets
- Zapier
- Google AI Studio Gemini
- Gmail

---

## Workflow

```text
Google Form Submission
        ↓
Google Sheets New Spreadsheet Row Trigger
        ↓
Gemini Generates SQL Interview Practice Content
        ↓
Google Sheets Updates the Original Row
        ↓
Gmail Sends the Practice Question to the User
```
---
## Automation Steps 

### 1. Create Google Form

The form collects:

- Name
- Email
- SQL Topic
- Difficulty Level

Example SQL topics:

- Joins
- Group By
- Window Functions
- CTEs
- Subqueries

<img width="1241" height="930" alt="image" src="https://github.com/user-attachments/assets/6413d234-24ca-4941-9502-bdbc4f6eae43" />

---

### 2. Connect Google Form to Google Sheets

Each form submission creates a new row in Google Sheets.

Initial columns:

- Timestamp
- Name
- Email
- SQL Topic
- Difficulty

Additional AI output columns:

- AI Response
- AI Question
- AI Answer
- AI Explanation

<img width="559" height="72" alt="image" src="https://github.com/user-attachments/assets/7b3cf66f-6229-4f87-a7ca-d9930a4e45e5" />

---

### 3. Create Zapier Workflow

Zapier was used to connect all apps into one automated workflow.

#### Trigger

- Google Sheets → New Spreadsheet Row

#### Actions

- Google AI Studio Gemini → Generate SQL content
- Google Sheets → Update Spreadsheet Row
- Gmail → Send Email

<img width="809" height="936" alt="image" src="https://github.com/user-attachments/assets/13080d01-b50a-491a-857e-86ae0e581b55" />

---

### 4. Generate SQL Content with Gemini

Gemini receives the SQL topic and difficulty level from the form submission.

#### Prompt Used

```text
Generate one SQL interview practice question.

Topic: {{SQL Topic}}
Difficulty: {{Difficulty}}

Return:
1. SQL Interview Question
2. SQL Answer
3. Step-by-Step Explanation
4. Common Mistake

Keep explanations beginner friendly.
```

<img width="363" height="705" alt="image" src="https://github.com/user-attachments/assets/921d2b2a-6a9e-4d59-975e-d065877b9ab5" />

---

### 5. Save AI Output Back to Google Sheets

The Gemini response is saved into the same Google Sheets row as the original form submission.

This creates a growing SQL practice question bank.

<img width="1298" height="763" alt="image" src="https://github.com/user-attachments/assets/3aec85c8-e69a-4767-acc6-02c66da99436" />

---

### 6. Send Email Automatically

Gmail sends the generated SQL practice question to the email submitted in the form.

<img width="373" height="558" alt="image" src="https://github.com/user-attachments/assets/0307235b-f2f7-4061-88b6-29e6e4d369d7" />

Email 1

<img width="1621" height="798" alt="image" src="https://github.com/user-attachments/assets/f0a5df44-a706-475b-a280-6d84ff3fc533" />

Email 2

<img width="1623" height="804" alt="image" src="https://github.com/user-attachments/assets/31694565-8909-4285-9e30-d4b9cca886b2" />

Email 3

<img width="1617" height="798" alt="image" src="https://github.com/user-attachments/assets/c5609241-b40b-4cbb-9740-4b973df7139c" />


---

## What Worked

- Google Forms and Google Sheets worked smoothly as the input and storage layer.
- Zapier made it easy to connect the tools visually without writing code.
- Google AI Studio Gemini worked well after creating an API key.
- Gmail successfully sent the generated SQL practice question to the user.

---

## What Did Not Work Initially

- OpenAI in Zapier required separate API billing, even though I had access to ChatGPT. Because of this, I switched to Google AI Studio Gemini.
- Gemini also required an API key setup, but once connected, it worked successfully.

---

## Use Cases for Data Analysts

This workflow can be adapted for:

- SQL interview practice generation
- Daily SQL challenge emails
- Automated learning content creation
- Candidate screening question generation
- Analytics training programs
- Internal data team upskilling

---

## Use Cases for Product Analysts

This automation can support:

- User onboarding quizzes
- Personalized learning paths
- Skill-based content recommendations
- Product education workflows
- User engagement campaigns
- Automated feedback loops

---

## Key Learning

This project showed how automation can combine user input, AI generation, structured data storage, and email delivery into one complete workflow. It also demonstrates how data analysts can use no-code automation tools to build practical internal tools without needing a full software development stack.

---
## Note on AI Integration

The workflow was originally designed to generate dynamic SQL interview questions using Google AI Studio (Gemini) inside Zapier. During final testing, the Gemini API free-tier quota became exhausted, which temporarily prevented additional live AI responses from being generated through the API integration. To preserve the complete end-to-end automation workflow for demonstration and testing purposes, a static SQL response was temporarily used in place of the live AI-generated output.

Despite the API limitation, the automation logic and workflow architecture were fully implemented and successfully tested, including:

- Google Form submission
- Google Sheets trigger
- Automated workflow execution in Zapier
- Spreadsheet row updates
- Automated email delivery

The workflow remains fully structured for future reconnection to a live AI model once API quota access is restored.

---

## Final Outcome

A working AI-powered SQL interview question generator that:

- Collects user input
- Generates SQL practice content with AI
- Saves the output to a database
- Sends the result by email
- Creates a reusable SQL question bank

