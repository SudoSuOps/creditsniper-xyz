# CreditSniper

**Fix your credit report. We read it. We find the errors. We write the letters.**

CreditSniper is an AI-powered consumer credit defense system built by [Swarm & Bee](https://swarmandbee.ai). It analyzes credit reports, identifies FCRA and FDCPA violations, generates dispute letters with real statute citations, and delivers them via certified or regular mail.

---

## How It Works

```
1. Paste your credit report
2. AI finds errors and violations
3. Dispute letters generated with real statute citations
4. Print them yourself (free) or we mail them
```

## What It Does

- **Credit Report Analysis** — parses every tradeline, identifies errors, flags violations
- **Dispute Letters** — complete, ready-to-send letters citing FCRA §611, §623, §609, FDCPA §809, §805
- **Score Optimization** — tactical FICO improvement strategies
- **Debt Collector Defense** — validation demands, cease and desist, SOL defense
- **Identity Theft Recovery** — FTC affidavit workflow, FACTA §605B blocking
- **Escalation Paths** — CFPB complaints, AG complaints, intent-to-litigate letters

## Privacy

```
We don't store your data.
We don't mine your data.
We are healers only.
```

- Credit reports processed in memory, never saved to our servers
- No database stores your report — it doesn't exist after processing
- All inference runs on bare-metal hardware we own
- No third party ever sees your report

## Pricing

| Plan | Price | What You Get |
|------|-------|-------------|
| **Pro** | $49/mo | Unlimited analysis, letters, strategies |
| Certified Mail | $4.99/letter | USPS Certified + return receipt |
| Regular Mail | $1.99/letter | USPS First Class |

Print letters yourself for free. Mail service is optional.

## The Model

CreditSniper-27B — Qwen3.5-27B fine-tuned on 84,115 consumer credit defense pairs.

- 1.35M FCRA mentions in training data
- 302K FDCPA mentions
- 28 specialized streams
- Eval loss: 0.5776
- Trained 42 hours on RTX PRO 6000 Blackwell (96GB), bare metal
- Adversarial tested: catches statute traps, FDCPA/OC distinction, cross-bureau inconsistencies

## Stack

```
Frontend:  Cloudflare Pages (creditsniper.xyz)
Backend:   Cloudflare Worker (api.creditsniper.xyz)
Inference: vLLM on RTX PRO 6000 Blackwell (bare metal)
Mail:      PostGrid API
Billing:   Stripe
Auth:      API key (cs_live_*)
Database:  Supabase (wallet + dispute status only — no report data)
Identity:  creditsniper.eth (ENS)
```

## Links

- **Product**: [creditsniper.xyz](https://creditsniper.xyz)
- **Parent**: [swarmandbee.ai](https://swarmandbee.ai)
- **ENS**: creditsniper.eth
- **Contact**: help@creditsniper.xyz

---

*CreditSniper is not a law firm, credit repair organization, or credit counseling service. It does not guarantee specific outcomes. Consumers should consult a licensed attorney for legal advice.*

*Built by [Swarm & Bee Intelligence](https://swarmandbee.ai) — Real compute. Real curation. Real Honey.*
