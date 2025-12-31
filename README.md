# Belief Dynamics

Learning, Convergence, and Collapse in Human Forecasting Systems

## Research Overview

This repository studies how collective beliefs evolve over time in real-world forecasting systems. Rather than treating market prices as financial signals, we interpret them as probabilistic belief states—dynamic estimates produced by many agents operating under uncertainty.

The central focus is not prediction accuracy, but belief dynamics:

- How uncertainty is reduced
- How competing hypotheses are eliminated
- How belief systems transition from exploration to certainty

Prediction markets serve as a measurement device for these processes, providing high-frequency, incentive-aligned traces of human belief updating.

## Core Research Question

**How do collective belief systems converge—and sometimes collapse—when exposed to discrete information shocks?**

We approach this question by modeling belief evolution as a stochastic process with absorbing states, where uncertainty collapses into near-certainty once sufficient information is revealed.

## Conceptual Grounding

This project is grounded in a structured synthesis of literature on:

- Bayesian updating and belief aggregation
- Prediction markets and information efficiency
- Failure modes of human forecasting systems

NotebookLM is used explicitly as a research support tool to extract assumptions, known limitations, and conceptual frameworks from prior work. All interpretations and formalizations are human-authored and critically evaluated.

Key themes identified include:

- Delayed belief updating under uncertainty
- Abrupt belief revision following credible signals
- Structural inertia due to liquidity, coordination, and institutional constraints

## Empirical Case Study: Federal Reserve Rate Cut Markets

As an empirical substrate, we analyze Federal Reserve interest rate prediction markets. These markets are well-suited for studying belief dynamics because:

- Information arrives in bursts (FOMC meetings, speeches)
- Multiple competing hypotheses coexist (e.g., 2 vs. 3 vs. 4 cuts)
- Outcomes resolve discretely, enabling clear observation of convergence

Market price trajectories are treated as belief paths, not investment signals.

## Observed Belief Phenomena

Across examined markets, we observe recurring structural patterns:

- Gradual belief drift during periods of weak or ambiguous information
- Abrupt belief collapse following decisive announcements
- Absorbing states where uncertainty vanishes and prices stabilize near certainty
- Liquidity decay once disagreement is eliminated

These behaviors align closely with theoretical expectations from the belief aggregation literature.

## Modeling Perspective

Rather than optimizing predictive accuracy, we focus on characterization:

- Belief volatility and decay
- Update frequency and inactivity regimes
- Transitions between exploratory and settled belief states

This framing emphasizes learning dynamics, making the project relevant to machine learning, statistical inference, and computational social science.

## Technical Implementation

The repository includes a robust data pipeline for extracting high-frequency belief trajectories from the Kalshi v2 API using secure RSA-PSS authentication.

The codebase exists to:

- Enable reproducible empirical analysis
- Support diagnostic visualization
- Export clean time-series data for further study

The technical stack is intentionally lightweight and transparent.

## Research Scope & Non-Claims

- **Not a trading system**: No strategies are optimized for profit
- **Not outcome prediction**: The goal is to study belief formation, not to forecast economic events
- **Case-study driven**: Empirical results illustrate general dynamics rather than universal laws

## Future Directions

- Comparative analysis of converging vs. collapsing belief trajectories
- Cross-domain validation in other forecasting environments
- Formal links to stochastic learning models and Bayesian convergence theory
