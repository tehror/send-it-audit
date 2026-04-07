# Send-It-Audit

A Claude skill that audits any landing page or app against 7 conversion-readiness criteria. Point it at a URL and it tells you whether the page can capture emails and money if traffic arrives today.

Framework credit: **[ideabrowser.com](https://ideabrowser.com)** — the guys there published the original checklist this skill is built on. Go read their stuff.

---

## What it checks

| # | Criterion | The question |
|---|-----------|--------------|
| 1 | Honest Product Promise | Does the copy describe what the product does *today*, or a future state it can't deliver yet? |
| 2 | Buy Button Present | Is there a visible price and a way to pay? |
| 3 | Single, Clear CTA | One call to action, or three competing ones? |
| 4 | Value Before Login | Does the user see something useful before you ask for their Google account? |
| 5 | Complete Funnel | Is there an actual path from "I found you" to "take my money"? |
| 6 | Selling, Not Building | Does the page speak to customer outcomes, or does it read like a changelog? |
| 7 | Shareability Mechanism | Is there anything that makes it easy for a new user to tell someone else? |

Each criterion scores as **PASS**, **PARTIAL**, or **FAIL**.

---

## What you get

- **Top Priority Fix** — the single most important thing blocking conversions, stated plainly
- **Scored table** — all 7 criteria at a glance
- **Fix list** — one specific action per failure, ordered by conversion impact
- **What's working** — genuine PASSes worth preserving

---

## Install

```bash
npx skills add tehror/send-it-audit
```

---

## Usage

Once installed, give Claude a URL:

> Audit my landing page: https://yoursite.com

Claude will fetch the page automatically and return the full audit. No copy-pasting required.

---

## Scoring guide

| Score | Verdict |
|-------|---------|
| 7/7 | READY — send traffic |
| 5-6/7 | NEEDS WORK — fixable in a day |
| 3-4/7 | NOT READY — core gaps blocking conversions |
| 0-2/7 | NOT READY — rebuild the funnel before driving traffic |

---

## Origin

This skill operationalizes the checklist published by the team at [ideabrowser.com](https://ideabrowser.com). The original framing: most founders ship products that aren't ready to receive customers — not because the product is bad, but because the page can't convert anyone who finds it.

The fix is boring: figure out who you're selling to, what they'll pay for, and build the simplest possible path from "I found you" to "take my money."

This skill makes sure that path exists before you drive traffic into a dead end.
