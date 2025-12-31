# Belief Dynamics

**Learning, Convergence, and Collapse in Human Forecasting Systems**

---

## Overview

This repository studies **how collective beliefs evolve over time** in real-world forecasting systems. Rather than treating prediction market prices as financial or trading signals, we interpret them as **probabilistic belief states**—dynamic estimates produced by many agents operating under uncertainty.

The emphasis is **not prediction accuracy**, but **belief dynamics**:

- How uncertainty is reduced
- How disagreement persists
- How belief systems abruptly converge
- When learning occurs—and when it fails

Prediction markets serve as a **measurement device** for these processes, providing high-frequency, incentive-aligned traces of belief updating.

---

## Core Research Question

**How do collective belief systems converge—and sometimes fail to converge—when exposed to discrete information shocks?**

Belief evolution is treated as a stochastic process with potential **absorbing states**, where uncertainty collapses into near-certainty once sufficient information is revealed.

---

## Conceptual Framing

This project is grounded in ideas from:

- Bayesian updating and belief aggregation
- Prediction markets as information aggregation mechanisms
- Learning under uncertainty
- Failure modes of human forecasting systems

Belief trajectories are analyzed as **learning paths**, not as financial opportunities.

NotebookLM was used strictly as a **research support tool** to extract assumptions, limitations, and conceptual frameworks from existing literature. All interpretations, metrics, and conclusions are human-authored.

---

## Data Sources

### 1. Kalshi Prediction Markets (Primary Data)

Kalshi markets provide structured belief traces with clear resolution events. Market prices are interpreted as probabilistic beliefs.

The following notebooks analyze **Kalshi belief dynamics only**, without external signals:

- **Cuomo NYC Mayoral Race** (`belief_convergence_cuomo.ipynb`)
  - Extended uncertainty window
  - Gradual belief drift
  - Sharp convergence near resolution

- **Papal Election (Conclave)** (`belief_convergence_pope.ipynb`)
  - Extremely rapid information resolution
  - Minimal exploration phase
  - Near-immediate belief collapse

- **Epstein House Vote Markets** (`belief_convergence_eps.ipynb`)
  - Degenerate or inactive belief regimes
  - Little sustained disagreement
  - Immediate or near-immediate resolution

These case studies intentionally span **distinct belief regimes**, rather than representing a single narrative.

Corresponding belief traces:
- `belief_trace__kalshi__cuomo.csv`
- `belief_trace__kalshi__pope.csv`
- `belief_trace__kalshi__house.csv`

---

### 2. Google Trends (Secondary Attention Signal)

Google Trends data are introduced **only in the merge notebook** to contextualize belief dynamics with public attention.

The notebook:
- **`belief_convergence_merge.ipynb`**

This notebook aligns:
- Kalshi belief trajectories
- Weekly Google Trends time series

to examine the relationship between:
- Attention spikes
- Belief convergence timing
- Post-resolution attention decay

Included Google Trends files:
- `cuomo_grends_timeline.csv` *(filename preserved as uploaded)*
- `pope_gtrends_timeline.csv`
- `epstein_gtrends_timeline.csv`

Google Trends is treated strictly as a **secondary, coarse attention proxy**, not as a predictive signal.

---

## Belief Dynamics Metrics

The analysis emphasizes **diagnostic**, not predictive, metrics:

- Mean belief volatility
- Maximum belief jump
- Inactivity fraction
- Observation count
- Estimated belief collapse time

These metrics enable **cross-case comparison** across markets with very different timelines and structures.

---

## Key Observations

Across examined cases, three recurring regimes emerge:

1. **Exploratory → Convergent Learning**
   - Prolonged disagreement
   - Gradual volatility decay
   - Sudden collapse into consensus

2. **Immediate Resolution**
   - Minimal disagreement
   - Abrupt belief locking
   - No extended learning phase

3. **Degenerate / No Learning**
   - Low activity
   - Static beliefs
   - No meaningful convergence process

A key negative result is that **not all forecasting environments generate learning dynamics**.

The merge analysis further suggests that **public attention often peaks before belief convergence**, and may decay even as beliefs stabilize.

---

## What This Project Is Not

- ❌ Not a trading strategy
- ❌ Not a forecasting system
- ❌ Not a claim of market efficiency

The goal is **characterization of belief formation**, not optimization or outcome prediction.

---

## Repository Structure

### Notebooks

- `belief_convergence_cuomo.ipynb` — Kalshi-only analysis
- `belief_convergence_pope.ipynb` — Kalshi-only analysis
- `belief_convergence_eps.ipynb` — Kalshi-only analysis
- `belief_convergence_merge.ipynb` — Kalshi + Google Trends integration

### Data

- Kalshi belief traces (`belief_trace__kalshi__*.csv`)
- Google Trends timelines (`*_gtrends_timeline.csv`)

---

## Research Status

This repository represents an **exploratory but structured research program**.

Current contributions:
- A reusable pipeline for belief-trace extraction
- Empirical identification of belief convergence regimes
- Contextual validation using external attention data

Planned extensions:
- Additional resolved markets
- Formal stochastic models of belief collapse
- Cross-domain validation beyond prediction markets

---

## Takeaway

> Collective belief systems do not always learn.  
> When they do, convergence follows a measurable and structured process.

This repository provides a framework for studying that process.
