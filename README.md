# Doctoral Research Code

Research code supporting my doctoral dissertation in Computational Economics
at Bielefeld University:

**Advancing the Next Industrial Revolution: The Role of AI, Smart Products,
and Algorithmic Decision Making**

This repository contains the functional Wolfram Mathematica implementations
used in three dissertation papers. The projects combine reinforcement learning,
dynamic optimization, simulation, game theory, and algorithm design to study
sequential decision problems under uncertainty.

## Research Projects

### 1. Optimal Timing of Product Introduction and Safety Investments
Analytical dynamic models of safety investment and autonomous-vehicle market
introduction under deterministic and stochastic liability regulation.

**Methods:** dynamic optimization, optimal control, open-loop strategies,
Markov strategies, welfare analysis.

### 2. Safety Investment and Market Introduction under Endogenous Training
A two-stage framework combining autonomous-vehicle learning simulations with
dynamic investment optimization.

The first stage uses TD(0)-Search to model vehicle learning. The resulting
performance data are used in a second-stage investment problem. A Dyna-2
approach provides state-dependent investment decisions and is compared with
an open-loop benchmark.

**Methods:** TD(0)-Search, Dyna-2, simulation, reinforcement learning,
dynamic optimization.

### 3. Collusion under Algorithmic Pricing
Research on tacit collusion among reinforcement-learning pricing agents.

The project includes implementations of tabular Q-learning and the proposed
Smooth Q-Learning and Smooth Dyna-Q algorithms. The algorithms are evaluated
in both potential and non-potential pricing environments.

**Methods:** Q-learning, Dyna-Q, Smooth Q-Learning, Smooth Dyna-Q,
multi-agent reinforcement learning, algorithmic pricing.

## Software

The original dissertation code was developed in **Wolfram Mathematica**.
Python implementations of selected algorithms are currently being developed
as extensions of the doctoral research.

## Repository Structure

- `paper-1-optimal-timing/` — analytical safety-investment and welfare models
- `paper-2-endogenous-training/` — AV learning simulations and investment models
- `paper-3-algorithmic-collusion/` — Q-learning and Smooth Dyna-Q experiments

## Author

**Andreas Pietryga, Dr. rer. pol.**

Computational Economics  
Bielefeld University

LinkedIn: https://www.linkedin.com/in/andreaspietryga
