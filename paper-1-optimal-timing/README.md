# The Optimal Timing of Product Introduction and Safety Investments for Automated Vehicles

## Overview

This project contains the Wolfram Mathematica implementations supporting the
first paper of my doctoral dissertation in Computational Economics.

The research studies how liability regulation affects a monopolistic producer's
safety investments and the timing of market introduction of autonomous vehicles.

The model combines dynamic investment decisions, endogenous accident
probabilities, market demand, liability allocation, and welfare analysis over a
finite planning horizon.

## Research Question

The project investigates how different liability regimes affect:

- optimal safety investment,
- the timing of market introduction,
- accident probabilities,
- producer profits,
- and social welfare.

The analysis considers both deterministic liability and uncertainty regarding
future liability regulation.

## Computational Models

The repository contains three Wolfram Mathematica notebooks.

### `deterministic-liability-welfare.nb`

Implements the deterministic-liability benchmark.

The notebook numerically determines optimal investment decisions over the
planning horizon and evaluates the resulting welfare outcomes under different
liability allocations.

### `stochastic-liability-open-loop-welfare.nb`

Implements the model under uncertainty about future liability regulation using
an open-loop investment strategy.

Investment decisions are determined without conditioning future actions on the
subsequently realized liability state.

### `stochastic-liability-markov-welfare.nb`

Implements the model under liability uncertainty using state-dependent Markov
investment strategies.

Investment decisions can therefore respond to the realized state of the system.

## Main Economic Results

The analysis shows that liability regulation can affect safety investment in
non-monotonic ways.

In particular:

- stronger producer liability does not necessarily increase safety investment
  at all demand levels;
- delaying market introduction reduces cumulative safety investment and can
  increase accident risk;
- the qualitative conclusions remain robust when uncertainty about future
  liability regulation is introduced;
- neither full producer liability nor full consumer liability maximizes social
  welfare in the analyzed framework.

## Methods

- Dynamic Optimization
- Optimal Control
- Open-Loop Strategies
- Markov Strategies
- Numerical Optimization
- Stochastic Modeling
- Welfare Analysis

## Software Requirements

The notebooks were developed in:

**Wolfram Mathematica 12.3**

Later Mathematica versions also run the notebooks, but the original
implementations were developed and tested using Mathematica 12.3.

## Running the Code

Each notebook can be executed independently.

1. Open the desired `.nb` file in Wolfram Mathematica.
2. Start with a clean Mathematica kernel.
3. Evaluate the notebook from top to bottom.
4. The parameter values are defined near the beginning of each notebook.
5. The subsequent cells solve the corresponding investment problem and compute
   the welfare outcomes.

The notebooks contain numerical optimization routines and may require
substantial computation time depending on the model specification and hardware.

## Paper

**Andreas Pietryga**

*The Optimal Timing of Product Introduction and Safety Investments for
Automated Vehicles*

Doctoral research in Computational Economics, Bielefeld University.

## Repository

This project forms part of the doctoral research code repository:

`doctoral-research-code`
