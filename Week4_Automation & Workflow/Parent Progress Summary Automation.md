# Parent Progress Summary Automation

## Overview

Parent Progress Summary Automation is a workflow built using Google Forms, Google Sheets, Make.com, and Gmail. The system automatically tracks student learning activity from my educational apps Little Noories, Tamilingo, and Little Readers and sends personalized learning progress summaries to parents. The automation helps simulate how educational platforms can improve parent communication, engagement, and progress tracking using no-code automation tools.

<img width="1280" height="853" alt="image" src="https://github.com/user-attachments/assets/2b6334e8-3101-4118-ac75-65688af5cdb7" />


---

## About the Apps

### Little Noories
An interactive Islamic learning app focused on Quran-inspired stories, Arabic learning, duas, habits, quizzes, and activities for children.

### Tamilingo
A Tamil language learning app designed to help children learn Tamil vocabulary, pronunciation, tracing, and literacy skills through interactive experiences.

### Little Readers
An early literacy app that helps children improve reading confidence through beginner-friendly stories, quizzes, vocabulary activities, and comprehension exercises.

---

## Problem Statement

Educational apps often require consistent parent communication to keep families informed about student progress. Manually creating weekly progress summaries for every learner can become repetitive and time-consuming. This automation streamlines the process by automatically generating personalized learning summaries using form submissions and email workflows.

---

## Tools Used

- Google Forms
- Google Sheets
- Make.com
- Gmail

---

## Workflow

```text
Parent Progress Form Submission
                ↓
Google Sheets Updates Automatically
                ↓
Make.com Watches New Rows
                ↓
Personalized Parent Summary Email Generated
                ↓
Email Sent Automatically

```
<img width="685" height="381" alt="Screenshot 2026-05-13 214136" src="https://github.com/user-attachments/assets/090a4860-67fc-43b6-80d8-ebd43b011e66" />

---

# Automation Steps

## 1. Create Parent Progress Form

A Google Form was created to simulate educational app activity tracking.

The form collects:
* Child Name
* App Name
* Lessons Completed
* Quiz Score
* Vocabulary Learned
* Activities Completed
* Parent Email
* Weekly Progress Notes

<img width="320" height="598" alt="image" src="https://github.com/user-attachments/assets/68c0e50f-d17d-415d-8fde-7565ed8d74c4" />

---

## 2. Connect Google Forms to Google Sheets

Each form submission automatically creates a new row inside Google Sheets. This sheet acts as the student progress tracking database.

<img width="1083" height="153" alt="image" src="https://github.com/user-attachments/assets/460513ff-8e39-4c36-9797-03d245552ede" />

---

## 3. Create Make.com Scenario

Make.com was used to automate the workflow.

Trigger:

* Google Sheets → Watch New Rows

Action:

* Gmail → Send Email

<img width="685" height="381" alt="Screenshot 2026-05-13 214136" src="https://github.com/user-attachments/assets/4cf626c0-3f19-446f-aba6-40449a1d9e81" />

---

## 4. Configure Parent Summary Email

The Gmail module dynamically inserts student progress information from Google Sheets into a personalized email template.

Example email includes:
* Child Name
* App Name
* Lessons Completed
* Quiz Score
* Vocabulary Learned
* Progress Notes

<img width="634" height="867" alt="Screenshot 2026-05-13 213833" src="https://github.com/user-attachments/assets/d04c1aab-9c90-4f8f-8466-8e023f345be0" />


---

## 5. Automated Parent Communication

Whenever a new form response is submitted:
* Google Sheets updates automatically
* Make.com detects the new row
* A personalized learning progress summary is emailed to the parent

<img width="1621" height="239" alt="image" src="https://github.com/user-attachments/assets/9b576d93-b5c7-4052-a153-560055b144b1" />

---

## Example Use Cases

### Little Noories
* Weekly Quran story progress
* Arabic vocabulary updates
* Islamic habit tracking
* Quiz completion summaries

### Tamilingo
* Tamil vocabulary progress
* Pronunciation milestones
* Tracing activity completion
* Quiz performance updates

### Little Readers
* Reading comprehension progress
* Story completion summaries
* Vocabulary growth tracking
* Literacy milestone updates

---

## What Worked
* Google Forms made it easy to simulate app learning activity.
* Google Sheets worked effectively as a lightweight tracking database.
* Make.com successfully automated the workflow.
* Gmail personalization created dynamic parent progress summaries.

---

## What I Would Improve Next

Future improvements could include:
* Weekly scheduled digest emails
* Parent dashboards
* Visual progress charts
* AI-generated encouragement summaries
* Reward badge automation
* Student streak tracking

---

## Key Learning

This project helped me understand how automation can support educational product workflows, user engagement, and parent communication systems without needing a full backend infrastructure. It also demonstrated how no-code tools can simulate scalable educational product operations using structured workflows.

---

## Final Outcome

A working Parent Progress Summary Automation system that:
* Tracks student learning activity
* Stores progress data in Google Sheets
* Automatically generates personalized parent updates
* Sends email summaries using Make.com and Gmail
* Supports engagement workflows for Little Noories, Tamilingo, and Little Readers

---

## Future Improvement — Real App Integration

Currently, the workflow uses Google Forms to simulate learning activity submissions for demonstration purposes. In a production-ready version, the automation could be connected directly to the app backend using platforms such as:

- Firebase
- Supabase
- Airtable
- Custom APIs

This would allow real-time lesson completion data, quiz performance, vocabulary progress, and engagement metrics from the apps to automatically update Google Sheets and trigger parent progress summaries without manual form submissions.

```
```
