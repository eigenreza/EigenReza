# Reza Azad Gholami

I am an applied mathematician and AI engineer based in Bergen, Norway. My work sits at the intersection of uncertainty modelling, stochastic optimisation, and machine learning.

My entry point was fluid mechanics and aerodynamics. CFD taught me that physical models are never exact. Turbulence is inherently stochastic, boundary conditions carry uncertainty, and resolving fine-scale phenomena is often computationally prohibitive. My early research used neural networks as surrogate models to accelerate aerodynamic shape optimisation, replacing expensive CFD evaluations with learned approximations while preserving physical consistency. The core problem was always the same: how do you reason reliably when your model is expensive, noisy, or partially wrong?

That question carried naturally into stochastic optimisation. My PhD at NHH built algorithms for multi-period decision problems where demand, prices, and competitor behaviour are all uncertain. The mathematical tools shifted from PDEs and numerical grids to dynamic programming, bilevel games, and equilibrium computation under stochastic dynamics, but the underlying concern stayed the same.

At NORCE, I applied Bayesian deep learning to problems where uncertainty quantification is not optional: market volatility prediction, drilling diagnostics, and meteorological forecasting. These are settings where a point prediction without a confidence estimate is not just incomplete but potentially dangerous. That work sharpened my thinking about what it means to produce reliable outputs from learned models.

My MSc at UiB brought this into scientific machine learning, with a thesis on transformer models for integrating marine camera and acoustic data. More recently I have been building agentic AI systems for financial risk analysis, where the same principles apply at the system level: grounded outputs, bounded autonomy, and honest uncertainty disclosure at every step.

---

### Featured project

**[Agentic Financial Risk Assistant](https://github.com/eigenreza/agentic-financial-risk-assistant)**

A production-style prototype for uncertainty-aware financial risk analysis. The system uses a LangChain agent over controlled Python tools, an MCP-style access layer, RAG over methodology documents, and a safety layer that maps user requests to EU AI Act risk tiers. Analysis runs on Equinor, Brent crude, and USD/NOK time series. The design reflects a conviction that AI systems handling consequential questions should be transparent about what they computed, what they retrieved, and where their confidence ends.

---

### Background

- Postdoctoral Scientist, Bayesian Deep Learning, NORCE Norwegian Research Centre
- PhD, Operations Research / Applied Mathematics, NHH Norwegian School of Economics
- MSc, Applied and Computational Mathematics, University of Bergen
