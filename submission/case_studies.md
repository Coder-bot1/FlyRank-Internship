# General AI Fluency — Week 2: Frame It as Cases (Work That Speaks for Itself)

---

## 1. Voice Card
> **"Direct, grounded, precise, skeptical of hype, transparent."** (6 words)

---

## 2. Flagship Case Study: Search Intelligence & Content Refresh Opportunity Engine

### Beat 1: The Problem
Enterprise content teams manage tens of thousands of published articles, but have finite editorial bandwidth to audit and update them. When rankings slip, teams often rely on blunt rules of thumb—like reviewing every article older than six months. On a dataset of 30,000 enterprise URLs, this naive heuristic produced severe false positives (wasting editorial hours on evergreen, stable content) while completely overlooking high-volume pages undergoing rapid traffic collapse.

### Beat 2: What I Did (and What I Decided)
I built a multi-signal **Refresh Opportunity Scoring Engine** using Python, scikit-learn, and DuckDB to rank pages by genuine recovery potential rather than age alone:
- **Pre-decision Signals**: Combined keyword search demand, 90-day visibility, striking-distance ranking opportunity (positions 4–20), recent 30-day impression change, and content staleness into a bounded index $[0, 100]$.
- **Leakage Prevention**: Strictly excluded target-derived percentages (`trend_pct`) and future-window outcomes from the feature matrix, verifying zero correlation leakage.
- **Honest Generalization**: Validated models using grouped client-holdout splits (`client_id`) rather than random row splits to prevent domain memorization.
- **Decision Support**: Assigned each page one of four transparent reason codes (`HIGH_DEMAND_DECLINE`, `STALE_CONTENT`, `RANKING_DROP`, `CTR_FIX`) paired with a concrete editorial action.

### Beat 3: What Came of It
- **2.8× Precision Lift**: At backlog depth (Top 500), the model achieved a precision of **0.662** vs. the heuristic rule's **0.240** (~175% relative improvement) in isolating declining, high-value assets.
- **Actionable Triage**: Segmented 28,795 active pages into clear priority tiers (`Critical`, `High`, `Medium`, `Low`), turning unmanageable backlogs into an immediate queue.
- **Deployed Research Paper**: Published the full findings, methodology, and interactive SVG charts as a live, open-access research paper: [https://coder-bot1.github.io/FlyRank-Internship/](https://coder-bot1.github.io/FlyRank-Internship/).

---

## 3. Bio Copy
Applied Machine Learning engineer specializing in Search Intelligence and decision-support systems. I turn large, messy enterprise search logs into leak-free models and transparent, reason-coded action queues that content teams can actually trust.

---

## 4. Contact & Call-to-Action (CTA) Copy
Looking for an engineer who frames business problems rigorously, writes clean code, and validates without shortcuts?  
**[Send me an email to schedule a 15-minute technical intro call](smuqashif@gmail.com)** or inspect the full codebase on **[GitHub](https://github.com/Coder-bot1/FlyRank-Internship)**.

---

## 5. Before & After: Generic AI vs. Honest Edited Copy

* **Before (Generic AI Draft):**
  > *"I am a highly motivated, results-driven AI specialist passionate about leveraging cutting-edge machine learning algorithms to optimize search engine ranking performance, empower digital marketing synergy, and unlock unprecedented ROI across complex enterprise ecosystems."*

* **After (Edited & Human Version):**
  > *"I built a multi-signal scoring model on 30,000 enterprise search pages that beat standard heuristic rules by 2.8× at flagging declining content, without leaking target data or pretending to predict Google's algorithm."*

* **Why the edit works:**
  Cuts four empty buzzwords ("results-driven", "cutting-edge", "synergy", "unprecedented ROI") and replaces them with verifiable numbers (30,000 pages, 2.8× lift), concrete methodology (no target leakage), and disciplined scientific framing.
