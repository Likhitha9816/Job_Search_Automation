# AI Job Search Automation

Automated daily job search pipeline built with n8n.

## What it does
- Fetches 80+ AI Engineer jobs daily from JSearch API
- Filters out staffing agencies and wrong experience levels
- Scores each job against my profile using GPT-4o-mini
- Saves top 15 jobs to Google Sheets
- Sends daily HTML email with apply links at 6am

## Tech Stack
- n8n (automation)
- JSearch API via RapidAPI
- OpenAI GPT-4o-mini (job scoring)
- Google Sheets (tracking)
- Gmail (daily digest)

## How to use
1. Import the workflow JSON into n8n
2. Add your API keys (JSearch, OpenAI)
3. Connect Gmail and Google Sheets
4. Activate the workflow

## Workflow
Schedule Trigger → HTTP Request → Code (filter) → OpenAI (score) → Code (top 15) → Google Sheets → Aggregate → Gmail
