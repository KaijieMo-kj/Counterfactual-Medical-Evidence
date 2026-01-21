# MedCounterFact Dataset

This repository contains the **MedCounterFact** dataset, introduced in the paper:

**Faithfulness vs. Safety: Evaluating LLM Behavior Under Counterfactual Medical Evidence**  
Kaijie Mo, Siddhartha Venkatayogi, Chantal Shaib, Ramez Kouzy, Wei Xu, Byron C. Wallace, Junyi Jessy Li  
(Submitted Jan 2026)

---

## Overview

**MedCounterFact** is a counterfactual medical question answering (QA) dataset designed to study how large language models (LLMs) respond to **implausible, adversarial, or unsafe medical evidence**.

The dataset is constructed by systematically replacing real medical interventions in clinical comparison questions and supporting evidence with counterfactual alternatives. This enables controlled evaluation of the trade-off between:

- **Faithfulness** to provided evidence  
- **Safety and plausibility awareness** in high-stakes medical settings

---

## Files

- **`MedCounterFact_original_data.jsonl`**  
  The original medical QA instances derived from real-world randomized controlled trials, before counterfactual replacement.

- **`MedCounterFact_replaced_data.jsonl`**  
  The counterfactual version of the dataset, where medical interventions in both questions and evidence are replaced with counterfactual stimuli.

- **`readme.markdown`**  
  Dataset documentation.

---

## Counterfactual Types

Each instance in the replaced dataset belongs to one of the following counterfactual categories:

- **Nonce**: invented or meaningless words 
- **Medical**: real medical interventions mismatched to the evidence context 
- **Non-medical**: entities unrelated to medicine  
- **Toxic**: harmful or clearly unsafe substances  

---

## Data Format

Each line in the `.jsonl` files is a JSON object representing one QA instance.  
The data description is provided in README.markdown.

## Citation

If you use **MedCounterFact** in your research, please cite the following paper:

```bibtex
@misc{mo2026faithfulnessvssafetyevaluating,
  title        = {Faithfulness vs. Safety: Evaluating LLM Behavior Under Counterfactual Medical Evidence},
  author       = {Mo, Kaijie and Venkatayogi, Siddhartha and Shaib, Chantal and Kouzy, Ramez and Xu, Wei and Wallace, Byron C. and Li, Junyi Jessy},
  year         = {2026},
  eprint       = {2601.11886},
  archivePrefix= {arXiv},
  primaryClass = {cs.CL},
  url          = {https://arxiv.org/abs/2601.11886}
}
