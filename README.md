# AI Automation Portfolio

## Project 1 — AI Lead Capture Bot

### What it does
Automatically captures leads, uses Claude AI to qualify 
and summarize them, saves to Airtable, and sends an 
email notification to the business owner.

### Workflow
Webhook → Claude AI → Airtable → Email Notification

### Tools Used
- n8n (workflow automation)
- Claude AI by Anthropic (lead qualification)
- Airtable (database)
- Gmail (email notification)

### How it works
1. A lead submits a form on a website
2. n8n catches the submission via Webhook
3. Claude AI reads the lead data and rates them as Hot, Warm, or Cold
4. The lead is saved to Airtable with AI summary
5. Business owner receives an email notification instantly

### Business Value
Saves business owners hours of manual lead sorting. 
Every lead is automatically qualified by AI within seconds.

## Project 2 — AI Customer Support Agent (Telegram Bot)

### What it does
A Telegram bot powered by Claude AI that automatically 
replies to customer inquiries 24/7 without human intervention.

### Workflow
Telegram Message → n8n → Claude AI → Reply back to Telegram

### Tools Used
- n8n (workflow automation)
- Claude AI by Anthropic (intelligent replies)
- Telegram Bot API (messaging platform)
- ngrok (webhook tunneling for local development)

### Business Value
Businesses save hours of manual DM replies. 
The bot handles FAQs, pricing, bookings, and policies 
instantly — even at 3AM.

### Real World Demo
Built a customized version for "Mani Mami" — a nail salon 
in Fairview, Quezon City — that handles pricing inquiries, 
booking policies, and FAQs in Taglish automatically.
