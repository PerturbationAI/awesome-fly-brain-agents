# 🪰 Awesome Fly Brain Agents

> **Real Drosophila connectomes, actually running things.**

A curated list of projects that put large-scale fruit-fly connectomes into an active loop: games, robots, simulated bodies, markets, desktop agents, and other environments.

This repository is intentionally narrower than a general Drosophila or connectomics resource list.

The question is simple:

> **What happens when you take measured fly wiring, simulate it at large scale, give it inputs, and let neural activity control something?**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

---

# 🎮 Games

| Project | Connectome / scale | Environment | Closed loop | Notes |
|---|---|---|:---:|---|
| [nftechie/doomfly](https://github.com/nftechie/doomfly) | MaleCNS, full retained graph | Doom / ViZDoom | ✅ | Connectome-based spiking simulation drives an engineered Doom interface. The project explicitly cautions against interpreting this as validated fly vision or demonstrated learning. |
| [ornata/fly](https://github.com/ornata/fly) | MaleCNS | Super Mario 64 | ✅ | Fly64 connects a MaleCNS-based brain model to SM64 through a visual-input → neural-network → controller loop. |
| [blendi-remade/fly-brain-minecraft](https://github.com/blendi-remade/fly-brain-minecraft) | MaleCNS, repo reports 176,422 neurons | Minecraft | ✅ | Minecraft sensory events drive real sensory populations; descending and motor activity controls a fly mob. |
| [michaelpersonal/flytype](https://github.com/michaelpersonal/flytype) | MaleCNS, repo reports 166,700 neurons | Typing + brick breaker | ✅ | Rendered pixels drive the connectome and neural activity is read back into actions. |
| [MidTermDev/immortal-fruit-fly](https://github.com/MidTermDev/immortal-fruit-fly) | FlyWire, repo reports 139,248 neurons | Arena + Doom | ✅ | Whole-brain LIF simulation with embodied arena and Doom modes; also records state hashes on-chain. |

---

# 🤖 Robots, bodies & control

| Project | Connectome / scale | Environment | Closed loop | Physical | Notes |
|---|---|---|:---:|:---:|---|
| [FutureJJ/ommatid](https://github.com/FutureJJ/ommatid) | MaleCNS, repo reports 165,122 CNS neurons + FlyVis visual frontend | Hexapod robot | ✅ | ✅ | Camera input reaches the model; descending and motor populations drive a six-legged robot. |
| [MarkUnthank/flyhard](https://github.com/MarkUnthank/flyhard) | MaleCNS, repo reports 165,122 traced neurons | Simulated fly body + steering wheel + CARLA | 🧪 | ❌ | Connectome-based controller learns to physically operate a simulated steering wheel; full driving remains an experimental target. |
| [rembish/fruit-fly](https://github.com/rembish/fruit-fly) | FlyWire, repo reports 139,255 neurons | Desktop environment | ✅ | ❌ | A desktop fly driven by a whole-brain LIF simulation; cursor / looming input is mapped into identified circuits. |

---

# 📈 Markets & trading

> These are neural-interface experiments, **not evidence of profitable trading** and not financial advice.

| Project | Connectome / scale | Environment | Closed loop | Notes |
|---|---|---|:---:|---|
| [nftechie/stonkfly](https://github.com/nftechie/stonkfly) | MaleCNS, repo reports 166,700 neurons / 25.6M connections | Coinbase market data + guarded trading actions | ✅ | Market state becomes sensory input; neural activity proposes buy / sell / hold. The project explicitly states that profitable learning has not been demonstrated. |

---

## Scope

### Main-list projects should satisfy most of these

- Use **measured Drosophila connectome data** such as MaleCNS or FlyWire.
- Run at **whole-brain / whole-CNS or comparable large scale** — generally around 100k+ neurons.
- Actually **simulate or propagate neural activity**, rather than only visualize the graph.
- Feed sensory or external information into the neural system.
- Read neural activity back out as actions, controls, or decisions.
- Preferably operate in a **closed sensor → brain → action → environment loop**.
- Provide public code, technical documentation, or enough evidence to inspect what is happening.

### Usually not in the main list

- Static connectome viewers.
- Small hand-selected circuits.
- Generic neural networks merely *inspired by* flies.
- Compound-eye or insect-inspired robotics that do not use measured connectome data.
- Projects with only a viral video and no inspectable technical material.

Only existing projects supported by inspectable evidence belong in the main list. Do not add wanted entries or placeholder categories.

---

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

> **Real connectome ≠ reconstructed mind.**<br>
> **Controls a game ≠ understands the game.**

Neuron counts also vary between projects because filtering and inclusion policies differ. Counts in the list are reported according to each project's public documentation and should not be assumed to be directly comparable.

---

## Legend

- **Closed loop** — environment affects neural input and neural output affects the next environment state.
- **Physical** — controls real hardware.
- **Docs checked** — the project description was checked against the project's public repository documentation. It does **not** mean the experiment was independently reproduced.

---

# 🧪 Inclusion checklist

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

---

# 🧭 Related lists & resources

This repository intentionally overlaps with broader Drosophila collections while keeping a narrower inclusion rule.

- [cobanov/awesome-fly](https://github.com/cobanov/awesome-fly) — broad collection of fruit-fly connectome projects, tools, datasets, games, and resources.
- [watthem/awesome-fruit-fly-connectome](https://github.com/watthem/awesome-fruit-fly-connectome) — broad connectome resource list covering datasets, papers, tools, analysis libraries, simulations, and community experiments.
- [natverse/malecns](https://github.com/natverse/malecns) — programmatic access and utilities for MaleCNS data.

The distinction here is:

> **large-scale connectomes doing things.**

---

# 🤝 Contributing

Found a real fly connectome controlling something strange, useful, or delightful?

Please read [CONTRIBUTING.md](CONTRIBUTING.md), then open an issue using **Suggest a project** or **Correction / metadata update**, or submit a pull request.

Templates: [project suggestion](.github/ISSUE_TEMPLATE/suggest-project.yml), [correction](.github/ISSUE_TEMPLATE/correction.yml), and [pull request checklist](.github/pull_request_template.md).

A strong submission includes:

```text
Project:
Repository:
Connectome:
Neuron count:
Connection / synapse count:
Filtering policy:
Neural model:
Input:
Output:
Environment:
Closed loop:
Learning / optimization:
Physical hardware:
Evidence:
Why it belongs:
```

---

## License

This curated list and original repository text are released under the [MIT License](LICENSE).

Individual linked projects, datasets, papers, images, and other third-party materials retain their own licenses and terms.

---

## 🪰 One connectome. 100,000+ neurons. Give it something to do.
