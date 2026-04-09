---
title: 'Building Intelligent Apps with Azure AI Services — Microsoft Ignite 2025'
description: 'Recap of my Ignite 2025 session on building production-ready intelligent applications using Azure AI Services and the Azure AI SDK.'
pubDate: 'Nov 19 2025'
heroImage: '../../assets/blog-placeholder-2.jpg'
---

What an incredible experience presenting at **Microsoft Ignite 2025**! Here's a recap of my session on building intelligent applications with Azure AI Services.

## Session Recap

The session focused on taking AI applications from prototype to production. We covered the full lifecycle — from model selection to deployment, monitoring, and responsible AI practices.

## Topics Covered

### 1. Azure OpenAI Service in Production
We discussed patterns for building reliable, scalable applications on top of Azure OpenAI, including retry strategies, token management, and cost optimization.

### 2. Retrieval-Augmented Generation (RAG)
A deep dive into implementing RAG patterns using Azure AI Search and Azure Cosmos DB as vector stores. I demonstrated a live coding example building a knowledge assistant.

### 3. AI Application Observability
How to monitor your AI applications in production using Azure Monitor and Application Insights, tracking metrics like latency, token usage, and response quality.

### 4. Responsible AI Guardrails
Implementing content filtering, grounding detection, and prompt shields to ensure your AI applications are safe and trustworthy.

## Demo Code

All demo code from the session is available on my GitHub. The main project is a full-stack intelligent document assistant built with:
- **Backend**: Node.js with Azure AI SDK
- **Frontend**: React + TypeScript
- **Infrastructure**: Azure Container Apps + Bicep templates

## Audience Q&A Highlights

The most popular question was about managing costs at scale. My recommendation: implement semantic caching with Azure Redis and use GPT-4o mini for classification tasks before routing to more powerful models.

Thanks to everyone who attended and asked great questions!
