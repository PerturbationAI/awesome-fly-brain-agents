# Contributing

Thanks for helping build **Awesome Fly Brain Agents**.

This list has a deliberately narrow scope: **large-scale, measured Drosophila connectomes that actively control or participate in an environment**.

The goal is not to collect every Drosophila project. It is to make the unusual whole-brain / whole-CNS agent experiments easy to find and easy to compare.

## Before submitting

Please search the README and existing issues first, then use the [Suggest a project form](https://github.com/PerturbationAI/awesome-fly-brain-agents/issues/new?template=suggest-project.yml).

A project must meet the following requirements for the main list:

1. Uses measured **Drosophila connectome data** such as MaleCNS or FlyWire.
2. Runs at **whole-brain / whole-CNS or comparable large scale**, generally around 100k+ neurons.
3. Actually simulates or propagates neural activity.
4. Has an external input or sensory interface.
5. Reads neural activity back out as actions, controls, or decisions.
6. Has public code, technical documentation, or inspectable evidence.

A closed loop is preferred. Partial control experiments must clearly state what has been demonstrated and what remains untested.

## Not enough by itself

The following are useful, but normally do not qualify for the main list:

- a connectome viewer,
- a static graph rendering,
- a small circuit simulation,
- an insect-inspired controller with no measured connectome data,
- a compound-eye camera project,
- a fly-inspired reinforcement-learning agent,
- a viral video without code or technical documentation.

Only submit existing projects supported by inspectable evidence. Do not add wanted entries or empty placeholder categories.

## Required project information

Provide the following details where available. Mark unknown values explicitly and include evidence for technical claims:

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
Closed loop: Yes / No / Partial / Unclear
Learning / optimization:
Physical hardware:
Evidence:
Why it belongs:
```

## Evidence quality

Prefer primary sources in this order:

1. the project's repository and technical documentation,
2. a paper or preprint from the project authors,
3. released experiment logs / reproducibility material,
4. a project website maintained by the authors,
5. secondary reporting only when no primary source is available.

Do not use a social-media post as the only evidence for a strong technical claim when better sources exist.

## How to describe claims

Use precise descriptions and attribute reported results.

| Prefer | Avoid |
|---|---|
| The repository reports a retained MaleCNS graph of 166,700 neurons. | This is literally a complete living fly brain. |
| Neural activity is decoded into left / right steering actions. | The fly understands how to drive. |
| The project reports a trading integration; profitable learning has not been demonstrated. | A fruit fly can beat the market. |

## Neuron counts

Different projects use different inclusion and filtering rules.

For example, one project may count all neuron entries while another may exclude unresolved objects, glia-like entries, unassigned classes, weak edges, or specific anatomical regions.

Therefore:

- preserve the project's stated number,
- include the filtering policy when known,
- do not silently normalize counts,
- do not imply that two counts are directly comparable unless they are.

## Games

For game projects, verify:

- what the model actually sees,
- how game state becomes neural input,
- how neural activity becomes game controls,
- whether control is closed-loop,
- whether the project uses fixed decoding, trained decoding, or synaptic learning.

## Robotics and drones

A project qualifies as a connectome-driven robot or drone only if the measured connectome actively participates in the control loop.

"Fly-inspired", "insect-inspired", or "neuromorphic" alone is not enough.

## Markets and trading

Trading projects may be included as technical experiments.

Descriptions must not imply:

- profitability,
- reliable prediction,
- investment merit,
- safety of live trading,

unless the source provides strong reproducible evidence — and even then, describe the evidence rather than turning it into financial advice.

## Pull requests

Keep PRs focused.

A good PR should:

- add or correct one logical group of entries,
- preserve the existing table format,
- use direct repository links where possible,
- keep descriptions factual and concise,
- avoid marketing language,
- include evidence for neuron counts and technical claims.

Please complete the [pull request checklist](.github/pull_request_template.md), which GitHub loads automatically for new PRs.

## Corrections

Corrections are welcome, especially for:

- dead links,
- wrong neuron counts,
- incorrect connectome attribution,
- incorrect closed-loop claims,
- outdated project status,
- misleading wording,
- duplicate projects.

Use the [Correction / metadata update form](https://github.com/PerturbationAI/awesome-fly-brain-agents/issues/new?template=correction.yml) if you do not want to open a PR.

## Style

- Project names use their repository or official project name.
- Prefer one or two sentences per entry.
- Use `repo reports ...` when a value has not been independently reproduced.
- Avoid hype, anthropomorphism, and consciousness claims.
- Keep caveats close to the claim they qualify.

## License

By contributing original text to this repository, you agree that your contribution may be distributed under the repository's MIT License.

Third-party projects and datasets keep their own licenses.
