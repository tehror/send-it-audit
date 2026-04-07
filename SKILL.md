---
name: send-it-audit
description: Audit a webpage or app landing page to check if it is conversion-ready — meaning it can capture emails and money when traffic arrives. Use this skill whenever the user asks to audit, review, critique, or check a website, landing page, app page, or product page for conversion readiness, go-to-market readiness, funnel quality, CTA clarity, pricing presence, or similar. Trigger on phrases like "audit my site", "review my landing page", "is my app ready for traffic", "check my funnel", "landing page feedback", "conversion rate", or "is my site ready to launch". Also trigger when the user shares a URL and asks for feedback on it.
---

# App Audit Skill

Audit a webpage or app landing page against 7 conversion-readiness criteria. Determines whether the page can capture emails and money if a surge of traffic arrives today.

Framework credit: [ideabrowser.com](https://ideabrowser.com)

---

## Step 1: Fetch the page automatically

When the user provides a URL, immediately call `web_fetch` on it. Do not ask them to paste content. Do not wait for confirmation. Fetch it, read the full output, and proceed.

- If `web_fetch` fails, try `web_search` with the URL or site name to get a cached or summarized version.
- If both fail, ask the user to paste the page content or a screenshot.

While reading, capture:
- Headlines and subheadlines
- CTA button text, count, and placement
- Pricing (present or absent)
- Login/signup gates before value
- Lead magnets, demos, free sample output
- Email capture forms
- Social sharing or referral mechanisms
- Overall promise vs. described current functionality

---

## Step 2: Score against the 7 criteria

Evaluate each as **PASS**, **FAIL**, or **PARTIAL**. Be direct. Do not soften failures.

#### Criterion 1: Honest Product Promise
Does the copy describe what the product does *today*, not a future vision?

- PASS: Describes current, working functionality with concrete outcomes.
- PARTIAL: Accurate claims mixed with vague aspirational language.
- FAIL: Oversells a future state the product cannot currently deliver.

Red flags: "revolutionize," "transform," "the future of," capability claims tied to unbuilt features.

---

#### Criterion 2: Buy Button Present
Is there a visible, clickable way to pay?

- PASS: Clear pricing and a buy/subscribe/pay CTA visible without excessive scrolling.
- PARTIAL: Pricing exists but is buried, vague ("contact us"), or requires navigating away.
- FAIL: No pricing. No way to pay. Waitlist-only or "coming soon."

Note: "Pay what you want" or "$5 early access" counts. A waitlist does not.

---

#### Criterion 3: Single, Clear CTA
How many distinct calls to action are on the page? Do they conflict?

- PASS: One primary CTA. All other links are visually subordinate.
- PARTIAL: One dominant CTA with minor competing links.
- FAIL: Multiple CTAs of equal visual weight ("Get started," "Join waitlist," "Book a demo" — all competing).

---

#### Criterion 4: Value Before Login Gate
Does the user see meaningful value before being asked to create an account?

- PASS: Demo, sample output, free tool, or lead magnet accessible without signing in.
- PARTIAL: Some value visible, but key proof is gated behind a login.
- FAIL: First ask is account creation before any value is shown.

---

#### Criterion 5: Complete Funnel
Is there a clear, complete path from "I found you" to "take my money"?

Map against five stages:
1. Traffic source (implied or stated)
2. Landing page CTA
3. Lead capture or value delivery
4. Email nurture or direct offer
5. Purchase path

- PASS: All five stages present or clearly implied.
- PARTIAL: Funnel exists but has gaps (no email capture, CTA leads nowhere, no follow-up).
- FAIL: Page exists in isolation. No capture, no nurture, no purchase path.

---

#### Criterion 6: Selling, Not Just Building
Does the page reflect a go-to-market mindset or a feature-shipping mindset?

- PASS: Focused on customer outcome and one core use case. Features are secondary.
- PARTIAL: Mix of outcome language and feature-list thinking.
- FAIL: Page reads like a changelog. Features dominate. No clear ideal customer implied.

Red flags: bullet lists of features without outcome framing, technical jargon without translation.

---

#### Criterion 7: Shareability / Virality Mechanism
Is there any mechanism that makes it easy for a new user to tell someone else?

- PASS: Referral link, share button, social proof, "powered by" branding on output, or built-in sharing in the product itself.
- PARTIAL: Social links present but no active sharing incentive or mechanism.
- FAIL: No sharing mechanism. Word-of-mouth requires 100% user effort.

---

## Step 3: Deliver the audit

Use this exact output format:

---

## App Audit: [Page Name or URL]

**Overall Verdict:** [READY / NEEDS WORK / NOT READY]

**Top Priority Fix:** [One sentence. The single most important thing blocking conversions right now. No hedging.]

| # | Criterion | Status | Notes |
|---|-----------|--------|-------|
| 1 | Honest Product Promise | PASS/PARTIAL/FAIL | One-line finding |
| 2 | Buy Button Present | PASS/PARTIAL/FAIL | One-line finding |
| 3 | Single, Clear CTA | PASS/PARTIAL/FAIL | One-line finding |
| 4 | Value Before Login | PASS/PARTIAL/FAIL | One-line finding |
| 5 | Complete Funnel | PASS/PARTIAL/FAIL | One-line finding |
| 6 | Selling, Not Building | PASS/PARTIAL/FAIL | One-line finding |
| 7 | Shareability Mechanism | PASS/PARTIAL/FAIL | One-line finding |

**Score: X/7**

---

### What to fix

List only FAILs and PARTIALs, ordered by conversion impact. For each:

**[Criterion name]**
What's broken: [One sentence]
Fix: [One specific, actionable step — not a list of options]

---

### What's working

Call out genuine PASSes worth preserving. Keep this short.

---

## Scoring Guide

| Score | Verdict |
|-------|---------|
| 7/7 | READY — send traffic |
| 5-6/7 | NEEDS WORK — fixable in a day |
| 3-4/7 | NOT READY — core gaps blocking conversions |
| 0-2/7 | NOT READY — rebuild the funnel before driving traffic |

---

## Tone Guidelines

- Be direct. Founders need to hear what is broken, not what might possibly be improved.
- Do not hedge. "The CTA could potentially be clearer" is not useful. "There are three CTAs. Pick one." is.
- If something is genuinely good, say so. Credibility comes from honest PASSes too.
- One fix per failure. Not a menu of options.