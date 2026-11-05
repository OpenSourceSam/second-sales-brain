# 🏢 Constrained Enterprise Implementation (Microsoft / Local AI)

> **For large orgs with strict IT policies. No paid AI seats. Sensitive customer data.**
> Works within any security policy using tools you already have approved.

[← Back to Overview](../README.md)

---

## At a Glance

| | |
|---|---|
| **Cost** | $0 |
| **Setup Time** | 1 hour |
| **Capture Friction** | High — manual copy-paste |
| **Best For** | Corporate BDRs at traditional enterprises |
| **Security** | Highest — sensitive data stays local |

---

## The Core Idea

You probably can't install new apps or get a paid AI subscription. But you CAN use OneNote/SharePoint (already approved) and run a free local AI model on your work laptop for anything involving customer data.

**The split:** Cloud AI for generic tasks (brainstorming, frameworks). Local AI for anything with real names, companies, or email content.

---

## The Stack

| Component | Tool | What It Does |
|-----------|------|--------------|
| **Database** | SharePoint list or OneNote | Tagged, searchable email log |
| **AI (generic tasks)** | Microsoft Copilot (free) | Draft frameworks, brainstorm subject lines |
| **AI (sensitive tasks)** | Ollama + Mistral 7B (local) | Analyze real emails — nothing leaves your machine |
| **Capture** | Manual copy-paste | Tag with hashtags or SharePoint metadata |
| **Retrieval** | SharePoint search | Filter by tags, personas, scores |

---

## The Bifurcated Model

| Task | Sensitivity | Where It Runs | Example |
|------|-------------|---------------|---------|
| Draft cold email framework | Low | Copilot (cloud) | "Write a cold email framework for construction VPs" |
| Tag existing email | High (names, companies) | Local model | "Tag this email with success/failure reasons" |
| Brainstorm subject lines | Low | Copilot (cloud) | "Give me 10 subject lines for a follow-up" |
| Analyze real email thread | High (customer data) | Local model | "Why did this get a reply and this one didn't?" |
| Weekly pattern review | Medium | Local model | "What do my top 5 emails have in common?" |

---

## Local AI Setup

**Minimum specs:** 16GB RAM, Intel i7 (10th gen+), 50GB free storage

**Install Ollama:**
1. Download from [ollama.com](https://ollama.com) (check with IT — usually no admin rights needed)
2. Terminal: `ollama pull mistral` (downloads Mistral 7B, ~4GB)
3. Chat: `ollama run mistral`

**Performance:** ~10-15 tokens/second on 16GB RAM. Good for tagging and analysis. Use Copilot for longer drafts.

---

## IT Compliance

- **Local model:** data never leaves your machine. Compliant with virtually any policy.
- **Copilot free tier:** processed under Microsoft enterprise terms (work account).
- **No personal accounts.** Always use work email for cloud AI.
- **SharePoint/OneNote:** already approved storage. No new concerns.

---

## Limitations

- Manual capture only (no automation without IT-approved connectors)
- Local model is slower and less capable than cloud models
- Copilot free tier has usage limits and no persistent memory
- Can't build automated pipelines without Power Automate approval

---

## Beyond Email: Additional SSB Modules

The email library is the foundation. These modules extend the SSB using the same constrained-environment approach. See the [main README](../README.md) for the complete framework.

### Account & Vertical Research

- Use **Copilot (free)** for generic industry research -- no customer data needed
- Use **local model** for analyzing your account-specific notes and call transcripts
- Build vertical intelligence in **OneNote** -- one section group per industry, one section per account
- Manual research compounds over time into a searchable knowledge base
- Export and organize research in **SharePoint** for team-wide access

### Automation & List Building

- Limited by IT policies -- no Zapier/Make without approval
- Manual workaround: **SharePoint list with filtered views** by ICP criteria
- **Power Automate** (if approved): auto-capture emails to SharePoint list
- CSV exports from SharePoint for CRM import
- **Copilot** can format and clean prospect lists from raw data

### Cold Calling Support

- **Pre-call:** query local model with the prospect's OneNote section for context
- **Objection prep:** "Based on my notes for [industry], what objections should I expect from a [persona]?"
- **Post-call:** add call notes to the prospect's OneNote entry, tag outcomes
- Keep call scripts in SharePoint alongside email templates
- **Local model stays compliant** -- no customer names leave your machine

---

[← Back to Overview](../README.md)
