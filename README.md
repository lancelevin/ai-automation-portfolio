# AI Automation Portfolio

A collection of AI-powered automation projects focused on workflow orchestration, LLM integration, RAG, APIs, business process automation, and human-in-the-loop systems.

---

# Featured Project

## RAG Support Assistant

AI-powered internal knowledge assistant built with n8n, Retrieval-Augmented Generation (RAG), Slack, Qdrant, Google Drive, Airtable, Gemini, and Anthropic Claude.

The system ingests approved company documents, retrieves relevant knowledge, generates grounded answers, handles conversational follow-ups, and escalates unsupported questions to a human reviewer.

### Key Capabilities

- Document ingestion from Google Drive
- Recursive text chunking
- Embedding generation
- Qdrant vector search
- Retrieval-Augmented Generation
- Conversational follow-up handling
- Grounded answer generation
- Source attribution
- Human-in-the-loop escalation
- Airtable case logging
- Slack integration
- Escalation state tracking

### Architecture

Knowledge Base  
→ Document Ingestion  
→ Chunking  
→ Embeddings  
→ Qdrant Vector Database  
→ Slack Question  
→ Retrieval  
→ LLM Answerability Check  
→ Grounded Response / Human Escalation

### Tech Stack

`n8n` · `RAG` · `Qdrant` · `Google Gemini` · `Anthropic Claude` · `Slack` · `Airtable` · `Google Drive` · `JavaScript` · `REST APIs`

### Project Files

[View the RAG Support Assistant →](./rag-support-assistant/)

---

# Other Projects

## AI Lead Capture Bot

AI-powered lead qualification workflow that receives inbound leads, uses Claude to summarize and classify them, stores structured data in Airtable, and sends automated notifications.

**Workflow:**  
Webhook → Claude → Airtable → Email

**Tech:** `n8n` · `Anthropic Claude` · `Airtable` · `SMTP` · `REST API`

[View Project →](./ai-lead-capture-bot/)

---

## AI Customer Support Agent

Conversational support automation that receives customer inquiries through Telegram, generates business-specific responses using Claude, and replies automatically.

**Workflow:**  
Telegram → Claude → Telegram Response

**Tech:** `n8n` · `Anthropic Claude` · `Telegram Bot API` · `REST API`

[View Project →](./ai-customer-support-agent/)

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
