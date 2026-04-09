---
title: 'End-to-End DevOps with GitHub Actions — Microsoft Reactor'
description: 'A hands-on workshop I delivered at Microsoft Reactor on building CI/CD pipelines with GitHub Actions for cloud-native applications.'
pubDate: 'Mar 15 2026'
heroImage: '../../assets/blog-placeholder-3.jpg'
---

Last month I had the pleasure of running a **hands-on workshop at Microsoft Reactor** on end-to-end DevOps with GitHub Actions. Here's what we built together!

## Workshop Format

This was a 3-hour hands-on session where attendees built a complete CI/CD pipeline from scratch. We started with a simple Node.js application and progressively added:

1. **Automated testing** — Unit tests, integration tests, and E2E tests running on every push
2. **Container builds** — Multi-stage Docker builds with layer caching
3. **Security scanning** — Dependency audits, SAST with CodeQL, and container image scanning
4. **Deployment to Azure** — Blue-green deployments to Azure Container Apps
5. **Infrastructure as Code** — Bicep templates deployed via GitHub Actions

## Key Patterns We Explored

### Reusable Workflows
We created a shared workflow library that teams can reference across repositories, promoting consistency and reducing duplication.

### Environment Protection Rules
Setting up required reviewers, wait timers, and branch policies for production deployments — ensuring no accidental releases.

### GitHub Environments and Secrets
Properly managing secrets with environment-scoped access, OIDC federation with Azure, and no long-lived credentials.

## Attendee Feedback

The session had about 80 attendees, and the feedback was overwhelmingly positive. The most requested follow-up topic was **GitHub Advanced Security** — which I'm now planning as a separate session!

## Resources

All workshop materials, including step-by-step instructions and starter code, are published on my GitHub repository. Fork it and try it yourself!
