# Reza Azad Gholami

I'm an applied mathematician and AI engineer based in Bergen, Norway. Most of my work has been about making good decisions and good predictions when the world is uncertain, and I have come at that from stochastic optimization, dynamic and differential games, and machine learning.

I started out in fluid mechanics and aerodynamics. Working with CFD, I learned early that a physical model is never quite exact: turbulence is partly random, boundary conditions are never known precisely, and resolving the fine details is often too expensive to do more than a few times. My early research trained neural networks to stand in for those expensive simulations, so that an aerodynamic shape could be optimized without a full CFD solve for every candidate. Looking back, the question underneath it was already the one I keep returning to: how do you reason well when your model is costly, noisy, or partly wrong?

That question took me into stochastic optimization. In my PhD at NHH I built algorithms for decisions spread over many periods, where demand, prices, and the behavior of competitors are all uncertain. The tools changed from PDEs and numerical grids to dynamic programming, bilevel games, and equilibrium computation, but the concern stayed the same. The idea I kept coming back to was how much is gained by adapting decisions as the uncertainty resolves, instead of committing to a fixed plan up front, and I have since seen it matter far beyond supply chains.

At NORCE I moved to Bayesian deep learning, on problems where knowing how far to trust a prediction matters as much as the prediction itself: market volatility, drilling diagnostics, and weather forecasting. In settings like these, a forecast without a sense of its own reliability can do real harm, and that experience has shaped how I think about learned models ever since.

My master's at UiB then took me into scientific machine learning, with a thesis on transformer models that combine underwater camera and acoustic data. More recently I have been building agentic AI systems for financial risk analysis and using reinforcement learning for decisions under uncertainty in logistics. In both, I care about the same things: answers grounded in real computation, clear limits on what an agent is allowed to do, and uncertainty that is stated honestly.

My most recent work follows a thread from my PhD into continuous time. The multi-period games I studied there are dynamic games played in discrete steps; let the steps shrink and you arrive at differential games, the field Rufus Isaacs built around the problem of pursuit, using a continuous-time form of the same dynamic programming. Pursuit also asks, in a very physical form, the question that ran through my PhD: when to commit to a prediction, and when to keep adapting to what you see. A chasing animal faces exactly that choice, running either at where its target is or at where it is about to be, so I set out to measure which of the two real animals actually do. The result is a study of about 13,900 tracked mouse chases, which you will find first among the projects below.

---

### Featured projects

**[Anticipate or React? Markov-Switching Pursuit](https://github.com/eigenreza/markov-switching-pursuit)**
A hidden Markov model over the classical guidance laws of pursuit (pure pursuit, lead pursuit, and proportional navigation) that infers, moment by moment, which steering rule a chasing animal is using and what makes it switch. The model is validated on simulated chases with known switches, then fitted to about 13,900 real chases from three open datasets of mice hunting crickets and mice chasing mice. Mice mostly react: they steer in short bursts of pure pursuit with a delay of 33 to 67 ms, yet catch their target in only 12 to 15 percent more time than the optimal pursuer of Isaacs' pursuit game. The [preprint (PDF)](https://github.com/eigenreza/markov-switching-pursuit/blob/main/paper/main.pdf), the code, and an [interactive demo](https://markov-switching-pursuit.streamlit.app), where you can build a chase and watch the model infer the switches, are all public.

**[Agentic Financial Risk Assistant](https://github.com/eigenreza/agentic-financial-risk-assistant)**
A production-style prototype for uncertainty-aware financial risk analysis. The system uses a LangChain agent over controlled Python tools, an MCP-style access layer, RAG over methodology documents, and a safety layer that maps user requests to EU AI Act risk tiers. Analysis runs on Equinor, Brent crude, and USD/NOK time series. The design reflects a conviction that AI systems handling consequential questions should be transparent about what they computed, what they retrieved, and where their confidence ends. The system is deployed live on Azure, and you can [try it here](https://financial-risk-assistant.salmonsmoke-c7ee3b6a.westeurope.azurecontainerapps.io/).

**[Proactive-Reactive Routing under Stochastic Returns](https://github.com/eigenreza/proactive-reactive-rl-routing)**
A two-stage optimization framework for reverse logistics collection routing under uncertain product return flows, motivated by end-of-life EV battery collection. A proactive stage solves a capacitated vehicle routing problem on expected returns, and a reactive Q-learning stage adapts the routes once realized returns are observed each day. Across Monte Carlo evaluation, the two-stage policy reduces empty trips by more than 98% relative to fixed planning at high uncertainty, with the advantage growing as returns become harder to predict. The framework runs as an [interactive web application](https://proactive-reactive-rl-routing-dmcswxot8epaarzazyvbgm.streamlit.app/) where the uncertainty level and learning parameters can be varied in real time.

---

### Background

- Postdoctoral Scientist, Bayesian Deep Learning, NORCE Norwegian Research Centre
- PhD, Operations Research / Applied Mathematics, NHH Norwegian School of Economics
- MSc, Applied and Computational Mathematics, University of Bergen, Bergen, Norway
