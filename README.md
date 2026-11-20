# n8n AI Automation Portfolio

Production n8n multi-agent automation workflows, LLM structured extraction pipelines, and API/webhook integrations.

## Featured Workflows

### 1. Daily AI Research Digest Automation
* **Stack:** `n8n`, `RSS/HTTP`, `Google Gemini`, `Email/Messaging`
* **Overview:** Automated ingestion, summarization, and structured digest delivery of daily AI and machine learning research updates.

### 2. AI Email Triage & Auto-Drafting Agent (`Project 2 (AI Email Triage & Auto-Drafting Agent).json`)
* **Stack:** `n8n`, `IMAP`, `Google Gemini`, `JavaScript Code Node`, `Gmail OAuth2`
* **Architecture:** `Email Trigger (IMAP)` → `Limit` → `Normalize Email` → `AI Agent (Gemini)` → `Parse AI JSON` → `If (requires_reply == true)` → `Gmail (Create Draft)`
* **Key Features:**
  * Sanitizes raw HTML/plain-text emails and strips tracking links to prevent token bloat.
  * Classifies incoming messages by category (`urgent_action`, `opportunity_lead`, `client_project`, `notification_social`, `newsletter_promo`, `spam`) and priority (`high`, `medium`, `low`).
  * Enforces a human-in-the-loop guardrail: only actionable emails (`requires_reply: true`) generate a contextual reply draft in Gmail `Drafts`; automated notifications and spam terminate cleanly without noise.

---

## Upcoming Portfolio Milestones
* **Project 3:** Multi-Modal Telegram AI Assistant (Voice Note Transcription, Conversational Memory & Live Tool-Calling)
* **Project 4:** AI Lead Qualification & Relational Database (`PostgreSQL` / `Supabase`) Sync Pipeline with Idempotency & Error Handling
* **Project 5:** Enterprise RAG Knowledge & Support Engine (`pgvector` / Vector Search + Cited Responses)
