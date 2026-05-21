# revenue-ops

> **The complete revenue operations plugin for Malaysian business owners**

Four AI skills that cover your full revenue cycle — from finding prospects to getting paid.

Compatible with **Claude Code** and any Claude Code plugin marketplace.

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

### Install all four skills (recommended)

```
/plugin marketplace add adrianchinghc/revenue-ops
/plugin install lead-researcher@revenue-ops
/plugin install inquiry-qualifier@revenue-ops
/plugin install proposal-writer@revenue-ops
/plugin install payment-chaser@revenue-ops
```

### Install a single skill

```
/plugin marketplace add adrianchinghc/revenue-ops
/plugin install lead-researcher@revenue-ops
```

Replace `lead-researcher` with any of: `inquiry-qualifier`, `proposal-writer`, `payment-chaser`.

### Test before installing

```bash
claude --plugin-dir ./lead-researcher
```

Clone the repo and run this to try a skill locally without installing it.

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

## License

MIT — free to use, modify, and distribute.
