# revenue-ops

> **The complete revenue operations plugin for Malaysian business owners**

Four AI skills that cover your full revenue cycle — from finding prospects to getting paid.

Compatible with **Claude Code**, **OpenAI Codex**, **GitHub Copilot**, and any [Agent Skills](https://agentskills.io)-compatible client.

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

### Option 1 — Claude Code (one command, all skills)

```bash
git clone https://github.com/adrianchinghc/revenue-ops.git /tmp/revenue-ops && \
  cp -r /tmp/revenue-ops/lead-researcher ~/.claude/skills/ && \
  cp -r /tmp/revenue-ops/inquiry-qualifier ~/.claude/skills/ && \
  cp -r /tmp/revenue-ops/proposal-writer ~/.claude/skills/ && \
  cp -r /tmp/revenue-ops/payment-chaser ~/.claude/skills/ && \
  rm -rf /tmp/revenue-ops
```

Skills are now available globally in every Claude Code session.

### Option 2 — Claude Code (project-only install)

Install into a specific project so teammates get the skills automatically when they open the project:

```bash
mkdir -p .claude/skills

git clone https://github.com/adrianchinghc/revenue-ops.git /tmp/revenue-ops && \
  cp -r /tmp/revenue-ops/lead-researcher .claude/skills/ && \
  cp -r /tmp/revenue-ops/inquiry-qualifier .claude/skills/ && \
  cp -r /tmp/revenue-ops/proposal-writer .claude/skills/ && \
  cp -r /tmp/revenue-ops/payment-chaser .claude/skills/ && \
  rm -rf /tmp/revenue-ops
```

### Option 3 — Agent Skills CLI

```bash
npx skills add https://github.com/adrianchinghc/revenue-ops
```

### Option 4 — Single skill only

```bash
# Replace SKILL_NAME with: lead-researcher, inquiry-qualifier, proposal-writer, or payment-chaser

# Global install (Claude Code)
git clone --depth 1 https://github.com/adrianchinghc/revenue-ops.git /tmp/revenue-ops && \
  cp -r /tmp/revenue-ops/SKILL_NAME ~/.claude/skills/ && \
  rm -rf /tmp/revenue-ops

# Project install (Claude Code)
cp -r /tmp/revenue-ops/SKILL_NAME .claude/skills/
```

---

## How to Use

Once installed, describe what you need in plain language. Claude Code will automatically activate the right skill.

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

*Requires an agent with web browsing capability (Claude Code with web access, Copilot Agent mode).*

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

## Compatibility

| Tool | Supported |
|---|---|
| Claude Code | ✅ |
| OpenAI Codex | ✅ |
| GitHub Copilot (Agent mode) | ✅ |
| Cursor | ✅ |
| Any Agent Skills-compatible client | ✅ |

---

## License

MIT — free to use, modify, and distribute.
