# The Optimal Timing of Product Introduction and Safety Investments for Automated Vehicles

## Overview

This directory contains the Wolfram Mathematica implementations supporting the
first paper of my doctoral dissertation in Computational Economics.

The research examines how liability regulation affects a monopolistic producer's
safety investments and the timing of market introduction of autonomous vehicles.

The model combines dynamic investment decisions, accident risk, market demand,
liability allocation, and welfare analysis over a finite planning horizon.

## Research Questions

The analysis investigates how alternative liability regimes affect:

- optimal safety investment,
- the timing of market introduction,
- accident probabilities,
- producer profits,
- and social welfare.

The framework considers both deterministic liability and uncertainty regarding
future liability regulation.

## Code Files

### `deterministic-liability-welfare.nb`

Implements the deterministic-liability benchmark and computes the corresponding
investment and welfare outcomes.

### `open-loop-welfare.nb`

Implements the investment problem under uncertainty using an open-loop strategy.

Future investment decisions are determined without conditioning them on the
subsequently realized state.

### `markov-welfare.nb`

Implements the investment problem using state-dependent Markov strategies.

Investment decisions can therefore respond to the realized state of the system.

## Main Results

The analysis shows that liability regulation can affect safety investment in
non-monotonic ways.

In particular:

- stronger producer liability does not necessarily increase safety investment
  at all demand levels;
- delaying market introduction reduces cumulative safety investment, increases
  accident risk, and reduces producer profits;
- the main qualitative results remain robust when uncertainty about future
  liability regulation is introduced;
- neither full producer liability nor full consumer liability maximizes social
  welfare in the analyzed framework;
- an intermediate liability allocation generates the highest welfare in the
  model.

## Methods

- Dynamic Optimization
- Optimal Control
- Open-Loop Strategies
- Markov Strategies
- Numerical Optimization
- Stochastic Modeling
- Welfare Analysis

## Software Requirements

The notebooks have been tested successfully with:

**Wolfram Mathematica 14**

All three notebooks execute successfully under this version.

## How to Run

Each notebook can be executed independently.

1. Open the desired `.nb` file in Wolfram Mathematica.
2. Start with a clean Mathematica kernel.
3. Evaluate the notebook from top to bottom.
4. Model parameters are defined within the respective notebook.
5. The subsequent cells solve the corresponding investment problem and compute
   the welfare outcomes.

Depending on the model specification and hardware, some numerical optimization
steps may require additional computation time.

## Paper

**Andreas Pietryga**

*The Optimal Timing of Product Introduction and Safety Investments for
Automated Vehicles*

Doctoral research in Computational Economics, Bielefeld University.

## Related Repository

This project is part of:

[doctoral-research-code](https://github.com/andreaspietryga/doctoral-research-code)
