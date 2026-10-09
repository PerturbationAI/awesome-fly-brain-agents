# 🪰 Awesome Fly Brain Agents

> **Real Drosophila connectomes, actually running things.**

A curated list of projects that put large-scale fruit-fly connectomes into an active loop: games, robots, simulated bodies, markets, desktop agents, and other environments.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

## 🎮 Games

| Project | Connectome / reported scale | Environment | Closed loop | Notes |
|---|---|---|:---:|---|
| [nftechie/doomfly](https://github.com/nftechie/doomfly) | MaleCNS, 166,700 neurons | Doom / ViZDoom | ✅ | Connectome-based spiking simulation drives an engineered Doom interface. The project explicitly cautions against interpreting this as validated fly vision or demonstrated learning. |
| [ornata/fly](https://github.com/ornata/fly) | MaleCNS | Super Mario 64 | ✅ | Fly64 connects a MaleCNS-based brain model to SM64 through a visual-input → neural-network → controller loop. |
| [blendi-remade/fly-brain-minecraft](https://github.com/blendi-remade/fly-brain-minecraft) | MaleCNS, 176,422 neurons | Minecraft | ✅ | Minecraft sensory events drive real sensory populations; descending and motor activity controls a fly mob. |
| [michaelpersonal/flytype](https://github.com/michaelpersonal/flytype) | MaleCNS, 166,700 neurons | Typing + brick breaker | ✅ | Rendered pixels drive the connectome and neural activity is read back into actions. |
| [MidTermDev/immortal-fruit-fly](https://github.com/MidTermDev/immortal-fruit-fly) | FlyWire, 139,248 neurons | Arena + Doom | ✅ | Whole-brain LIF simulation with embodied arena and Doom modes; also records state hashes on-chain. |
| [dohun1214/malecns-asteroids](https://github.com/dohun1214/malecns-asteroids) | MaleCNS, 166,700 neurons | Atari Asteroids | ✅ | Asteroid positions stimulate visual populations in a whole-brain LIF model; motor readouts steer escape or pursuit. Includes lesion and rewiring controls; firing and control timing use engineered rules. |
| [seanphan/flyt3](https://github.com/seanphan/flyt3) | MaleCNS, 166,700 neurons | Tic-tac-toe | ✅ | Board state drives a frozen LIF connectome and a trained motor-spike readout selects moves. The play server also applies hand-written win/block overrides; gameplay is not solely a neural readout. |
| [Reldnahc/pokefly](https://github.com/Reldnahc/pokefly) | MaleCNS, repo reports 166,700 neurons | Pokemon Red / PyBoy | ✅ | Screen pixels drive a connectome simulation with fixed motor-to-button mappings and experimental internal synaptic plasticity. Outcome rewards use game telemetry; useful screen-specific gameplay learning remains unestablished. |
| [shantanugoel/fly-games](https://github.com/shantanugoel/fly-games) | MaleCNS, repo reports 166,700 neurons | Super Mario Bros. / Kung Fu / Doom | ✅ | Structured game facts stimulate a frozen spiking connectome; descending activity feeds a fitted readout or hand-written decoder. Only the readout is trained, and held-out imitation scores do not establish closed-loop game success. |
| [almera-vs/malecns-pong-lab](https://github.com/almera-vs/malecns-pong-lab) | MaleCNS, repo reports 166,700 neurons | Pong with simulated limb-and-paddle control | ✅ | Pooled court pixels and joint feedback drive sparse spiking activity; tibia motor pools control engineered paddles. A three-seed pilot changed synaptic weights without improving held-out hit/miss counts. |
| [HakimElAyoubi/fly-chess](https://github.com/HakimElAyoubi/fly-chess) | MaleCNS, repo reports 144,209 neurons | Chess / UCI engine | ✅ | Encoded board state drives photoreceptors in a rate-based connectome; a trained descending-neuron readout selects moves. Network gains, biases and readout heads are trained; legal-move and anti-repetition rules constrain play. The walking fly in the demo is animated. |
| [blackicon-eth/fly-plays-games](https://github.com/blackicon-eth/fly-plays-games) | MaleCNS, repo reports 166,700 neurons | Retroid / Pokemon Red via PyBoy | ✅ | Game-supplied object positions drive visual projection neurons in a frozen LIF connectome; a trained descending-neuron readout controls the Retroid paddle. Only the readout is trained; the long Pokemon journey is scripted, not neural navigation. |
| [gabinacode/fox-vs-fly](https://github.com/gabinacode/fox-vs-fly) | MaleCNS, repo reports 166,700 neurons | Browser platform fighter | ✅ | Six engineered game sensors drive a full-graph rate model; a calibrated descending/motor readout selects movement and attacks. The model uses positive synapse counts without transmitter signs, and recovery logic and action gates are authored rather than learned. |
| [CodeMan1729/flybrain-arena](https://github.com/CodeMan1729/flybrain-arena) | MaleCNS, repo reports 166,700 neurons | Godot drone combat | ✅ | Aim/fire cues enter LC4/LPLC2 directly in a full-graph signed-rate model; DNp01/DNp03 activity is decoded into evasive motion. This FLYFEAR derivative combines neural dodge output with engineered pursuit and flight rules; retinal looming detection is not simulated. |
| [jamesbiederbeck/flappy-haltere](https://github.com/jamesbiederbeck/flappy-haltere) | MaleCNS v1.0, full-graph LIF model | Flappy Bird | ✅ | Pixels and fall-speed-derived haltere stimulation drive a shared connectome simulator; accumulated flight-muscle motor spikes trigger flaps. Input mappings and the flap threshold are engineered; reported play mainly holds altitude, without demonstrated active pipe avoidance. The engine requires a separate checkout and local graph preparation. |
| [icybb0903-sketch/flygo](https://github.com/icybb0903-sketch/flygo) | MaleCNS, repo reports 139,662 nodes / 5,536,347 connections | 9×9 Go | ✅ | Encoded board state drives a fixed-graph LIF simulation; pooled neural features feed an offline-trained linear readout with legal-move masking. Input/output pools are engineered, play does not train the policy online, and playing strength remains unestablished; the fly carrying stones is animated. |
| [professorwang/flybrain-banana-quest](https://github.com/professorwang/flybrain-banana-quest) | Repo reports FlyWire 139,255 / MaleCNS 176,422 neurons | Browser banana-foraging arena | ✅ | Modeled odor and taste drive a full-graph LIF network; descending activity steers movement and feeding-pool spikes gate consumption. Sensory pools, weight normalization and readouts are engineered; low-activity random wandering, food-proximity stopping and wall bounces are game rules, with no synaptic learning. |
| [0Sakura721/flyaim](https://github.com/0Sakura721/flyaim) | MaleCNS, repo reports 166,700 neurons | Offline aiming arena | ✅ | Pixels drive a full-brain LIF model; a trained descending-neuron readout moves the crosshair. The reported frozen-connectome experiment found no advantage over shuffled wiring and worse target distance than random actions; retinal mapping and transmitter signs include known approximations. |
| [castor639/fly-tennis](https://github.com/castor639/fly-tennis) | MaleCNS, repo reports 163,903 neurons | Simulated racket game | ✅ | Analytic compound-eye input drives full-graph rate networks; medulla activity relative to a ball-free twin network controls lateral positioning. Edges below five synapses are removed; the untrained match uses engineered decoding, while swings, return targets and recentering are scripted and legs are not simulated. |
| [ThomasLin070217/FlyGift](https://github.com/ThomasLin070217/FlyGift) | FlyWire v783, repo reports 139,255 neurons | macOS fly-swatting game | ✅ | Swatter approach and body feedback drive a whole-brain Metal LIF simulation; Giant Fiber spikes trigger escape and descending activity modulates movement. This SiliconFly derivative uses engineered sensory gains, procedural gait/flight, target selection and game timing; it has no synaptic learning or simulated ventral nerve cord. |

## 🤖 Robots, bodies & control

| Project | Connectome / reported scale | Environment | Closed loop | Notes |
|---|---|---|:---:|---|
| [FutureJJ/ommatid](https://github.com/FutureJJ/ommatid) | MaleCNS, 165,122 CNS neurons + FlyVis visual frontend | Physical hexapod | ✅ | Camera input and descending-neuron readouts connect to a physical hexapod. Direct leg-motor control is in dry run; tested reflexes were not established. |
| [MarkUnthank/flyhard](https://github.com/MarkUnthank/flyhard) | MaleCNS, 165,122 traced neurons | Simulated body + wheel + CARLA | 🧪 | Reports trained steering through a simulated foreleg and wheel connected to CARLA. Turns are instructed and speed is scripted; visual driving remains untested. |
| [rembish/fruit-fly](https://github.com/rembish/fruit-fly) | FlyWire, 139,255 neurons | Desktop sprite | ✅ | A desktop fly driven by a whole-brain LIF simulation; cursor / looming input is mapped into identified circuits. |
| [nsfm/fly-afterlife](https://github.com/nsfm/fly-afterlife) | MaleCNS, 162,517 neurons + FlyVis frontend | Simulated room | ✅ | Visual and contact inputs drive a spiking connectome; descending and leg-motor readouts control heading and pace. Loom-selectivity claims were withdrawn, and steering robustness varies across visual models. |
| [PtPavloTkachenko/fly-brain-spectacles](https://github.com/PtPavloTkachenko/fly-brain-spectacles) | MaleCNS, repo reports 166,700 neurons | AR fly on Snap Spectacles | ✅ | A browser-based LIF simulation receives room and headset cues; descending and motor readouts control a virtual fly. Visual features, walking rhythm and flight/landing control are engineered; pixels alone do not drive behavior in this model. |
| [Noir-infini/pianist-fly](https://github.com/Noir-infini/pianist-fly) | MaleCNS, repo reports 166,700 neurons | MuJoCo fly + piano | 🧪 | Modeled sugar and visual inputs drive a fixed-weight LIF connectome; motor-pool rates modulate scripted key-press timing. The score, target keys and leg trajectories are programmed; the directional gate reads plume data, and zero motor activity falls back to default timing. |
| [dimm0909/fly-in-the-bottle](https://github.com/dimm0909/fly-in-the-bottle) | MaleCNS, repo reports 164,606 neurons | Desktop fly in a simulated jar | ✅ | Touch, cursor cues and body feedback drive an adaptive-threshold LIF model; motor and descending pools control motion. Connections below five synapses and motor-neuron outputs are removed; sensory mappings, gait rhythms and body physics are engineered. Without the separately installed brain, the widget uses scripted behavior. |
| [Ryans-sS/malecns-embodied-fly](https://github.com/Ryans-sS/malecns-embodied-fly) | MaleCNS, repo reports 166,700 neurons | Simulated foraging arena | ✅ | Modeled odor, taste and body feedback drive a LIF connectome; descending/leg activity controls motion and proboscis activity gates ingestion. Edges below two synapses are removed; metabolism, exploration and feeding-stop rules are engineered, with simplified dopamine-gated KC→MBON plasticity. The separate NeuroMechFly demo uses scripted gait and wandering. |
| [yusenthebot/FlyArm](https://github.com/yusenthebot/FlyArm) | MaleCNS, repo reports 166,700 neurons / 10.5M connections | MuJoCo Franka arm | ✅ | Simulator state and task cues enter a trained encoder; a frozen whole-CNS rate model feeds a trained motor decoder. Self-connections and edges below three synaptic contacts are removed; this is simulation using privileged state, with no established advantage over alternative wiring. |
| [joshuabradley012/brainfly](https://github.com/joshuabradley012/brainfly) | MaleCNS, repo reports 166,700 neurons + FlyVis frontend | NeuroMechFly / MuJoCo rotating-drum arena | ✅ | A modeled visual scene drives a whole-graph spiking/graded network; baseline-corrected DNa02 activity steers the body. The documented loop uses the project's unvalidated inherited model and an engineered descending-to-gait mapping; FlyGym's walking controller supplies leg coordination. |
| [hsilvosa/fruit-fly-rl](https://github.com/hsilvosa/fruit-fly-rl) | MaleCNS, repo reports 167,184 neurons | Procedural 3D navigation | ✅ | Simulated sensors drive a fixed full-graph rate model whose features feed a learned flight policy. Sensors and flight dynamics are engineered; the current large-room demo uses explicit map planning, with a neural reader that cancels most recurrence, and does not establish learned navigation or a benefit from fly wiring. |
| [IrohAmca/NeuroPest](https://github.com/IrohAmca/NeuroPest) | FlyWire v783, repo reports 138,639 neurons in optional full mode | Desktop fly pet | ✅ | Cursor and body cues drive a LIF connectome; descending activity controls walking, retreat, escape and steering. The default uses a 15,000-neuron subset; full mode requires selecting the complete graph. Sensory mappings, state transitions and sprite motion are engineered, and the separate learning module uses synthetic mushroom-body wiring by default. |

## 📈 Markets & trading

> These are neural-interface experiments, **not evidence of profitable trading** and not financial advice.

| Project | Connectome / reported scale | Environment | Closed loop | Notes |
|---|---|---|:---:|---|
| [nftechie/stonkfly](https://github.com/nftechie/stonkfly) | MaleCNS, 166,700 neurons / 25.6M connections | Coinbase market data + guarded trading actions | ✅ | Market state becomes sensory input; neural activity proposes buy / sell / hold. The project explicitly states that profitable learning has not been demonstrated. |

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

The original nine project descriptions were checked against public repository documentation on **2026-09-16**. Entries for `dohun1214/malecns-asteroids`, `seanphan/flyt3`, and `nsfm/fly-afterlife` were checked against documentation and control-loop source on **2026-09-17**. `Reldnahc/pokefly` was checked against documentation and control-loop source on **2026-09-18**. `shantanugoel/fly-games` and `almera-vs/malecns-pong-lab` were checked against documentation and control-loop source on **2026-09-19**. `HakimElAyoubi/fly-chess` was checked against documentation and control-loop source on **2026-09-20**. `blackicon-eth/fly-plays-games` was checked against documentation, the Retroid control loop and upstream neural source on **2026-09-21**. `PtPavloTkachenko/fly-brain-spectacles` was checked against documentation and neural/control-loop source on **2026-09-22**. `Noir-infini/pianist-fly` was checked against documentation and neural/control-loop source on **2026-09-23**. `gabinacode/fox-vs-fly` and `CodeMan1729/flybrain-arena` were checked against documentation and neural/control-loop source on **2026-09-24**. `jamesbiederbeck/flappy-haltere` was checked against documentation, control-loop source and its shared neural engine on **2026-09-25**. `dimm0909/fly-in-the-bottle` was checked against documentation, graph construction and neural/body-loop source on **2026-09-26**. `icybb0903-sketch/flygo` was checked against documentation, neural/control-loop source and default readout metadata on **2026-09-28**. `professorwang/flybrain-banana-quest` was checked against documentation and neural/game-loop source on **2026-09-30**. `Ryans-sS/malecns-embodied-fly` was checked against documentation, graph construction and neural/arena-loop source on **2026-10-02**. `0Sakura721/flyaim` and `yusenthebot/FlyArm` were checked against documentation, graph metadata/construction and neural/control-loop source on **2026-10-03**. `joshuabradley012/brainfly` was checked against documentation and neural/body-loop source on **2026-10-04**. `castor639/fly-tennis` and `hsilvosa/fruit-fly-rl` were checked against documentation, graph construction/model details and neural/control-loop source on **2026-10-05**. `ThomasLin070217/FlyGift` was checked against documentation, packaged graph metadata and neural/game-loop source on **2026-10-07**. `IrohAmca/NeuroPest` was checked against documentation, full-graph selection/construction and neural/desktop-loop source on **2026-10-09**. These are source reviews, not independent reproductions.

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
