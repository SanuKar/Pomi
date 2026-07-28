# Pomi Architecture

## Overview

Pomi is an AI workspace built to demonstrate an end-to-end AI engineering pipeline.

## Architecture

User
↓
FastAPI Backend
↓
Application Services
↓
PostgreSQL + ChromaDB
↓
LLM API

## Core Components

### FastAPI
Handles API requests and connects the different parts of Pomi.

### PostgreSQL
Stores structured application data such as:
- Users
- Conversations
- Messages
- Document information

### LLM
Provides AI-generated responses to user questions.

### RAG
Retrieves relevant information from uploaded documents before sending context to the LLM.

### ChromaDB
Stores document embeddings and performs similarity search.

### Docker
Packages Pomi and its dependencies so the application can run consistently across environments.

## Pomi v1 Flow

User Question
↓
FastAPI
↓
Retrieve Relevant Context
↓
LLM
↓
Generate Response
↓
Save Conversation
↓
Return Response to User