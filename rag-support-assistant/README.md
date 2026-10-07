# RAG Support Assistant

AI-powered employee support assistant built with n8n, RAG, Slack, Airtable, and LLM APIs.

The system answers employee questions using company knowledge, supports follow-up questions, and escalates unanswered or low-confidence requests to a human.

## Architecture

The project is split into three workflows:

1. Knowledge Ingestion
2. RAG Query & Response
3. Human Escalation / Follow-up

## Core Technologies

- n8n
- Retrieval-Augmented Generation (RAG)
- Vector Database
- Embeddings
- LLM API
- Slack
- Airtable
- Google Drive

## Workflow Files

The exported n8n workflows are stored inside the `workflows/` directory.
