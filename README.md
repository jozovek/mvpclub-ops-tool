# 🛠️ MVP Club Platform

**A unified marketing, sales, and ops platform for a robust member AI community**

Built by MVP Club's 3 co-founders (Jill, Matt, Ryan). React + Express + Cloud SQL PostgreSQL, deployed on Google Cloud Run.

---

## What this is

A single platform that runs MVP Club's entire go-to-market and community operations — lead detection, relationship management, content generation, outreach, and newsletter automation. Everything a 3-person founding team needs to run a growing community without hiring an ops team.

---

## Modules

### Signal Detector
Automated lead scanning that finds AI enablement consulting opportunities across the web.
- Scans Google Jobs and Google News via SerpAPI on a configurable cron schedule
- Detects companies hiring for AI transformation roles or announcing AI investments
- Scores and surfaces high-value signals for review
- Signals can be promoted directly into the CRM as contacts

### External Opportunities Pipeline
Tracks podcasts, YouTube shows, conferences, and speaking opportunities from discovery to pitch to completion.
- Pipeline view showing everything in progress, pitched, accepted, and completed
- Auto-tagged by media type (podcast, conference, webinar, etc.)
- **Playbooks auto-attach based on media type** — tag something as "podcast" and the podcast prep playbook is added automatically so anyone preparing has a structured workflow

### CRM
Contact and company management with a deal pipeline built for a consulting business.
- Tracks contacts, companies, and deal stages
- Signals flow directly into the CRM from the detector
- Built for how a small founding team actually manages relationships — not enterprise CRM bloat

### Marketing & Content
AI-powered content generation using the Claude API, with a full content pipeline and publishing workflow.
- Draft blog posts, LinkedIn content, and outreach templates
- Markdown source files feed the content pipeline
- UTM tagging built in — every outbound link is automatically tagged for Google Analytics tracking
- Content flows through a 3-stage pipeline: `to-review/` → `to-post/` → `posted/`

### Newsletter Automation
A fully automated weekly newsletter workflow.
- Gathers meeting notes and community posts automatically
- Syncs subscribers from lead magnet signups to the master list
- Drafts newsletter HTML matching established format and brand
- Test sends, previews, and scheduled sends via Gmail API
- Personalized greetings from the subscriber list

---

## Architecture

| Layer | Stack |
|-------|-------|
| Frontend | React + Vite |
| Backend | Express + TypeScript |
| Database | Cloud SQL PostgreSQL |
| AI | Claude API (content generation + outreach) |
| Search | SerpAPI (Google Jobs + Google News) |
| Email | Gmail API (service account + OAuth) |
| Deployment | Google Cloud Run |

---

## Why I'm showing this

This is the tool I built to run my own business — and it's a demonstration of the same approach I bring to clients. Instead of stitching together 6 SaaS tools and hoping someone maintains the integrations, I built one platform that does exactly what we need.

It's also proof of concept for what non-technical founders can build with AI. The signal detector, the content pipeline, the newsletter automation — these are the kinds of systems I help clients design and deploy.

### A note on how I build

I can take a tool like this from zero to a strong, usable MVP — functional enough that our 3-person founding team runs our entire operation on it daily. But I'm not a software engineer. For anything that needs to be production-grade, external-facing, or handling scale, I pair with a developer to make sure the architecture, security, and reliability are where they need to be. That's the model I recommend to clients too: use AI to build fast, get to a working prototype quickly, then bring in engineering support to harden it for production.

---

## Status

🟢 **In production** — actively used by all 3 co-founders to run MVP Club's operations.

---

*Part of [Jill Ozovek's portfolio](https://github.com/jozovek) — Fractional Head of AI Adoption & Co-Founder, MVP Club*
