# Visual Analytics for Prompt Injection and Jailbreak Detection in Agentic AI Systems

**Authors:** Arshad Hussain Mughal, Hira Khan, Ali Ahmed Shaikh, Misha Sanjrani

**Journal:** Spectrum of Engineering Sciences, Vol. 4, No. 3, pages 6354-6367 (published 31 March 2026)

**Paper:** [Read it on the journal website](https://www.thesesjournal.com/index.php/1/article/view/3851)

This repository hosts the published version of the paper plus the full text of the abstract, the experimental results, and the citation details, all in one place.

## Abstract

Agentic AI systems are autonomous large language model (LLM) based agents that keep memory, use external tools, and reason in multiple steps. They introduce new security weaknesses that do not exist in normal chat models. Prompt injection and jailbreak attacks are critical threats here: adversarial inputs manipulate agent behavior and often get past existing defenses using semantic obfuscation and context exploitation.

This paper presents a visual analytics framework for detecting and analyzing prompt injection attempts in agentic systems. The framework has three parts:

1. A transformer based detection engine that flags suspicious prompts with 94.2% accuracy.
2. An interactive visual dashboard that shows attack trajectories, adversarial fluctuation heat maps, and model behavior patterns.
3. A human-in-the-loop validation interface where security analysts can investigate alerts and spot evolving attack patterns.

The framework was tested on a synthesized dataset of 5,000 agentic interaction scenarios. It reached 94.2% accuracy, 91.7% precision, and 93.8% recall. In analyst studies the visualization interface scored 82.4 on the System Usability Scale (SUS). The framework closes the gap between opaque LLM security and interpretable analyst driven investigation, and it gives actionable insights for enterprise AI security operations.

**Keywords:** visual analytics, LLM security, cybersecurity, human-in-the-loop, adversarial robustness

## Proposed Framework

The framework follows a modular architecture with three integrated components:

- **Detection Engine:** a fine-tuned DistilBERT model optimized for agentic system prompts.
- **Visualization Dashboard:** five primary views, including an attack trajectory view drawn as a directed graph so analysts can follow how an attack moves through an agent.
- **Human-in-the-Loop Validation:** a review workflow where an analyst checks each detection, confirms or disputes it, adds reasoning, and feeds corrections back into the knowledge base and the detection model.

## Results

### Detection Performance vs Baselines (Table I)

| Model | Accuracy | Precision | Recall | F1 | AUC-ROC |
| --- | --- | --- | --- | --- | --- |
| Rule-based | 78.6% | 75.2% | 76.8% | 76.0% | 0.821 |
| Random Forest | 82.3% | 79.8% | 80.5% | 80.1% | 0.865 |
| BERT-base | 89.4% | 87.2% | 88.1% | 87.6% | 0.932 |
| SPI-Detector | 91.2% | 89.5% | 90.3% | 89.9% | 0.948 |
| PromptGuard | 92.1% | 90.8% | 91.5% | 91.1% | 0.956 |
| **This framework** | **94.2%** | **91.7%** | **93.8%** | **92.7%** | **0.972** |

### Performance by Attack Type (Table II)

| Attack Type | Accuracy | Precision | Recall | F1 |
| --- | --- | --- | --- | --- |
| Instruction Overriding | 95.8% | 93.5% | 94.2% | 93.8% |
| Context Injection | 93.2% | 90.8% | 92.5% | 91.6% |
| Role-playing Exploitation | 92.5% | 89.7% | 91.8% | 90.7% |
| Subtask Hijacking | 91.8% | 88.9% | 90.6% | 89.7% |
| Combined Attacks | 89.4% | 86.2% | 88.5% | 87.3% |

Instruction overriding attacks are detected best (95.8%), while combined attacks are the hardest.

### Visualization Usability (Table III)

An analyst study with 15 security analysts (5 senior, 10 junior) rated the dashboard components:

| Component | Mean SUS | Std Dev |
| --- | --- | --- |
| Attack Trajectory Visualization | 83.2 | 8.5 |
| Adversarial Fluctuation Heatmap | 81.7 | 9.2 |
| Model Behavior Auditing | 82.8 | 7.8 |

## Article History

- Received: 1 January 2026
- Accepted: 16 March 2026
- Published: 31 March 2026

## Citation

APA:

> Mughal, A. H., Khan, H., Shaikh, A. A., & Sanjrani, M. (2026). Visual analytics for prompt injection and jailbreak detection in agentic AI systems. *Spectrum of Engineering Sciences*, 4(3), 6354-6367.

BibTeX (from the journal):

```bibtex
@article{Mughal2026,
  title={Visual Analytics for Prompt Injection and Jailbreak Detection in Agentic AI Systems},
  author={Mughal, Arshad Hussain and Khan, Hira and Shaikh, Ali Ahmed and Sanjrani, Misha},
  journal={Spectrum of Engineering Sciences},
  volume={4},
  number={3},
  pages={6354-6367},
  year={2026},
  url={https://www.thesesjournal.com/index.php/1/article/view/3851}
}
```

## Copyright

The paper states "Copyright @Author". The work belongs to the authors and is published in Spectrum of Engineering Sciences. All rights reserved.

## Files

- `visual-analytics-prompt-injection-jailbreak-detection.pdf` — the full paper (14 pages)
