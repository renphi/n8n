
# 🔄 Automate with n8n and a Local AI Agent

## Goal

In this module, you'll learn how to use [n8n](https://n8n.io/) in combination with a local LLM (via Ollama) and [LangChain](https://www.langchain.com/) to build a simple AI-powered automation.

You’ll create a small automation pipeline that:
- Receives a support ticket
- Summarizes it using a local LLM via LangChain
- Sends a Slack message or email with the summary

## Prerequisites

- [Docker](https://www.docker.com/) installed and running
- [n8n Docker Compose setup](https://docs.n8n.io/hosting/installation/docker/) (included in this repo)
- [Ollama](https://ollama.com/) running locally

```bash
ollama pull mistral:latest
```

## Challenge

1. Start n8n locally:
```bash
docker-compose up -d
```
n8n will be available at: [http://localhost:5678](http://localhost:5678)

2. Import the workflow in `support_summary_workflow.json`

3. Review the following nodes:
- 📨 HTTP Trigger: receives ticket data
- 🧠 LangChain Node (local model via Ollama): summarizes the message
- 🔁 Responds with summary (or sends via webhook/email)

4. Your Task:
- Open the **LangChain node** and adjust the **prompt** to produce clean, bullet-point summaries.
- Optional: Add a field that highlights urgency or customer mood.

## Bonus

- Add conditional routing based on sentiment or topic
- Log all outputs to a Google Sheet or database
