<img width="2560" height="1747" alt="image" src="https://github.com/user-attachments/assets/56b7179c-f780-4aea-89bc-081d21ea54a3" />

# Project Overview
## This project demonstrates an AI-powered email assistant built using  low-code n8n. 

##### The assistant:
- Monitors incoming emails
- Classifies them into categories (Support, Sales, Transactional, Spam, etc.) using OpenAI GPT
- Drafts human-like responses with AI
- Sends drafts for human review via gotoHuman
- The human can send the final reply via Gmail, modificate it or not send it

This workflow mimics a real-world customer support automation system and showcases end-to-end AI + workflow integration.

##### Tools used:
- n8n – A Low-code Workflow automation platform (open-source)
- API from OpenAI GPT (3.5 / 4) – For AI email classification and draft generation
- API's from Gmail – Email trigger and sending replies
- gotoHuman – Human-in-the-loop review and approval

## Workflow Architecture
<img width="1791" height="618" alt="image" src="https://github.com/user-attachments/assets/7c1f5cfd-8b2a-45f4-8bd2-faf6838aa4a2" />

###### Email Trigger:
- Workflow starts when a new email arrives in Gmail.

###### AI Classification:
- Email content is sent to GPT for classification.
Determines:
- Category (Support, Sales, etc.)
- If a reply is needed
- Importance of the email
###### Routing Logic
Emails are routed based on AI classification and importance:
- Needs reply → Draft created
- Needs review → Sent to human via gotoHuman
- Not important → Ignored

###### Draft Generation
- GPT drafts a human-like response
- Draft is structured for easy review
- Draft is reviewed and approved, rejected, or retried

###### Human Review
<img width="942" height="952" alt="image" src="https://github.com/user-attachments/assets/ba02bd0b-b4ab-4553-8c62-31ad541dbd25" />

###### Send Reply
Approved drafts are sent via Gmail

## Features
- AI classification of emails
- Draft email generation with OpenAI
- Human review with gotoHuman
- Conditional routing based on importance and reply need
- Easy-to-read workflow with structured outputs
- It could be expandable to  notifications, dashboards, excels, whatsapp...

## Importance of this Automation
##### Demonstrates real-world problem solving
Identify a common business challenge (email overload, slow response times)
Design a practical solution that improves efficiency
Companies receive hundreds of emails daily — automating classification and drafting shows business awareness.

##### Shows mastery of modern AI tools
Integrates OpenAI GPT for natural language understanding and generation
Shows you know how to use AI responsibly (human review)

##### Highlights the verification of human
Before sending any answers a human reviews the AI responses

### How to Set UP
###### n8n
Install n8n (local, Docker, or cloud)
Import workflow template JSON

###### Gmail
Create a Gmail OAuth2 credential in n8n
Connect inbox for email triggers

###### OpenAI
Create an API key
Configure GPT model node in n8n 

###### gotoHuman
Create a free account
Create a review template (e.g., “Email Smart Reply”)
Add your API key in the gotoHuman node

##### Run Workflow
Activate the n8n workflow

### Requirements
- gotoHuman account for human supervision
- OpenAI account for classification and email draft
- Gmail for emails
