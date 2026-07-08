# MedCounterFact Dataset

This repository contains the **MedCounterFact** dataset, introduced in the paper:

**Faithfulness vs. Safety: Evaluating LLM Behavior Under Counterfactual Medical Evidence**  
Kaijie Mo, Siddhartha Venkatayogi, Chantal Shaib, Ramez Kouzy, Wei Xu, Byron C. Wallace, Junyi Jessy Li  
**Paper Link:** https://aclanthology.org/2026.findings-acl.1847/

**Version Update** (March 2026): The dataset has been revised to correct minor issues identified in previous versions 

## Overview

**MedCounterFact** is a counterfactual medical question answering (QA) dataset designed to study how large language models (LLMs) respond to **implausible, adversarial, or unsafe medical evidence**.

The dataset is constructed by systematically replacing real medical interventions in clinical comparison questions and supporting evidence with counterfactual alternatives. We will release the codebase and additional model outputs in a future update.


## Files

- **`MedCounterFact_original_data.jsonl`**  
  The original medical QA instances derived from real-world randomized controlled trials, before counterfactual replacement ([Polzak et al., 2025](https://arxiv.org/abs/2505.22787)).

- **`MedCounterFact_replaced_data.jsonl`**  
  The counterfactual version of the dataset, where medical interventions in both questions and evidence are replaced with counterfactual stimuli.

- **`readme.markdown`**  
  Dataset documentation.


## Counterfactual Types

Each instance in the replaced dataset belongs to one of the following counterfactual categories:

- **Nonce**: invented or meaningless words 
- **Medical**: real medical interventions mismatched to the evidence context 
- **Non-medical**: entities unrelated to medicine  
- **Toxic**: harmful or clearly unsafe substances  


## Data Format

Each line in the `.jsonl` files is a JSON object representing one QA instance.  
The data description is provided in DataFormat.md.

## Citation

If you use **MedCounterFact** in your research, please cite the following paper:

```bibtex
@inproceedings{mo-etal-2026-faithfulness,
    title = "Faithfulness vs. Safety: Evaluating {LLM} Behavior Under Counterfactual Medical Evidence",
    author = "Mo, Kaijie  and
      Venkatayogi, Siddhartha  and
      Shaib, Chantal  and
      Kouzy, Ramez  and
      Xu, Wei  and
      Wallace, Byron C  and
      Li, Junyi Jessy",
    editor = "Liakata, Maria  and
      Moreira, Viviane P.  and
      Zhang, Jiajun  and
      Jurgens, David",
    booktitle = "Findings of the {A}ssociation for {C}omputational {L}inguistics: {ACL} 2026",
    month = jul,
    year = "2026",
    address = "San Diego, California, United States",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2026.findings-acl.1847/",
    doi = "10.18653/v1/2026.findings-acl.1847",
    pages = "37053--37081",
    ISBN = "979-8-89176-395-1"
}
