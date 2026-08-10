# Doctoral Research Code

Research code supporting my doctoral dissertation in Computational Economics
at Bielefeld University:

**Advancing the Next Industrial Revolution: The Role of AI, Smart Products,
and Algorithmic Decision Making**

This repository contains the computational implementations developed and used
across three dissertation projects. The research combines reinforcement learning,
dynamic optimization, simulation, game theory, and algorithm design to study
sequential decision problems under uncertainty.

All dissertation code included in this repository is functional and was used
in the underlying doctoral research.

## Research Projects

### 1. The Optimal Timing of Product Introduction and Safety Investments for Automated Vehicles

This project studies how liability regulation affects safety investment and
market-introduction decisions for autonomous vehicles.

The research develops analytical dynamic models under deterministic and
stochastic liability and examines both open-loop and Markov investment
strategies.

**Methods:** Dynamic Optimization, Optimal Control, Open-Loop Strategies,
Markov Strategies, Stochastic Modeling, Welfare Analysis

---

### 2. Safety Investment and Market Introduction of Automated Vehicles:
### An Analysis of Endogenous Training Effects

This project develops a two-stage framework linking autonomous-vehicle learning
with dynamic investment decisions.

In the first stage, a TD(0)-Search algorithm simulates the learning process of
an autonomous vehicle. Performance measures such as accident rates, traffic
violations, and completion times are then used as inputs into a dynamic
investment problem.

The project compares an open-loop investment strategy with a state-dependent
approach based on the Dyna-2 reinforcement learning algorithm.

**Methods:** TD(0)-Search, Dyna-2, Reinforcement Learning, Simulation,
Dynamic Optimization

---

### 3. Collusion under Algorithmic Pricing: How Robust Is It?

This project investigates algorithmic collusion among reinforcement-learning
pricing agents.

It includes implementations of standard tabular Q-Learning as well as
Smooth Q-Learning and Smooth Dyna-Q, two algorithms developed as part of the
doctoral research to mitigate collusive behavior and promote convergence toward
competitive Nash equilibria in the tested pricing environments.

Smooth Dyna-Q combines reinforcement learning with a model-based planning
component to improve learning efficiency and convergence behavior.

The algorithms are evaluated in both potential and non-potential pricing games,
including the pricing environment studied by Calvano et al. (2020).

**Methods:** Q-Learning, Dyna-Q, Smooth Q-Learning, Smooth Dyna-Q,
Multi-Agent Reinforcement Learning, Model-Based Planning, Algorithmic Pricing

---

## Repository Structure

```text
doctoral-research-code/
│
├── README.md
│
├── paper-1-optimal-timing/
│   ├── README.md
│   └── code/
│
├── paper-2-endogenous-training/
│   ├── README.md
│   └── code/
│
└── paper-3-algorithmic-collusion/
    ├── README.md
    └── code/
