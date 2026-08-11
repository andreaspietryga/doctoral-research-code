# Doctoral Research Code

Research code supporting my doctoral dissertation in Computational Economics
at Bielefeld University:

**Advancing the Next Industrial Revolution: The Role of AI, Smart Products,
and Algorithmic Decision Making**

This repository contains the computational implementations developed and used
across three dissertation projects. The research combines reinforcement
learning, dynamic optimization, simulation, game theory, and algorithm design
to study sequential decision problems under uncertainty.

All dissertation code included in this repository is functional and was used
in the underlying doctoral research.

## Research Projects

### 1. [The Optimal Timing of Product Introduction and Safety Investments for Automated Vehicles](./paper-1-optimal-timing/)

This project studies how liability regulation affects safety investment and
market-introduction decisions for autonomous vehicles.

The research develops dynamic analytical and numerical models under
deterministic and stochastic liability and examines both open-loop and
state-dependent Markov investment strategies.

The analysis studies how liability allocation and the timing of market
introduction affect safety investment, accident risk, producer profits,
and social welfare.

**Methods:** Dynamic Optimization, Optimal Control, Open-Loop Strategies,
Markov Strategies, Numerical Optimization, Stochastic Modeling, Welfare Analysis

---

### 2. [Safety Investment and Market Introduction of Automated Vehicles: An Analysis of Endogenous Training Effects](./paper-2-endogenous-training/)

This project develops a two-stage framework linking autonomous-vehicle learning
with dynamic investment decisions.

In the first stage, a TD(0)-Search-based learning algorithm simulates the
learning process of an autonomous vehicle in a stylized road environment.
The simulations generate realized performance observations including
accidents, inappropriate driving, and driving steps.

These performance outcomes are used as inputs to a dynamic investment problem.

In the second stage, a predetermined open-loop investment strategy is compared
with adaptive, state-dependent investment approaches based on the Dyna-2
reinforcement learning algorithm.

**Methods:** TD(0)-Search, Dyna-2, Reinforcement Learning, Model-Based Planning,
Simulation, Dynamic Optimization, Sequential Decision-Making

---

### 3. [Collusion under Algorithmic Pricing: How Robust Is It?](./paper-3-algorithmic-collusion/)

This project investigates algorithmic collusion among reinforcement-learning
pricing agents.

It includes implementations of standard Tabular Q-Learning as well as
**Smooth Q-Learning** and **Smooth Dyna-Q**, two algorithms developed as part
of the doctoral research to mitigate collusive behavior and promote convergence
toward competitive Nash equilibria in the tested pricing environments.

Smooth Q-Learning introduces a smoothing mechanism inspired by Smooth UCT.
Smooth Dyna-Q extends this approach with a model-based planning component to
improve learning efficiency and convergence behavior.

The algorithms are evaluated in both potential and non-potential pricing games,
including the pricing environment studied by Calvano et al. (2020). The
experiments also consider asymmetric settings in which only one interacting
agent uses Smooth Dyna-Q.

**Methods:** Tabular Q-Learning, Smooth Q-Learning, Dyna-Q, Smooth Dyna-Q,
Multi-Agent Reinforcement Learning, Model-Based Planning, Game Theory,
Algorithmic Pricing

---

## Repository Structure

```text
doctoral-research-code/
│
├── README.md
│
├── paper-1-optimal-timing/
│   ├── README.md
│   └── *.nb
│
├── paper-2-endogenous-training/
│   ├── README.md
│   └── *.nb
│
└── paper-3-algorithmic-collusion/
    ├── README.md
    └── *.nb
```

Each project directory contains the corresponding Wolfram Mathematica
implementations together with detailed documentation of the research question,
methods, computational experiments, software requirements, and main results.

Click on any of the three project titles above to access the corresponding
project directory and its detailed README.

## Software

The original dissertation implementations were developed primarily in
**Wolfram Mathematica**.

All Mathematica notebooks currently included in this repository have been
tested successfully with **Wolfram Mathematica 14**.

Selected reinforcement-learning algorithms are currently being translated and
extended in **Python** as part of continued research and development.

## Research Areas

- Reinforcement Learning
- Multi-Agent Reinforcement Learning
- Model-Based Reinforcement Learning
- Dynamic Optimization
- Optimal Control
- Sequential Decision-Making
- Game Theory
- Algorithm Design
- Algorithmic Pricing
- Autonomous Systems
- Simulation
- Computational Economics

## Repository Navigation

| Project | Main Topics |
| --- | --- |
| [Paper 1 – Optimal Timing and Safety Investment](./paper-1-optimal-timing/) | Dynamic Optimization, Liability, Optimal Control, Welfare |
| [Paper 2 – Endogenous Training Effects](./paper-2-endogenous-training/) | TD(0)-Search, Dyna-2, Simulation, Adaptive Investment |
| [Paper 3 – Algorithmic Collusion](./paper-3-algorithmic-collusion/) | Q-Learning, Smooth Q-Learning, Smooth Dyna-Q, Multi-Agent RL |

## Author

**Andreas Pietryga, Dr. rer. pol.**

Computational Economics  
Bielefeld University

[LinkedIn](https://www.linkedin.com/in/andreaspietryga)
