# Artifact for "How Effective are Large Language Models in Generating Software Specifications?"

This repository contains the supplementary materials and experimental resources accompanying our paper. It includes full experimental results and all prompt files used in our studies.

The paper is published in the **Proceedings of the 2025 IEEE International Conference on Software Analysis, Evolution and Reengineering (SANER)**


## 📑 Contents

### 🔹 supplementary_material.pdf
Contains additional results for:
- **RQ3 (Section VI)**: Qualitative analysis on two other datasets: DocTer-data and CallMeMaybe-data.
- **RQ3 (Section VI.C)**: Generalizability studies across two other models: StarCoder-15.5B and GPT-3.
- **RQ4 (Section VII)**: Comprehensive results for LLMs' performance on all three datasets with different values of *K*.



### 🔹 prompts/

This directory includes all prompt files used across our experimental settings. It is subdivided by dataset and data type.

- 📂 **callmemaybe/**
    - Prompts for the CallMeMaybe-data.
    - Includes both SR (Semantic Retrieval) and noSR (Random Retrieval) conditions.
    - Example:
    - Ground truth is stored in `condition` entry of each data point.

- 📂 **docter/**
    - Prompts for the DocTer-data.
    - Subfolders: `mx`, `pt`, `tf` (library-specific prompt sets).
    - Ground truth is stored in `constr` entry of each data point.

- 📂 **jdoctor/**
    - Prompts for the Jdoctor-, organized by tag type: `paramTag`, `returnTag`, and `throwsTag`
    - Ground truth is stored in `condition` entry of each data point.




### 🔍 File Naming Convention

Each JSON prompt file follows the structure:
```
<tag>_<#examples>_<retrieval_method>.json
```
- **tag**: Task-specific tag: `returnTag`, `paramTag`, or `throwsTag` for Jdoctor-data; `tf`, `pt`, or `mx` for DocTer-data; Empty for CallMeMaybe-data
- **#examples**: Number of examples used in in-context learning (e.g., 10, 20, 40, 60)
- **retrieval_method**:
    - **SR**: Semantic Retrieval
    - **noSR**: Random Retrieval



### 📬 Citation

If you use this artifact or build upon our work, please cite our paper:

```
@inproceedings{xie2025effective,
  title     = {How Effective are Large Language Models in Generating Software Specifications},
  author    = {Xie, Danning and Yoo, Byungwoo and Jiang, Nan and Kim, Mijung and Tan, Lin and Zhang, Xiangyu and Lee, Judy S},
  booktitle = {Proceedings of the 2025 IEEE International Conference on Software Analysis, Evolution and Reengineering (SANER)},
  year      = {2025},
  organization = {IEEE}
}
```
