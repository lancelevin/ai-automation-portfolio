# AI Automation Portfolio

A focused portfolio of AI-powered automation projects demonstrating workflow orchestration, LLM integration, Retrieval-Augmented Generation (RAG), API integration, business process automation, and human-in-the-loop systems.

---

# Featured Project

## RAG Support Assistant

AI-powered internal knowledge assistant built with n8n, Retrieval-Augmented Generation (RAG), Slack, Qdrant, Google Drive, Airtable, Google Gemini, and Anthropic Claude.

The system ingests approved company documents, retrieves relevant business knowledge, generates grounded answers, handles conversational follow-ups, and escalates unsupported requests to a human reviewer.

### Key Capabilities

- Automated document ingestion
- PDF text extraction
- Recursive text chunking
- Embedding generation
- Qdrant vector search
- Retrieval-Augmented Generation
- Conversational follow-up rewriting
- Grounded answer generation
- Source attribution
- Human-in-the-loop escalation
- Airtable case logging
- Slack thread handling
- Escalation state tracking

### Architecture

Google Drive Knowledge Base  
→ Document Ingestion  
→ Text Extraction  
→ Chunking  
→ Embeddings  
→ Qdrant Vector Database  
→ Slack Question  
→ Conversation-Aware Retrieval  
→ LLM Answerability Check  
→ Grounded Answer / Human Escalation

### Tech Stack

`n8n` · `RAG` · `Qdrant` · `Google Gemini` · `Anthropic Claude` · `Slack` · `Airtable` · `Google Drive` · `JavaScript` · `REST APIs`

[View RAG Support Assistant →](./01-rag-support-assistant/)

---

# Additional Projects

## AI Lead Capture Bot

AI-powered lead qualification workflow that receives inbound leads through a webhook, uses Claude to summarize and classify them, stores structured lead data in Airtable, and sends automated email notifications.

**Workflow:**  
Webhook → Claude → Airtable → Email Notification

**Tech:** `n8n` · `Anthropic Claude` · `Airtable` · `SMTP` · `REST API`

[View AI Lead Capture Bot →](./02-ai-lead-capture-bot/)

---

## AI Customer Support Agent

Conversational customer support automation that receives customer inquiries through Telegram, generates business-specific responses using Claude, and automatically replies to the customer.

**Workflow:**  
Telegram → Claude → Telegram Response

**Tech:** `n8n` · `Anthropic Claude` · `Telegram Bot API` · `REST API`

[View AI Customer Support Agent →](./03-ai-customer-support-agent/)

---

# Focus Areas

- AI Automation
- Workflow Orchestration
- Retrieval-Augmented Generation
- LLM Integration
- API Integration
- Vector Databases
- Conversational AI
- Human-in-the-Loop Systems
- Business Process Automation

---

## Architecture Diagram

![RAG Support Assistant Architecture](./docs/architecture.png)

---

## Repository Structure

```text
ai-automation-portfolio/
├── 01-rag-support-assistant/
├── 02-ai-lead-capture-bot/
├── 03-ai-customer-support-agent/
└── README.md
