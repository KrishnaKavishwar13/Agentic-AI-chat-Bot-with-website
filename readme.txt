Agentic AI Web Chatbot

An Agentic AI chatbot integrated into a website using n8n for workflow orchestration and Google Gemini API for language intelligence.

Overview

This project demonstrates an agent-based chatbot system where:

The website collects user input

n8n manages workflow logic

Gemini API generates responses

The system returns structured output to the frontend

Architecture flow:

User → Website → n8n Webhook → Gemini API → n8n Processing → Website

Tech Stack

Frontend: HTML, CSS, JavaScript

Workflow Automation: n8n

Language Model: Google Gemini API

Communication: REST API

Setup
1. Clone Repository
git clone https://github.com/your-username/agentic-ai-chatbot.git
cd agentic-ai-chatbot
2. Run n8n

Using npm:

npm install n8n -g
n8n

Using Docker:

docker run -it --rm -p 5678:5678 n8nio/n8n

Open:

http://localhost:5678
3. Configure Gemini API

Generate API key from Google AI Studio

Add key in n8n credentials

Use HTTP Request node to call Gemini endpoint

4. Connect Frontend

Example:

fetch("YOUR_N8N_WEBHOOK_URL", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
  body: JSON.stringify({ message: userMessage })
})
.then(res => res.json())
.then(data => console.log(data));
Features

Real-time AI responses

Agentic workflow logic

Extendable API integration

Lightweight frontend

Project Structure
agentic-ai-chatbot/
│
├── index.html
├── style.css
├── script.js
├── n8n-workflow.json
└── README.md
