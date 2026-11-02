AI News Telegram Agent

An automated AI agent built with n8n that fetches the latest news every morning, summarizes it using Google Gemini, and delivers it to a Telegram channel at 8:00 AM, with no manual work.

What it does
Runs automatically every day at 8:00 AM (scheduled trigger)
Fetches the latest news from [ RSS feed ]
Uses Google Gemini to summarize and format the news into a clean, readable digest
Sends the digest to a Telegram channel using the Telegram Bot API (HTML formatting)
Workflow
Schedule Trigger (8 AM)
        ↓
Fetch latest news
        ↓
Gemini AI (summarize + format)
        ↓
Telegram (send message to channel)

Workflow screenshot

Tech stack
Part	Tool
Automation / orchestration	n8n (self-hosted, local)
AI model	Google Gemini API
Delivery	Telegram Bot API
Scheduling	n8n Schedule Trigger
How to run it yourself
Install n8n locally (Docker or npm)
In n8n, go to Workflows → Import from File and select workflow.json
Add your own credentials:
Google Gemini API key (free key from Google AI Studio)
Telegram Bot token (create a bot via @BotFather)
Replace YOUR_CHAT_ID in the Telegram node with your channel or chat ID
Activate the workflow

Credentials are not included in this repo. You need to add your own.

What I learned
Building a scheduled, end-to-end automation workflow in n8n
Connecting an LLM (Gemini) into a real pipeline and shaping its output with prompts
Working with the Telegram Bot API and HTML message formatting
Keeping API keys and tokens out of version control
Future improvements
 Web archive of past news digests
 News categories (tech, sports, business) that subscribers can choose from
 Duplicate news removal and source links in each item
 Hindi / English language option
 Move from local n8n to cloud hosting so it runs 24/7
Demo
Telegram channel: (https://t.me/krishnabhola26)
 
Author
