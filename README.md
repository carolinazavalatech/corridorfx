# CorridorFX
### Product Discovery Case Study — Cross-Border Payments for UK SMEs

> **This is a product thinking exercise, not a live product or startup pitch.**
> All data shown is illustrative, based on publicly available market benchmarks

---

## 🔗 Live Prototype

**[View the interactive prototype →](https://carolinazavalatech.github.io/corridorfx/)**

Navigate through 3 screens · Toggle between payment flows · Test the FX conversion simulator

---

## The Problem

UK SMEs trading with European partners face three compounding pain points in cross-border payments:

**1. Hidden FX markups (2–4%)** — Banks embed a spread above the mid-market rate. The customer sees a "no fee" transfer, but pays 2–4% more than the real market rate on every conversion. Neither side sees the full cost before confirmation.

**2. Correspondent banking chain** — International transfers via SWIFT pass through one or more intermediary banks, each deducting fees from the value in transit. A payment of €10,000 may arrive as €9,988, with no explanation.

**3. Slow settlement (1–3 business days)** — While domestic UK transfers settle in seconds via Faster Payments, international transfers remain slow, locking up working capital and straining supplier relationships.

These problems affect both directions of trade:
- **UK → EU:** UK SME paying a European supplier in EUR
- **EU → UK:** European client paying a UK SME, with conversion to GBP

Post-Brexit, the UK–EU corridor has become more complex, with additional friction for UK-issued IBANs. The Bank of England, FCA, and HM Treasury's Payments Forward Plan (February 2026) have all flagged cross-border payment modernisation as an active priority.

---

## The Solution Concept

**CorridorFX** is a conceptual AI-powered orchestration layer for cross-border B2B payments. It addresses three core problems:

| Problem | Solution |
|---|---|
| Hidden FX markup | Mid-market rate applied to every conversion (no spread) |
| No fee visibility | Full cost shown to both sides before any confirmation |
| Slow settlement | AI smart routing selects the fastest available payment rail per corridor |

### Positioning

The product is designed as an **orchestration layer**, not a bank replacement:
- Connects to existing business bank accounts via Open Banking APIs
- Does not hold client funds as a bank
- Positioned as a **white-label layer** that financial institutions could adopt
- Collaborative model — works with incumbents, not against them

---

## What Was Built

A navigable high-fidelity prototype with **3 connected screens**:

### Dashboard
- AI insight banner with real-time FX recommendation
- 3 KPIs: FX savings this month (vs estimated standard bank rate), settled instantly, fee transparency
- Recent transactions with debit/credit indicators and timestamps
- AI payment routing breakdown (instant rail, domestic fast rail, standard wire)

### FX Intelligence
- Currency selector: EUR (EU countries), USD (United States), CHF (Switzerland)
- Pending balance input with live GBP preview at AI-timed rate
- Dynamic rate chart  
- AI conversion recommendation with "Convert now →" button
- 3 optimal conversion windows (next 72h) with AI pick indicator
- FX exposure and monthly efficiency cards

### Send / Receive
- Toggle between **UK paying EU →** and **← EU paying UK**
- Country selector (7 corridors) (automatically adjusts currency, FX rate, settlement time) 
- Live FX calculation with mid-market rate and fee breakdown
- Date picker for scheduling future payments
- Progress indicator when arriving from "Convert now" (tracks partial conversions across multiple corridors (e.g. €10k from Germany + €10k from Italy))

---

## FX Rates Used (30 March 2026 · mid-market)

| Pair | Rate |
|---|---|
| EUR/GBP | 0.8531 (GBP/EUR: 1.1724) |
| USD/GBP | 0.7540 (GBP/USD: 1.3261) |
| CHF/GBP | 0.9472 (GBP/CHF: 1.0558) |

Sources: Yahoo Finance, XE, OFX — March 29–30, 2026.

---

## Key Product Decisions

**Why no bank comparisons in the UI?** The product is positioned as collaborative with financial institutions — not competitive. Naming specific banks would misrepresent the strategic intent and could alienate the target adopters (the banks themselves).

**Why generic rail names?** "Instant rail", "Domestic fast rail" and "Standard wire" replace SEPA Instant, Faster Payments and SWIFT. The user sees the outcome (speed, cost), not the infrastructure.

**Why £ — placeholders for values?** Avoids the prototype being mistaken for real data. The product concept is the focus, not specific numbers.

**Why a progress indicator for EUR conversion?** A €20,000 pending balance typically comes from multiple countries (e.g. €10k Germany + €10k Italy). The progress bar bridges FX Intelligence (aggregate view) and Send / Receive (per-transaction execution) — making the multi-step flow intuitive.

---

## Discovery Sources

- Bank of England — cross-border payment cost data
- Financial Conduct Authority (FCA) — Consumer Duty, payments transparency
- HM Treasury — Payments Forward Plan, February 2026
- WorldFirst UK — Cross-border payment challenges for UK SMEs, January 2026
- Financial Stability Board (FSB) — G20 cross-border payments roadmap
- McKinsey — SME cross-border payment cost benchmarks
- PYMNTS Intelligence — Bank–fintech partnership data, April 2025

---

## About

Created by a Product Manager with 5+ years of experience in B2B digital products, including a payments product in Brazil's agribusiness sector. This case study was built as part of a product discovery exercise exploring the UK fintech market ahead of a career transition to the UK.

**Stack:** HTML · CSS · Vanilla JavaScript · Chart.js

---

*This is a product discovery case study — not a live product, real company, or investment pitch.*
