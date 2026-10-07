# AI Customer Support Agent

AI-powered customer support assistant built with n8n, Telegram, and Anthropic Claude.

## Problem

Small businesses often spend time repeatedly answering the same questions about pricing, booking policies, services, and availability.

## Solution

This workflow automatically:

- receives customer messages through Telegram
- sends the message to Claude
- generates a business-specific response
- returns the response directly to the customer

The assistant follows predefined business information and policies to provide consistent answers.

## Workflow

Telegram Message  
→ Claude Support Assistant  
→ Telegram Response

## Tech Stack

- n8n
- Anthropic Claude
- Telegram Bot API
- REST API
- JSON

## Workflow File

The sanitized n8n workflow export is available here:

`workflow.json`

## Security

The public workflow export has been sanitized and does not contain:

- API keys
- Telegram bot tokens
- credential bindings
- private webhook IDs
- production secrets

## Status

Portfolio prototype demonstrating conversational AI and customer support automation.
