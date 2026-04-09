---
title: 'Full-Stack TypeScript on Azure — .NET Conf 2025'
description: 'My talk at .NET Conf 2025 exploring how TypeScript developers can leverage Azure services to build end-to-end type-safe applications.'
pubDate: 'Nov 12 2025'
heroImage: '../../assets/blog-placeholder-4.jpg'
---

Even at **.NET Conf**, there's room for TypeScript! I gave a talk on building full-stack TypeScript applications on Azure, and here's the summary.

## Why TypeScript at .NET Conf?

Azure is a polyglot cloud, and TypeScript is one of the fastest-growing languages in the Azure ecosystem. With Azure Functions, Azure Static Web Apps, and the Azure SDK for JavaScript, you can build production-grade apps entirely in TypeScript.

## The Architecture

I demonstrated a real-time collaboration app with the following stack:

- **Frontend**: Astro + React islands for the interactive parts
- **API**: Azure Functions v4 with TypeScript
- **Real-time**: Azure Web PubSub for live collaboration
- **Database**: Azure Cosmos DB with the new v4 TypeScript SDK
- **Auth**: Microsoft Entra ID with MSAL.js

## Live Coding Highlights

### Type-Safe Database Queries
Using Cosmos DB's TypeScript SDK, we created strongly-typed containers where query results are automatically inferred — no `any` types anywhere.

### End-to-End Type Safety
With shared TypeScript interfaces between the frontend and API, we caught integration bugs at compile time rather than runtime. I showed how a schema change in Cosmos DB propagates type errors all the way to the React components.

### Serverless Cold Start Optimization
Tips for keeping Azure Functions TypeScript cold starts under 500ms, including tree-shaking, lazy imports, and the new flex consumption plan.

## Recording

The session recording is available on the .NET Conf YouTube channel. Search for "Full-Stack TypeScript on Azure" to find it!
