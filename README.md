# Reza Azad Gholami

I am an applied mathematician and AI engineer based in Bergen, Norway. My work sits at the intersection of uncertainty modelling, stochastic optimisation, and machine learning.

My entry point was fluid mechanics and aerodynamics. CFD taught me that physical models are never exact. Turbulence is inherently stochastic, boundary conditions carry uncertainty, and resolving fine-scale phenomena is often computationally prohibitive. My early research used neural networks as surrogate models to accelerate aerodynamic shape optimisation, replacing expensive CFD evaluations with learned approximations while preserving physical consistency. The core problem was always the same: how do you reason reliably when your model is expensive, noisy, or partially wrong?

That question carried naturally into stochastic optimisation. My PhD at NHH built algorithms for multi-period decision problems where demand, prices, and competitor behaviour are all uncertain. The mathematical tools shifted from PDEs and numerical grids to dynamic programming, bilevel games, and equilibrium computation under stochastic dynamics, but the underlying concern stayed the same. A recurring theme in that work is the value of adapting decisions as uncertainty resolves, rather than committing to a fixed plan in advance, a principle that turns out to matter well beyond supply chains.

At NORCE, I applied Bayesian deep learning to problems where uncertainty quantification is not optional: market volatility prediction, drilling diagnostics, and meteorological forecasting. These are settings where a point prediction without a confidence estimate is not just incomplete but potentially dangerous. That work sharpened my thinking about what it means to produce reliable outputs from learned models.

My MSc at UiB brought this into scientific machine learning, with a thesis on transformer models for integrating marine camera and acoustic data. More recently I have been building agentic AI systems for financial risk analysis, and applying reinforcement learning to decision-making under uncertainty in logistics, where the same principles apply at the system level: grounded outputs, bounded autonomy, and honest uncertainty disclosure at every step.

---

### Featured projects

**[Agentic Financial Risk Assistant](https://github.com/eigenreza/agentic-financial-risk-assistant)**
A production-style prototype for uncertainty-aware financial risk analysis. The system uses a LangChain agent over controlled Python tools, an MCP-style access layer, RAG over methodology documents, and a safety layer that maps user requests to EU AI Act risk tiers. Analysis runs on Equinor, Brent crude, and USD/NOK time series. The design reflects a conviction that AI systems handling consequential questions should be transparent about what they computed, what they retrieved, and where their confidence ends. The system is deployed live on Azure, and you can [try it here](https://financial-risk-assistant.salmonsmoke-c7ee3b6a.westeurope.azurecontainerapps.io/). 

**[Proactive-Reactive Routing under Stochastic Returns](https://github.com/eigenreza/proactive-reactive-rl-routing)**
A two-stage optimisation framework for reverse logistics collection routing under uncertain product return flows, motivated by end-of-life EV battery collection. A proactive stage solves a capacitated vehicle routing problem on expected returns, and a reactive Q-learning stage adapts the routes once realised returns are observed each day. Across Monte Carlo evaluation, the two-stage policy reduces empty trips by more than 98% relative to fixed planning at high uncertainty, with the advantage growing as returns become harder to predict. The framework runs as an [interactive web application](https://proactive-reactive-rl-routing-dmcswxot8epaarzazyvbgm.streamlit.app/) where the uncertainty level and learning parameters can be varied in real time.

---

### Background

- Postdoctoral Scientist, Bayesian Deep Learning, NORCE Norwegian Research Centre
- PhD, Operations Research / Applied Mathematics, NHH Norwegian School of Economics
- MSc, Applied and Computational Mathematics, University of Bergen, Bergen, Norway
