# AI Lead Capture Bot

AI-powered lead capture and qualification workflow built with n8n, Claude, Airtable, and email automation.

## Problem

Businesses often receive inbound leads through forms or webhooks, but manually reviewing, qualifying, summarizing, and notifying the sales team creates unnecessary work.

## Solution

This workflow automatically:

- receives a new lead through a webhook
- sends the lead information to Claude
- summarizes and classifies the lead as Hot, Warm, or Cold
- stores the structured lead information in Airtable
- sends an email notification to the business owner

## Workflow

Webhook  
→ Claude Lead Qualification  
→ Airtable Lead Record  
→ Email Notification

## Tech Stack

- n8n
- Anthropic Claude
- Airtable
- SMTP / Email
- REST API
- JSON

## Workflow File

The sanitized n8n workflow export is available here:

`workflow.json`

## Security

The public workflow export has been sanitized and does not contain:

- API keys
- credential bindings
- private webhook URLs
- Airtable account IDs
- personal email addresses
- production secrets

## Status

Portfolio prototype demonstrating AI-assisted lead qualification and business workflow automation.
