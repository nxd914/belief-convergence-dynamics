# Belief Dynamics

**Learning, Convergence, and Collapse in Human Forecasting Systems**

## Overview

This repository studies how collective beliefs evolve over time in real-world forecasting environments.

Rather than treating prediction market prices as financial signals, we interpret them as **probabilistic belief states**—dynamic estimates produced by many agents operating under uncertainty.

The core objective is not prediction accuracy, but **belief dynamics**:
- How uncertainty is reduced
- How competing hypotheses coexist and are eliminated
- How belief systems transition from disagreement to consensus
- When convergence occurs—and when it fails to occur

Prediction markets serve as a measurement device for these processes, providing high-frequency, incentive-aligned traces of human belief updating.

## Core Research Question

**How do collective belief systems converge—and sometimes fail to converge—when exposed to discrete information shocks?**

We study belief evolution as a stochastic process with possible absorbing states, where uncertainty collapses into near-certainty once sufficient information is revealed.

## Conceptual Framing

This project is grounded in ideas from:
- Bayesian updating and belief aggregation
- Prediction markets and information efficiency
- Collective learning under uncertainty
- Failure modes of human forecasting systems

Belief trajectories are treated as objects of study, not inputs to trading strategies.

## Empirical Approach

### Data Source

We analyze historical Kalshi prediction markets, focusing exclusively on finalized (resolved) markets.

These markets are well-suited for belief analysis because:
- Information arrives in bursts (announcements, votes, decisions)
- Multiple competing hypotheses coexist
- Outcomes resolve discretely
- Belief collapse (or non-collapse) can be clearly observed

### What We Measure

For each market, we extract a high-frequency belief trace and compute diagnostic metrics, including:
- **Belief volatility** (average magnitude of belief updates)
- **Maximum belief jump** (largest single update)
- **Inactivity fraction** (periods of belief stasis)
- **Collapse time** (if and when belief enters a high-certainty absorbing state)

Importantly, collapse is not assumed—it is detected.

## Key Findings

Across examined cases, we observe distinct belief regimes:

### 1. Collapse Dynamics

Some belief systems exhibit:
- Extended disagreement
- Sparse or delayed updating
- Abrupt belief collapse following decisive information
- Rapid stabilization near certainty

### 2. Non-Collapse Dynamics

Other systems show:
- Continuous belief movement
- Persistent disagreement
- No absorbing state prior to resolution
- Ongoing uncertainty even late in the timeline

The existence of both regimes suggests that belief convergence is not guaranteed, even in incentive-aligned environments.

## What This Project Is Not

To avoid confusion, this repository explicitly makes **no claims** about:
- Trading strategies
- Alpha generation
- Forecasting superiority
- Market inefficiency exploitation

This is a descriptive and analytical study of learning dynamics, not a financial system.

## Technical Implementation

The codebase provides:
- Secure access to Kalshi's v2 API using RSA-PSS authentication
- A reusable, domain-agnostic pipeline for extracting belief traces
- Clean CSV exports for reproducibility
- Lightweight analysis and visualization tools

The same pipeline is applied unchanged across all case studies; only the market identifiers differ.

## Reproducibility

Each case study consists of:
- A finalized market identifier
- A fixed observation window
- A belief trace CSV
- Deterministic analysis code

All results can be reproduced by re-running the notebooks top-to-bottom.

## Future Directions

Planned extensions include:
- Comparative analysis across many domains
- Cross-case clustering of belief dynamics
- Integration of external attention signals (e.g., search interest)
- Formal links to stochastic learning models and Bayesian convergence theory

## High-Level Takeaway

Even when incentives are aligned and information is public, collective belief systems can behave very differently—sometimes converging abruptly, sometimes never fully agreeing at all.

This repository provides a framework for measuring and comparing those dynamics.
