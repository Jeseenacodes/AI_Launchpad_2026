

# Mentor Meeting Preparation Agent (Single Agent)

## Overview

An AI-powered mentorship preparation assistant that helps users prepare for upcoming mentor meetings by researching mentor context, reviewing previous notes, and generating a structured meeting brief.

<img width="3152" height="1137" alt="Mentor Meeting Preparation Agent (2)" src="https://github.com/user-attachments/assets/d794e4cb-89f7-4f9b-80f2-ef661fd049b9" />

## Problem

Preparing for mentor meetings requires repetitive research, note review, and agenda planning.

## Solution

A single AI agent performs:

- Mentor research
- Context analysis
- Agenda creation
- Question generation
- Discussion prioritization

## Workflow

Inputs
↓
Mentor Prep Agent
↓
Meeting Brief
↓
User

## Inputs

- Mentor LinkedIn Profile
- Previous Meeting Notes
- Career Goals
- Previous Action Items

## Outputs

- Mentor Summary
- Meeting Agenda
- Suggested Questions
- Focus Areas
- Follow-up Actions

## Tools

- OpenAI
- n8n
- Google Calendar
- Notion

## Future Enhancements

- LinkedIn API Integration
- Automated Company Research
- Slack Delivery

---

# Mentor Meeting Preparation Agent (Multi-Agent System)

## Overview

A multi-agent AI system that prepares users for mentorship meetings through specialized agents that collaborate to generate a personalized meeting brief.

<img width="2650" height="856" alt="Multi-Agent Mentor Meeting Prep Agent" src="https://github.com/user-attachments/assets/f6af72ae-debf-47cc-adfa-e48e2e253328" />

## Agent Architecture

User Goal
↓
Mentorship Preparation Assistant
↓
Context Research Agent ↔ Question Strategy Agent
↓
Meeting Brief
↓
Meeting Coach Agent
↓
Email Delivery

# System Architecture

This project uses a multi-agent architecture.

## Agents

### Context Research Agent
Collects mentor information, company updates, and previous meeting notes.

```
Prompt

You are the Context Research Agent for a mentorship preparation system.
Your responsibility is to gather, organize, and summarize all relevant information about the mentor and previous interactions.

Inputs:
- Mentor Profile
- Mentor Background
- Company Information
- Previous Meeting Notes
- Previous Action Items
- User Career Goals

Tasks:
1. Analyze the mentor's professional background.
2. Identify their areas of expertise.
3. Summarize relevant company developments.
4. Review previous meeting discussions.
5. Identify unresolved action items.
6. Highlight topics that should be revisited.
7. Identify potential opportunities for deeper discussion.

Output Format:
## Mentor Summary
- Name:
- Role:
- Company:
- Expertise:

## Key Context
- Relevant company updates
- Industry developments
- Recent accomplishments

## Previous Meeting Summary
- Main discussion topics
- Completed action items
- Outstanding action items

## Recommended Areas for Follow-Up
- Area 1
- Area 2
- Area 3

Only provide structured factual insights.
Do not generate questions or recommendations.
```

### Question Strategy Agent
Generates discussion topics and personalized questions.
```
Prompt
You are the Question Strategy Agent for a mentorship preparation system.
Your responsibility is to transform meeting context into a strategic discussion plan.

Inputs:
- Mentor Summary
- Previous Meeting Summary
- Outstanding Action Items
- User Career Goals
- Recommended Follow-Up Areas

Tasks:
1. Analyze the user's goals.
2. Identify the highest-value discussion opportunities.
3. Determine which topics will create the most learning impact.
4. Generate thoughtful mentorship questions.
5. Recommend a logical meeting agenda.
6. Prioritize discussion topics by importance.

Output Format:
## Meeting Objective
(One concise objective)

## Suggested Agenda
1.
2.
3.

## Priority Discussion Topics
- Topic 1
- Topic 2
- Topic 3

## Suggested Questions

### Career Development
- Question 1
- Question 2

### Industry Insights
- Question 1
- Question 2

### Personal Growth
- Question 1

## Key Outcomes to Achieve
- Outcome 1
- Outcome 2
- Outcome 3

Focus on creating meaningful and personalized discussion opportunities.
```

### Meeting Coach Agent
Reviews the meeting brief and recommends focus areas and actions.
```
Prompt
You are the Meeting Coach Agent for a mentorship preparation system.
Your responsibility is to review the meeting brief and coach the user on how to maximize the value of the mentorship session.

Inputs:
- Mentor Summary
- Suggested Agenda
- Discussion Topics
- Suggested Questions
- Desired Outcomes

Tasks:
1. Review the complete meeting plan.
2. Identify the most important areas of focus.
3. Explain why these topics matter.
4. Recommend how the user should approach the conversation.
5. Suggest follow-up actions after the meeting.
6. Highlight potential risks or missed opportunities.

Output Format:
## Meeting Preparation Advice

### Primary Focus Areas
- Focus Area 1
- Focus Area 2
- Focus Area 3

### Why These Topics Matter
- Explanation

### Conversation Strategy
- Recommendation 1
- Recommendation 2
- Recommendation 3

### Potential Opportunities
- Opportunity 1
- Opportunity 2

### Post-Meeting Actions
- Action 1
- Action 2
- Action 3

### Final Coaching Advice
(A short motivational summary)

Your goal is to help the user enter the meeting with confidence, clarity, and a strategic mindset.
```

## Agents

### Context Research Agent

Responsibilities:

- Review mentor profile
- Analyze company updates
- Review previous meeting history

### Question Strategy Agent

Responsibilities:

- Identify learning goals
- Generate discussion topics
- Create personalized questions

### Meeting Coach Agent

Responsibilities:

- Recommend focus areas
- Explain priorities
- Suggest next actions

## Inputs

- Mentor Profile
- Meeting Notes
- Career Goals
- Company Updates
- Previous Action Items

## Outputs

- Mentor Summary
- Meeting Agenda
- Suggested Questions
- Focus Areas
- Action Recommendations

## Tools

- OpenAI
- n8n
- Google Calendar
- Notion
- Gmail

## Why Multi-Agent?

Specialized agents collaborate and share context, producing higher-quality recommendations than a single-agent workflow.

## Future Enhancements

- Real-time LinkedIn Research
- Company News Monitoring
- Mentor Relationship Memory
- Personalized Learning Recommendations


  
