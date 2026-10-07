# RAG Support Assistant

AI-powered employee support assistant built with n8n, Retrieval-Augmented Generation (RAG), Slack, Airtable, Google Drive, Qdrant, Gemini, and Anthropic Claude.

The system answers employee questions using approved company knowledge, rewrites follow-up questions for better retrieval, returns grounded answers with source metadata, and escalates unsupported requests to a human reviewer.

## Problem

Internal teams often waste time answering repetitive questions that are already documented in company policies, handbooks, and operational guides.

This project automates first-line support while avoiding hallucinated company answers.

## Solution

The assistant:

- ingests approved business documents
- chunks and embeds document content
- stores embeddings in a vector database
- receives employee questions through Slack
- rewrites conversational follow-ups into standalone retrieval questions
- retrieves relevant business knowledge
- generates grounded answers using only retrieved context
- appends source metadata
- escalates unsupported questions to a human
- logs escalation cases in Airtable

## Architecture

The project is split into three modular n8n workflows.

### 1. Knowledge Ingestion

Google Drive  
→ PDF extraction  
→ metadata normalization  
→ recursive text splitting  
→ embeddings  
→ Qdrant vector database

### 2. Slack RAG Assistant

Slack mention  
→ thread context retrieval  
→ follow-up question rewriting  
→ vector search  
→ retrieval context assembly  
→ LLM answerability check  
→ grounded response

### 3. Human Escalation

Unsupported question  
→ escalation payload  
→ Airtable case creation  
→ case tracking  
→ Slack human review notification

## Retrieval Strategy

Documents are split using recursive character chunking.

- Chunk size: `800`
- Chunk overlap: `150`

Document metadata is preserved for retrieval and source attribution.

## Hallucination Control

The answer model is instructed to use only retrieved business knowledge for company-specific facts.

If the retrieved context is insufficient, ambiguous, or unsupported, the workflow returns:

`ESCALATE`

instead of generating an unsupported answer.

## Conversation Handling

Slack thread history is retrieved and used to understand conversational references.

Follow-up questions such as:

`What about sick leave?`

can be rewritten into standalone retrieval queries before vector search.

## Human Escalation

When the RAG system cannot confidently answer a question:

1. an escalation case is created
2. the case is logged in Airtable
3. the Slack thread is marked as escalated
4. a human reviewer is notified
5. follow-up messages related to the existing case are routed back to the human reviewer

## Tech Stack

- n8n
- Retrieval-Augmented Generation (RAG)
- Qdrant Vector Database
- Google Gemini Embeddings
- Google Gemini LLM
- Anthropic Claude
- Slack API
- Airtable API
- Google Drive
- JavaScript
- JSON
- REST APIs

## Workflow Files

The sanitized n8n workflow exports are available in:

`workflows/`

- `01-knowledge-ingestion.json`
- `02-slack-rag-assistant.json`
- `03-human-escalation.json`

## Security

Public workflow exports have been sanitized.

The repository does not include:

- API keys
- OAuth tokens
- private webhook URLs
- credential bindings
- internal account identifiers
- production environment secrets

## Status

Prototype / portfolio implementation focused on demonstrating RAG architecture, workflow orchestration, conversational retrieval, grounded answer generation, and human-in-the-loop escalation.
