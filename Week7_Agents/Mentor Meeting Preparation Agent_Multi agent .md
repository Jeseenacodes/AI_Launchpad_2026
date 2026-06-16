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

