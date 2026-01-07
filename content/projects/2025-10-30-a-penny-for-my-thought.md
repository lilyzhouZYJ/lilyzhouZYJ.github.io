---
title: "A Penny For My Thought - Journaling App (WIP)"
summary: "AI-powered journaling web app"
tags: ["ML/AI", "personal"]
showTags: true
date: 2025-10-30
---

Journaling is something I’ve tried over and over again during tough days, but I never quite learned how. As someone who's always been reserved and emotionally closed off (I'm working on it!), I struggle to talk about myself honestly and vulnerably, even to the blank pages of my own private journal.

So I thought, maybe turning it into a conversation would make it less daunting.

I started vibe-coding an AI-powered journaling web app, using spec-driven development to make the vibe-coding more efficient. Hopefully, this becomes a safe and more open space for myself.

### GitHub repo

[lilyzhouZYJ/a_penny_for_my_thought](https://github.com/lilyzhouZYJ/a_penny_for_my_thought)

### Features

- Conversational AI Journaling: Chat with an AI assistant for journaling
- Persistent Storage: Conversations automatically saved in SQLite database
- Semantic Search: RAG-powered context retrieval from past conversations using ChromaDB
- Real-time Streaming: ChatGPT-like streaming responses with Server-Sent Events
- Context Management: Dynamic conversation summarization for context window management

### Tech stack

**Backend:**

- FastAPI
- ChromaDB (vector database for RAG)
- SQLite (conversation storage)
- Pydantic (data validation)
- Uvicorn (ASGI server)
- Tenacity (retry logic)

**Frontend:**

- Next.js
- Tailwind
- shadcn/ui