# revenue-ops

> **The complete revenue operations plugin for Malaysian business owners**

Four AI skills that cover your full revenue cycle — from finding prospects to getting paid.

Works with **Claude Code**, **OpenAI Codex**, **Cursor**, **Windsurf**, and any agent that supports the [Agent Skills spec](https://agentskills.io).

---

## The Four Skills

| Skill | What It Does | Best For |
|---|---|---|
| 🔍 `lead-researcher` | Finds target companies, surfaces contact intelligence, and builds a multi-touch outreach sequence | Business owners doing outbound BD |
| 📩 `inquiry-qualifier` | Scores incoming leads, reads the psychology behind the message, and drafts a response that advances the sale | Anyone receiving client inquiries |
| 📋 `proposal-writer` | Turns rough briefs into persuasive, client-ready proposals | Service businesses, consultants, agencies |
| 💰 `payment-chaser` | Diagnoses why an invoice is unpaid and drafts the right follow-up for the situation | Any business with AR and overdue invoices |

---

## Installation

### Option 1 — CLI (recommended, works everywhere)

```bash
npx skills add adrianchinghc/revenue-ops
```

Installs to `.agents/skills/` and symlinks into `.claude/skills/` for Claude Code compatibility.

### Option 2 — Claude Code plugin marketplace

```
/plugin marketplace add adrianchinghc/revenue-ops
/plugin install revenue-ops@revenue-ops
```

### Option 3 — Manual copy

```bash
git clone https://github.com/adrianchinghc/revenue-ops.git
cp -r revenue-ops/skills/* ~/.agents/skills/
```

---

## How to Use

Once installed, describe what you need in plain language. Your agent will automatically activate the right skill.

**Examples:**

| What you type | Skill that activates |
|---|---|
| *"Find me 5 logistics companies in Klang Valley I can reach out to"* | Lead Researcher |
| *"Got this WhatsApp from a prospect, is it worth pursuing?"* | Inquiry Qualifier |
| *"Write a proposal for a client who wants to digitise their warehouse operations"* | Proposal Writer |
| *"Ahmad Construction hasn't paid Invoice 045, it's 3 weeks overdue"* | Payment Chaser |

---

## Skill Details

### 🔍 Lead Researcher

Two modes:
- **Research a specific company** — provide a name, get a deep research card, contact intelligence, and a 3-touch personalised outreach sequence
- **Find target companies** — provide an industry and location, get 5–8 prospects researched with contact details and outreach drafts for each

Includes exact Google search strings, a signal library for identifying pain from job postings and news, and a phone script for follow-ups.

*Requires an agent with web browsing capability.*

---

### 📩 Inquiry Qualifier

Reads an incoming inquiry at multiple levels and produces:
- Full BANT assessment (Budget, Authority, Need, Timeline)
- Psychological read — buying trigger, primary motivation, decision style, hidden signals
- Immediate action recommendation
- Two ready-to-send response options (short WhatsApp + full email)
- Qualifying questions with reasoning, and anticipated objections with rebuttals

**Works from:** WhatsApp messages, emails, web form submissions, any text inquiry.

---

### 📋 Proposal Writer

Starts with a brief analysis before writing, then produces a complete proposal with:
- Executive summary using the Problem → Consequence → Solution → Proof → Commitment formula
- Cost-of-inaction framing to make the investment feel justified
- Scoped solution with explicit inclusions and exclusions
- Why-projects-fail risk reversal section
- Decision support section to help internal champions get sign-off

Special variants: retainer, competitive, re-proposal, budget-constrained.

**Works from:** Voice note transcripts, discovery call notes, client emails, verbal briefs.

---

### 💰 Payment Chaser

Diagnoses the non-payment situation first (forgetful / cash flow / disputing / avoiding), then picks the right strategy. Produces:
- Messages across 5 escalation levels — from pre-due reminder to formal demand
- Multi-channel sequence (WhatsApp → email → call script)
- Special templates for disputed invoices, payment arrangement offers, and ghost clients
- Batch processing for multiple invoices in one go

**Works from:** Single invoice details or a batch list with multiple clients and amounts.

---

## Demo Script

The examples below use **Upstack Studio** — a Malaysian software agency that builds custom integrations for SMEs — as the sample business. Swap in your own context and the outputs will be tailored accordingly.

### Setup (say this first)

> "I'm Adrian from Upstack Studio. We build custom software and system integrations for Malaysian SMEs. Our target clients are COOs and Operations Directors at manufacturing, logistics, or trading companies doing RM50M+ in revenue. Our typical project is RM80K–RM180K."

---

### 🔍 Lead Researcher

> "Find me 5 manufacturing or logistics companies in Shah Alam or Klang Valley that we can approach about warehouse or operations digitisation. We build custom software and integrations for SMEs — targeting COOs and Operations Directors at companies doing RM50M+ revenue who still run on Excel or disconnected systems."

**What you get:** A prospect table with 5 companies → research card for each (pain signals, who to contact) → a personalised 3-touch outreach sequence per company (Day 1, Day 4–5, Day 10).

---

### 📩 Inquiry Qualifier

> "Got this WhatsApp from a prospect just now — qualify it for me:
>
> 'Hi, I got your number from David at AmBank. We're a building materials company, about 300 staff. Been having a lot of problems with our inventory — our guys keep making errors and we lose track of stock across 3 warehouses. A friend said you build custom systems? We've been looking at this for about a year but haven't done anything yet. Budget is flexible if the solution is right. Can we do a call this week?'"

**What you get:** BANT score → psychological read (buying trigger, decision style, hidden signals) → immediate action recommendation → two ready-to-send responses (short WhatsApp + full email) → 3 qualifying questions with reasoning.

---

### 📋 Proposal Writer

> "Write a proposal for Syarikat Bumi Jaya Sdn Bhd — building materials distributor in Shah Alam, 3 warehouses, 200 staff. They track inventory on Excel and want to connect it to SQL Accounting for real-time stock visibility across all 3 locations. Biggest pain: stock discrepancies causing wrong invoicing — they've lost two clients this year because of it. Decision maker is COO Kenny Lim. Timeline is ASAP. Our proposed scope is a 14-week integration project at RM145,000."

**What you get:** Brief analysis (real problem, buying trigger, risk profile) → full 10-section proposal including executive summary (Problem→Consequence→Solution→Proof→Commitment), cost-of-inaction framing, scoped solution with explicit inclusions and exclusions, why-projects-fail risk reversal, and a decision support section so Kenny can get it approved internally.

---

### 💰 Payment Chaser

> "Chase this payment: Client is Mega Steel Trading, Invoice #112, RM78,000 for a completed inventory system we delivered 8 weeks ago. They signed the UAT sign-off. Every time we follow up they say 'it's in finance processing' — but it's been 6 weeks since the 30-day payment term. Last reply from them was 10 days ago. They're still using the system."

**What you get:** Situation diagnosis (avoiding vs cash flow vs disputing) → the right escalation level → WhatsApp message, email, and call script tailored to the situation → next-step trigger (if no response in 5 days, escalate to formal demand).

---

### Demo flow (20 minutes)

| Time | What |
|------|------|
| 2 min | Install skills or show already installed |
| 1 min | Set business context (the Upstack Studio intro above) |
| 4 min | Lead Researcher — let it search, talk while it runs |
| 4 min | Inquiry Qualifier — paste the WhatsApp, walk through the output |
| 5 min | Proposal Writer — paste the brief, scroll through the proposal |
| 4 min | Payment Chaser — paste the invoice situation, show the diagnosis |

---

## License

MIT — free to use, modify, and distribute.
