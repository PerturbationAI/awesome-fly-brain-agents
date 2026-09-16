# 🪰 Awesome Fly Brain Agents

> **Real Drosophila connectomes, actually running things.**

A curated list of projects that put large-scale fruit-fly connectomes into an active loop: games, robots, simulated bodies, markets, desktop agents, and other environments.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

## 🎮 Games

| Project | Connectome / reported scale | Environment | Closed loop | Notes |
|---|---|---|:---:|---|
| [DOOMFLY](https://github.com/nftechie/doomfly) | MaleCNS, 166,700 neurons | Doom / ViZDoom | ✅ | Connectome-based spiking simulation drives an engineered Doom interface. The project explicitly cautions against interpreting this as validated fly vision or demonstrated learning. |
| [Fly64](https://github.com/ornata/fly) | MaleCNS | Super Mario 64 | ✅ | Fly64 connects a MaleCNS-based brain model to SM64 through a visual-input → neural-network → controller loop. |
| [Fly Brain Minecraft](https://github.com/blendi-remade/fly-brain-minecraft) | MaleCNS, 176,422 neurons | Minecraft | ✅ | Minecraft sensory events drive real sensory populations; descending and motor activity controls a fly mob. |
| [flytype](https://github.com/michaelpersonal/flytype) | MaleCNS, 166,700 neurons | Typing + brick breaker | ✅ | Rendered pixels drive the connectome and neural activity is read back into actions. |
| [Immortal Fruit Fly](https://github.com/MidTermDev/immortal-fruit-fly) | FlyWire, 139,248 neurons | Arena + Doom | ✅ | Whole-brain LIF simulation with embodied arena and Doom modes; also records state hashes on-chain. |

## 🤖 Robots, bodies & control

| Project | Connectome / reported scale | Environment | Closed loop | Notes |
|---|---|---|:---:|---|
| [Ommatid](https://github.com/FutureJJ/ommatid) | MaleCNS, 165,122 CNS neurons + FlyVis visual frontend | Physical hexapod | ✅ | Camera input and descending-neuron readouts connect to a physical hexapod. Direct leg-motor control is in dry run; tested reflexes were not established. |
| [Flyhard](https://github.com/MarkUnthank/flyhard) | MaleCNS, 165,122 traced neurons | Simulated body + wheel + CARLA | 🧪 | Reports trained steering through a simulated foreleg and wheel connected to CARLA. Turns are instructed and speed is scripted; visual driving remains untested. |
| [fruit-fly](https://github.com/rembish/fruit-fly) | FlyWire, 139,255 neurons | Desktop sprite | ✅ | A desktop fly driven by a whole-brain LIF simulation; cursor / looming input is mapped into identified circuits. |

## 📈 Markets & trading

> These are neural-interface experiments, **not evidence of profitable trading** and not financial advice.

| Project | Connectome / reported scale | Environment | Closed loop | Notes |
|---|---|---|:---:|---|
| [Stonkfly](https://github.com/nftechie/stonkfly) | MaleCNS, 166,700 neurons / 25.6M connections | Coinbase market data + guarded trading actions | ✅ | Market state becomes sensory input; neural activity proposes buy / sell / hold. The project explicitly states that profitable learning has not been demonstrated. |

## Scope

### Required for the main list

- Use **measured Drosophila connectome data** such as MaleCNS or FlyWire.
- Run at **whole-brain / whole-CNS or comparable large scale** — generally around 100k+ neurons.
- Actually **simulate or propagate neural activity**, rather than only visualize the graph.
- Feed sensory or external information into the neural system.
- Read neural activity back out as actions, controls, or decisions.
- Provide public code, technical documentation, or enough evidence to inspect what is happening.

A **closed sensor → brain → action → environment loop** is preferred. Partial control experiments must clearly state what has been demonstrated and what remains untested.

### Usually not in the main list

- Static connectome viewers.
- Small hand-selected circuits.
- Generic neural networks merely *inspired by* flies.
- Compound-eye or insect-inspired robotics that do not use measured connectome data.
- Projects with only a viral video and no inspectable technical material.

Only existing projects supported by inspectable evidence belong in the main list. Do not add wanted entries or placeholder categories.

## Important caveat

A connectome is a wiring diagram, not a complete biological brain model.

Every runnable project must make additional assumptions about some combination of:

- neuron dynamics,
- synaptic signs and weights,
- membrane parameters,
- sensory encoding,
- motor decoding,
- plasticity,
- reward signals,
- time scaling,
- missing or uncertain biological data.

> **Real connectome ≠ reconstructed mind.**<br>**Controls a game ≠ understands the game.**

Neuron counts also vary between projects because filtering and inclusion policies differ. Counts in the list are reported according to each project's public documentation and should not be assumed to be directly comparable.

## Reading the tables

- **Closed loop** — environment affects neural input and neural output affects the next environment state.
- **✅** — a closed loop is documented; this does not establish successful learning or biological fidelity.
- **🧪** — partial or experimental integration; see the entry's limitations.

Project descriptions were checked against public repository documentation on **2026-09-16**. This is a documentation review, not an independent reproduction.

## 🧪 Inclusion checklist

Before adding a project, try to answer:

1. Which connectome is used?
2. How many neurons are actually simulated?
3. What edge / synapse filtering policy is used?
4. What neuronal dynamics are used?
5. What exactly enters the network?
6. Which neurons or readouts determine actions?
7. Is the environment genuinely closed-loop?
8. Is anything trained or optimized?
9. If so, which parameters are trained?
10. Can another person inspect or reproduce the setup?

When a number or capability comes only from a project README, describe it as **the project's reported value or claim**.

## 🧭 Related lists & resources

This repository intentionally overlaps with broader Drosophila collections while keeping a narrower inclusion rule.

- [cobanov/awesome-fly](https://github.com/cobanov/awesome-fly) — broad collection of fruit-fly connectome projects, tools, datasets, games, and resources.
- [watthem/awesome-fruit-fly-connectome](https://github.com/watthem/awesome-fruit-fly-connectome) — broad connectome resource list covering datasets, papers, tools, analysis libraries, simulations, and community experiments.
- [natverse/malecns](https://github.com/natverse/malecns) — programmatic access and utilities for MaleCNS data.

## 🤝 Contributing

Found a real fly connectome controlling something strange, useful, or delightful?

Read [CONTRIBUTING.md](CONTRIBUTING.md), then [suggest a project](https://github.com/PerturbationAI/awesome-fly-brain-agents/issues/new?template=suggest-project.yml), [submit a correction](https://github.com/PerturbationAI/awesome-fly-brain-agents/issues/new?template=correction.yml), or open a pull request using the [PR checklist](.github/pull_request_template.md).

## License

This curated list and original repository text are released under the [MIT License](LICENSE).

Individual linked projects, datasets, papers, images, and other third-party materials retain their own licenses and terms.

**🪰 One connectome. 100,000+ neurons. Give it something to do.**
