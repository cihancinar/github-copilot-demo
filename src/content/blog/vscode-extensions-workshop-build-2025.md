---
title: 'Building VS Code Extensions with AI — Microsoft Build 2025'
description: 'Recap of my Build 2025 workshop on creating VS Code extensions that leverage the Language Model API and Chat Participants.'
pubDate: 'May 22 2025'
heroImage: '../../assets/blog-placeholder-5.jpg'
---

At **Microsoft Build 2025**, I hosted a workshop on building VS Code extensions that integrate with AI through the new Language Model API and Chat Participants.

## What We Built

Over the course of the workshop, attendees built a fully functional VS Code extension that:

- Registers a custom **Chat Participant** (e.g., `@myagent`) in GitHub Copilot Chat
- Uses the **Language Model API** to call GPT models directly from the extension
- Implements **tool calling** so the chat participant can read files, query APIs, and take actions
- Provides a custom **code action** that uses AI to explain and refactor selected code

## Architecture of a Chat Participant

The key concepts we covered:

### Request Handlers
Each chat participant has a request handler that receives the user's prompt and a response stream. You process the prompt, call the language model, and stream back the response.

### Commands and Intent Detection
We added slash commands like `/explain`, `/refactor`, and `/test` to give users structured ways to interact with the participant.

### Tool Integration
The most exciting part — making the participant capable of *doing things*. We integrated file system access, terminal commands, and API calls as tools the model can invoke.

## Key Learnings

1. **Start small**: A chat participant with one focused capability beats a Swiss Army knife
2. **Stream responses**: Users perceive streaming responses as faster and more natural
3. **Handle errors gracefully**: Always provide fallback responses when the model is unavailable
4. **Test with prompt variants**: AI behavior varies — test your participant with diverse prompts

## What's Next

I'm planning a follow-up session on **building MCP servers** that work with VS Code and GitHub Copilot. Stay tuned for the announcement!
