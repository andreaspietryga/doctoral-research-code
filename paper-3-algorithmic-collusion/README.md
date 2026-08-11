# Collusion under Algorithmic Pricing: How Robust Is It?

## Overview

This directory contains the Wolfram Mathematica implementations supporting the
third paper of my doctoral dissertation in Computational Economics.

The project studies algorithmic collusion in repeated pricing games populated
by reinforcement-learning agents.

Standard tabular Q-Learning can learn supra-competitive pricing behavior in
multi-agent pricing environments without explicit communication between the
agents.

The project investigates the mechanisms underlying this behavior and develops
two modified reinforcement-learning algorithms:

- **Smooth Q-Learning**
- **Smooth Dyna-Q**

The objective is to reduce the tendency toward collusive pricing while
preserving adaptive learning and promoting convergence toward competitive Nash
equilibria in the analyzed environments.

The algorithms are evaluated first in a pricing environment formulated as a
potential game and subsequently in the pricing environment studied by
Calvano et al. (2020).

## Research Questions

The project investigates:

- whether standard Q-Learning agents can learn collusive pricing strategies;
- whether collusion also emerges in pricing environments with favorable
  equilibrium properties;
- whether modified action-selection mechanisms can reduce collusive behavior;
- whether model-based planning improves learning efficiency and convergence;
- how robust the proposed algorithms are across different pricing
  environments;
- and whether competitive outcomes can still emerge when only one of the
  interacting agents uses the proposed learning mechanism.

## Algorithms

### Tabular Q-Learning

Standard tabular Q-Learning serves as the primary benchmark.

Agents repeatedly choose prices, observe the resulting profits, and update
their Q-values based on their experienced rewards and future value estimates.

The benchmark experiments demonstrate how independent Q-Learning agents can
learn supra-competitive pricing behavior in repeated market interaction.

### Smooth Q-Learning

Smooth Q-Learning extends standard Q-Learning by introducing a smoothing
mechanism inspired by the Smooth UCT Search framework.

The algorithm partially incorporates observed competitor behavior into the
action-selection process.

The resulting additional stochasticity changes the exploration dynamics and
reduces the tendency of the learning agents to stabilize at collusive pricing
strategies.

### Smooth Dyna-Q

Smooth Dyna-Q extends the smoothing approach by adding a model-based planning
component.

The algorithm combines:

- Q-Learning from actual market interactions;
- the smoothing mechanism used for action selection; and
- additional learning updates based on simulated experience generated from an
  internal model.

The planning component is designed to improve learning efficiency and
accelerate convergence while retaining the anti-collusive properties of the
smoothing mechanism.

## Experimental Environments

The computational experiments are organized around two pricing environments.

### Model 1: Potential-Game Pricing Environment

The first environment is a repeated duopoly pricing game formulated as a
potential game.

The experiments compare:

- standard Tabular Q-Learning;
- Smooth Q-Learning; and
- Smooth Dyna-Q.

This environment is used to study whether algorithmic collusion can emerge even
when the underlying pricing game possesses favorable equilibrium properties and
to evaluate whether the proposed algorithms improve convergence toward the
competitive equilibrium.

### Calvano et al. Pricing Environment

The second set of experiments uses the repeated pricing environment studied by
Calvano et al. (2020), in which standard Q-Learning agents are known to be able
to learn supra-competitive pricing behavior.

The experiments examine both symmetric and asymmetric combinations of learning
algorithms.

This allows the robustness of Smooth Dyna-Q to be evaluated when:

- both agents use Smooth Dyna-Q;
- Smooth Dyna-Q interacts with standard Dyna-Q; and
- Smooth Dyna-Q interacts with standard Tabular Q-Learning.

## Files

### Model 1

#### `model1-tabular-q-learning.nb`

Implements the standard Tabular Q-Learning benchmark in the first pricing
environment.

The notebook is used to study whether two independent Q-Learning agents converge
toward competitive or supra-competitive pricing behavior.

#### `model1-smooth-q-learning.nb`

Implements Smooth Q-Learning in the first pricing environment.

The notebook evaluates whether the smoothing mechanism reduces collusive
behavior and improves convergence toward the competitive Nash equilibrium.

#### `model1-smooth-dyna-q.nb`

Implements Smooth Dyna-Q in the first pricing environment.

The notebook combines smoothing with model-based planning and evaluates its
effects on convergence, learning efficiency, and pricing behavior.

### Calvano et al. Environment

#### `calvano-tabular-q-learning.nb`

Implements the standard Tabular Q-Learning benchmark in the Calvano et al.
pricing environment.

This experiment provides the reference case for the emergence of
supra-competitive pricing under standard independent Q-Learning.

#### `calvano-smooth-dyna-q-vs-dyna-q.nb`

Compares a Smooth Dyna-Q agent with an agent using standard Dyna-Q.

The experiment evaluates whether the smoothing mechanism remains effective when
only one side of the interaction employs the proposed modification.

#### `calvano-smooth-dyna-q-vs-smooth-dyna-q.nb`

Simulates an environment in which both pricing agents use Smooth Dyna-Q.

This experiment evaluates the behavior and convergence of the proposed
algorithm under symmetric adoption.

#### `calvano-smooth-dyna-q-vs-tabular-q.nb`

Compares a Smooth Dyna-Q agent with a standard Tabular Q-Learning agent.

This asymmetric experiment tests whether the proposed algorithm can promote
competitive behavior even when the competing agent continues to use standard
Q-Learning.

## Experimental Structure

The experiments can be summarized as:

```text
                    Algorithmic Pricing
                           |
             -----------------------------
             |                           |
             v                           v
     Model 1 Environment           Calvano Environment
             |                           |
     -------------------        --------------------------
     |        |        |        |           |            |
     v        v        v        v           v            v
 Tabular   Smooth   Smooth    Tabular   Smooth Dyna-Q  Smooth Dyna-Q
 Q         Q        Dyna-Q     Q         vs Dyna-Q      vs Tabular Q
                                                       
                                      +
                                Smooth Dyna-Q
                                vs Smooth Dyna-Q
```

The individual notebooks represent separate computational experiments and do
not need to be executed sequentially.

## Main Results

The simulations show that algorithmic collusion is sensitive to the design of
the learning algorithm.

In the analyzed environments:

- standard Tabular Q-Learning can converge to supra-competitive pricing
  outcomes;

- Smooth Q-Learning substantially reduces the tendency toward collusive
  behavior;

- Smooth Dyna-Q combines the smoothing mechanism with model-based planning and
  achieves faster and more stable convergence in the analyzed experiments;

- the proposed algorithms promote convergence toward competitive Nash
  equilibria in both the potential-game environment and the Calvano pricing
  environment;

- stronger smoothing can be required in the more complex Calvano environment;

- and the anti-collusive effect remains robust in asymmetric experiments in
  which only one agent employs Smooth Dyna-Q.

The results demonstrate that collusive behavior is not an unavoidable
consequence of reinforcement learning in repeated pricing environments and that
the design of the learning mechanism can materially affect market outcomes.

## Methods

- Tabular Q-Learning
- Smooth Q-Learning
- Dyna-Q
- Smooth Dyna-Q
- Model-Based Reinforcement Learning
- Model-Based Planning
- Multi-Agent Reinforcement Learning
- Game Theory
- Algorithmic Pricing
- Simulation
- Nash Equilibrium Analysis

## Software Requirements

All notebooks in this directory have been tested successfully with:

**Wolfram Mathematica 14**

The computational notebooks execute successfully under this version.

## Running the Notebooks

Each notebook represents an independent experimental configuration.

For computational notebooks:

1. Open the desired `.nb` file in Wolfram Mathematica.
2. Start with a clean Mathematica kernel.
3. Evaluate the notebook from top to bottom.
4. Model and learning parameters are defined within the respective notebook.
5. Depending on the experiment, execution time may vary with hardware and
   parameter settings.

Because the simulations use stochastic reinforcement-learning processes,
individual learning trajectories can vary across runs.

## Paper

**Andreas Pietryga**

*Collusion under Algorithmic Pricing: How Robust Is It?*

Doctoral research in Computational Economics, Bielefeld University.

## Related Repository

This project is part of the main doctoral research code repository:

[doctoral-research-code](https://github.com/andreaspietryga/doctoral-research-code)
