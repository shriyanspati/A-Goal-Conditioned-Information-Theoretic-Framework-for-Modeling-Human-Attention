![GitHub release](https://img.shields.io/github/v/release/shriyanspati/A-Goal-Conditioned-Information-Theoretic-Framework-for-Modeling-Human-Attention)
![License](https://img.shields.io/github/license/shriyanspati/A-Goal-Conditioned-Information-Theoretic-Framework-for-Modeling-Human-Attention)
![Paper](https://img.shields.io/badge/Paper-Research-blue)

# A Goal-Conditioned Information-Theoretic Framework for Modeling Human Attention

**Author:** Shriyans Pati  
**GitHub:** https://github.com/shriyanspati  
**Contact:** shriyansvpati@gmail.com  

A research manuscript proposing an information-theoretic framework for modeling human attention as **goal-conditioned information transfer** rather than simple time-on-task.

---

## Abstract

Human attention is often described as focus or concentration, but modern cognitive environments require a more precise measurement language.

This paper proposes a **goal-conditioned information-theoretic framework** for modeling attention. Instead of treating attention as a fixed cognitive resource, the framework defines relevant information relative to an explicit task goal and examines how much goal-relevant information is preserved between stimuli and behavioral responses.

A proof-of-concept analysis was performed using a publicly available Stroop dataset containing 131 participant observations. Classical response-time analysis was combined with mutual information estimation to demonstrate how information theory can complement traditional cognitive measurements.

The results show that information-theoretic analysis can capture task-condition information in behavioral responses while emphasizing that mutual information is not equivalent to measuring total attentional capacity. A complete validation requires trial-level behavioral, eye-tracking, or neural data.

---

# Motivation

Traditional attention measurements often rely on:

- Response time
- Accuracy
- Time-on-task
- Subjective ratings

While useful, these measurements do not directly quantify how much **goal-relevant information** is successfully transmitted through a cognitive system.

This project explores whether concepts from information theory can provide a mathematical framework for understanding attention while remaining grounded in cognitive psychology.

---

# Key Contributions

This work introduces:

- A definition of attention based on **goal-conditioned information control**
- A distinction between **statistical information** and **useful information**
- A mathematical framework using conditional mutual information
- Proposed metrics for:
  - Attentional throughput
  - Distractor leakage
  - Cognitive efficiency
- A proof-of-concept evaluation using a public Stroop dataset

---

# Framework Overview

The framework defines attention through:

- **Goal (G):** What the system is trying to accomplish
- **Stimulus field (S):** Available information in the environment
- **Relevant information (S_rel):** Features that affect optimal decisions
- **Irrelevant information (S_irrel):** Features that may influence behavior but do not help the goal
- **Response (R):** Behavioral or neural output

The central idea:

> Attention should be measured by how effectively a system preserves goal-relevant information while limiting irrelevant information leakage.

---

# Proposed Metrics

## Goal-Conditioned Attentional Throughput

\[
T_A(G)=\frac{I(S_{rel};R|G)}{\Delta t}
\]

Measures the rate at which relevant information is transmitted through the cognitive system.

---

## Distractor Leakage

\[
D(G)=
\frac{I(S_{irrel};R|G)}
{I(S_{rel};R|G)+\epsilon}
\]

Measures how much irrelevant information influences responses relative to relevant information.

---

## Attention Efficiency

\[
E_A(G)=T_A(G)-\lambda C_{effort}-\gamma D(G)
\]

A future metric combining useful information transfer, cognitive effort, and distraction.

---

# Experimental Demonstration

## Dataset

**Dataset:** Stroop Dataset  
**Source:** Daniel Lakens  

Dataset characteristics:

- 131 participants
- Congruent completion times
- Incongruent completion times
- Participant-level observations

Dataset source:

https://github.com/Lakens/Stroop

---

# Results

| Measurement | Result |
|---|---:|
| Mean Congruent Completion Time | 15.10 seconds |
| Mean Incongruent Completion Time | 23.00 seconds |
| Stroop Interference Effect | 7.90 seconds |
| Paired t-test | t(130)=18.04 |
| Significance | p < 0.001 |
| Cohen's dz | 1.58 |
| Raw Mutual Information | 0.404 bits |
| Miller-Madow Corrected MI | 0.399 bits |
| Bootstrap 95% CI | [0.324, 0.505] bits |
| Majority-bin Classification Accuracy | 79.4% |

---

# Interpretation

The analysis demonstrates that:

- Stroop interference appears in both traditional response-time analysis and information-theoretic analysis.
- Mutual information can quantify how much task-condition information is preserved in behavioral responses.
- Information theory alone does not define attention.

A distractor can contain predictive information while still harming task performance.

Therefore:

> Statistical information is not automatically meaningful attention.

---

# Limitations

This work is a proof-of-concept and does not claim to provide a complete measurement of human attention.

Current limitations:

- Uses block-level rather than trial-level data
- Does not include eye tracking
- Does not include EEG or neural measurements
- Cannot directly calculate full attentional throughput
- Requires future validation with preregistered experiments

---

# Future Work

Future studies should investigate:

- Trial-level attention measurements
- Eye-tracking integration
- EEG and neural recordings
- AI-assisted learning environments
- Human-computer interaction systems
- Cognitive effort estimation
- Comparison against existing attention metrics

---

# Repository Structure

```
.
├── README.md
├── LICENSE
├── CITATION.cff
├── paper/
│   └── A_Goal_Conditioned_Information_Theoretic_Framework_for_Modeling_Human_Attention.pdf
├── figures/
├── code/
└── data/
```

---

# Paper

The complete manuscript is available here:

`paper/A_Goal_Conditioned_Information_Theoretic_Framework_for_Modeling_Human_Attention.pdf`

---

# Citation

If you use or reference this work, please cite:

```bibtex
@misc{pati2026goalconditionedattention,
  title={A Goal-Conditioned Information-Theoretic Framework for Modeling Human Attention},
  author={Shriyans Pati},
  year={2026},
  note={Research manuscript},
  url={https://github.com/shriyanspati/A-Goal-Conditioned-Information-Theoretic-Framework-for-Modeling-Human-Attention}
}
```

---

# License

The paper is © 2026 Shriyans Pati.

Code contained in this repository is released under the MIT License unless otherwise specified.

---

# Contact

**GitHub:**  
https://github.com/shriyanspati

**Email:**  
shriyansvpati@gmail.com

---

# Disclaimer

This repository contains a theoretical framework and proof-of-concept analysis.

The proposed information-theoretic quantities should not be interpreted as validated measurements of human attentional capacity. Further experimental validation using richer behavioral and physiological datasets is required.
