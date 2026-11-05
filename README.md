# Reza Azad Gholami

I'm an applied mathematician and AI engineer based in Bergen, Norway. Most of my work has been about making good decisions and good predictions when the world is uncertain, and I have come at that from stochastic optimization, dynamic and differential games, and machine learning.

I started out in fluid mechanics and aerodynamics. Working with CFD, I learned early that a physical model is never quite exact: turbulence is partly random, boundary conditions are never known precisely, and resolving the fine details is often too expensive to do more than a few times. My early research trained neural networks to stand in for those expensive simulations, so that an aerodynamic shape could be optimized without a full CFD solve for every candidate. Looking back, the question underneath it was already the one I keep returning to: how do you reason well when your model is costly, noisy, or partly wrong?

That question took me into stochastic optimization. In my PhD at NHH I built algorithms for decisions spread over many periods, where demand, prices, and the behavior of competitors are all uncertain. The tools changed from PDEs and numerical grids to dynamic programming, bilevel games, and equilibrium computation, but the concern stayed the same. The idea I kept coming back to was how much is gained by adapting decisions as the uncertainty resolves, instead of committing to a fixed plan up front, and I have since seen it matter far beyond supply chains.

At NORCE I moved to Bayesian deep learning, on problems where knowing how far to trust a prediction matters as much as the prediction itself: market volatility, drilling diagnostics, and weather forecasting. In settings like these, a forecast without a sense of its own reliability can do real harm, and that experience has shaped how I think about learned models ever since.

My master's at UiB then took me into scientific machine learning, with a thesis on transformer models that combine underwater camera and acoustic data. More recently I have been building agentic AI systems for financial risk analysis and using reinforcement learning for decisions under uncertainty in logistics. In both, I care about the same things: answers grounded in real computation, clear limits on what an agent is allowed to do, and uncertainty that is stated honestly.

My most recent work follows a thread from my PhD into continuous time. The multi-period games I studied there are dynamic games played in discrete steps; let the steps shrink and you arrive at differential games, the field Rufus Isaacs built around the problem of pursuit, using a continuous-time form of the same dynamic programming. Pursuit also asks, in a very physical form, the question that ran through my PhD: when to commit to a prediction, and when to keep adapting to what you see. A chasing animal faces exactly that choice, running either at where its target is or at where it is about to be, so I set out to measure which of the two real animals actually do. The result is a study of about 13,900 tracked mouse chases.

---

### Featured projects

Most of the projects below grew out of questions from my earlier or ongoing research.

**[Agentic Financial Risk Assistant](https://github.com/eigenreza/agentic-financial-risk-assistant)**
A production-style prototype for uncertainty-aware financial risk analysis. The system uses a LangChain agent over controlled Python tools, an MCP access layer, RAG over methodology documents, and a safety layer that maps user requests to EU AI Act risk tiers. Analysis runs on sample series for Equinor, Brent crude, and USD/NOK, and can switch to real market data. The design reflects a conviction that AI systems handling consequential questions should be transparent about what they computed, what they retrieved, and where their confidence ends. The system is deployed live on Azure, and you can [try it here](https://financial-risk-assistant.salmonsmoke-c7ee3b6a.westeurope.azurecontainerapps.io/).

**[Annual Report Intelligence](https://github.com/eigenreza/annual-report-intelligence)**
Question answering over company annual reports with cited, document-grounded answers. It parses text and tables from PDF and Word files, combines embedding and keyword search (FAISS and BM25), and checks every cited figure against the retrieved text. It is evaluated on a set of analyst questions that include deliberate traps, with the results and a failure analysis in the README.

**More AI engineering**
- [nl-to-app-model](https://github.com/eigenreza/nl-to-app-model): an agentic system that turns natural-language descriptions into validated, editable application models.
- [schema-constrained-extraction](https://github.com/eigenreza/schema-constrained-extraction): an empirical study of schema-constrained LLM extraction from regulatory text.

**Data and forecasting**
- [AquaRisk Norway](https://github.com/eigenreza/aquarisk-norway): Bayesian spatiotemporal inference and early warning for salmon-lice pressure in Norwegian aquaculture.
- [CoastCast Vestland](https://github.com/eigenreza/coastcast-vestland): coastal water-level forecasting with calibrated uncertainty for Vestland, Norway.
- [Calibrated Graph Forecasting](https://github.com/eigenreza/calibrated-graph-forecasting): a graph neural network weather forecaster on ERA5 data, testing how reliable its uncertainty estimates stay for extremes at longer lead times.

**Research**
- [Visual Transformers for Deep Vision and Acoustic Data](https://github.com/eigenreza/visual-transformers-deep-vision-acoustic): my UiB master's thesis, linking underwater camera images with echosounder data.
- [Hydro Stochastic Scheduling](https://github.com/eigenreza/hydro-stochastic-scheduling): the value of operational flexibility in stochastic hydropower reservoir scheduling, with a 22-year backtest on the Arendalsvassdraget system.
- [Proactive-Reactive Routing](https://github.com/eigenreza/proactive-reactive-rl-routing): a two-stage routing framework for EV battery collection under stochastic returns, combining vehicle routing with Q-learning ([interactive app](https://proactive-reactive-rl-routing-dmcswxot8epaarzazyvbgm.streamlit.app/)).
- [Anticipate or React? Markov-Switching Pursuit](https://github.com/eigenreza/markov-switching-pursuit): a hidden Markov model over classical pursuit guidance laws, fitted to about 13,900 real mouse chases ([preprint](https://github.com/eigenreza/markov-switching-pursuit/blob/main/paper/main.pdf), [interactive demo](https://markov-switching-pursuit.streamlit.app)).

---

### Background

- Postdoctoral Scientist, Bayesian Deep Learning, NORCE Norwegian Research Centre
- PhD, Operations Research / Applied Mathematics, NHH Norwegian School of Economics
- MSc, Applied and Computational Mathematics, University of Bergen, Bergen, Norway
