## Dataset Overview
This directory contains two subsets: original data and replaced data.

The original data are drawn directly from MedEvidence and preserve the original questions and evidence summaries from systematic reviews.

The replaced data, referred to as MedCounterFact, are constructed by replacing "treatment A" in both the "question" and "article_summaries" fields of the original data with counterfactual intervention terms (specified by the "item" field), while keeping all other components unchanged.

## Data Format Description

Each record in the dataset is a JSON object representing a single question–evidence instance derived from a systematic review.

### Top-level Fields

- **index** *(int)*  
  Unique index of the data instance.

- **question** *(string)*  
  The natural-language comparison question, typically asking whether an outcome is higher, lower, or the same between two interventions.

- **article_summaries** *(list of strings)*  
  a set of evidence RCTS extracted from relevant systematic reviews

- **metadata** *(object)*  
  Structured annotations and attributes associated with the instance.

### Metadata Fields

- **id** *(string)*  
  Internal identifier shared across original and replaced data for the same question.

- **treatment A** *(string)*  
  The intervention or treatment being evaluated.

- **treatment B** *(string)*  
  The comparator treatment (often placebo or standard care).

- **question** *(string)*  
  Canonical form of the comparison question used in the original review.

- **answer** *(string)*  
  Gold answer label (e.g., `higher`, `lower`, `no difference`).

- **MainCategory** *(string)*  
  High-level category of the intervention (e.g., Nonce).

- **SubCategory** *(string)*  
  Finer-grained category of the intervention (e.g., Everyday Objects).

- **item** *(string)*  
  The specific substituted counterfactual intervention term.

- **medical_specialty** *(string)*  
  Clinical domain relevant to the question.

- **evidence_certainty** *(string)*  
  Certainty level of the evidence (e.g., `high`, `moderate`, `low`).

- **fulltext_required** *(string: yes/no)*  
  Whether full-text articles are required to answer the question.

- **relevant_sources** *(list of strings)*  
  Identifiers (e.g., PubMed IDs) of supporting studies.

- **original_review** *(int)*  
  Identifier of the original systematic review.

- **review_year** *(int)*  
  Publication year of the systematic review.

- **source_concordance** *(float)*  
  Degree of agreement among sources supporting the answer.
