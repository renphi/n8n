# 🔄 Automate with n8n and AI

## Goal

In this repository, you'll find examples of how to use [n8n](https://n8n.io/) with AI capabilities to build powerful automations.

## Included Workflows

### 📰 Web Scraping and Summarization Workflow

This workflow:
- Scrapes the latest Paul Graham essays from his website
- Extracts the text content
- Uses OpenAI's GPT model to generate concise summaries
- Returns the titles, summaries, and URLs

## Prerequisites

- [Docker](https://www.docker.com/) installed and running
- [n8n Docker Compose setup](https://docs.n8n.io/hosting/installation/docker/) (included in this repo)
- OpenAI API key for the summarization workflow

## Getting Started

1. Start n8n locally:
```bash
docker-compose up -d
```
n8n will be available at: [http://localhost:5678](http://localhost:5678)

2. Import the workflow in `Scrape_and_summarize_webpages_with_AI.json`

3. Configure your OpenAI API key in the credentials section

4. Run the workflow to fetch and summarize the latest essays

## Customization Ideas

- Modify the workflow to scrape different websites
- Change the OpenAI model or customize the prompts
- Add notification outputs (Slack, email, etc.)
- Schedule the workflow to run periodically