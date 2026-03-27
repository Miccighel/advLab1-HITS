# Analyzing AI Evaluation Benchmarks Through Information Retrieval and Network Science

This repository contains the released results and supplementary materials for studying **AI evaluation benchmarks** through an **information retrieval** and **network science** perspective.

The project analyzes benchmark results as a bipartite graph linking models and questions, with the goal of uncovering latent structure, assessing ranking stability, and identifying the influence of easier question subsets on leaderboard outcomes.

The released materials include serialized outputs and tabular exports derived from the experimental pipeline.

---

## Overview

Benchmarking plays a central role in the evaluation of both **information retrieval systems** and **large language models**. This project studies benchmark behavior through an IR-inspired graph-based approach originally developed for TREC evaluation settings.

A bipartite graph is constructed between models and benchmark questions, and **Kleinberg’s HITS algorithm** is applied to derive structural signals from the evaluation data.

Within this framework:

- **Model hubness** reflects a model’s tendency to perform well on easier questions
- **Question hubness** reflects a question’s ability to discriminate between more and less effective models

This perspective helps identify benchmark-induced biases and better understand the stability of model rankings.

---

## What is included

This repository hosts **results and supplementary artifacts** associated with the project. The released materials are provided in two main formats:

- **Serialized results bundles** (`.pkl`) for programmatic reuse
- **Tabular exports** (`.csv`) for direct inspection and analysis

The repository may also include **intermediate derived artifacts**, such as discretized or binarized representations and clustering labels, when relevant to the analyses.

---

## Benchmarks

The experiments consider seven multiple-choice QA benchmarks:

- **ARC-C**
- **CRASS**
- **MMLU**
- **RACE**
- **OpenBookQA**
- **SciQ**
- **HellaSwag**

For each benchmark question and model, evaluation is based on **per-question correctness**:

- `1` if the selected option matches the correct answer
- `0` otherwise

These values populate the effectiveness matrix used throughout the analysis.

**Note:** please refer to the original benchmark sources for the raw data.

---

## Models

The experiments use a pool of instruction-tuned LLMs, including the following models:

| Model | Params (Billions) |
|---|---:|
| EuroLLM-1.7B-Instruct | 1.7 |
| EuroLLM-9B-Instruct | 9 |
| Llama-3.1-Nemotron-70B-Instruct-HF | 70 |
| Llama-3.2-1B-Instruct | 1 |
| Meta-Llama-3-8B-Instruct | 8 |
| Meta-Llama-3.1-70B-Instruct | 70 |
| Meta-Llama-3.1-8B-Instruct | 8 |
| Ministral-8B-Instruct-2410 | 8 |
| Mistral-7B-Instruct-v0.1 | 7 |
| Mistral-Large-Instruct-2411 | 123 |
| Mistral-Nemo-Base-2407 | 12 |
| Mistral-Nemo-Instruct-2407 | 12 |
| Mistral-Small-Instruct-2409 | 22 |
| Mixtral-8x7B-Instruct-v0.1 | 46 |
| Nemotron-Mini-4B-Instruct | 4 |
| Phi-3-mini-128k-instruct | 3.8 |
| Phi-3-mini-4k-instruct | 3.8 |
| Pixtral-12B-2409 | 12 |
| Qwen2-VL-2B-Instruct | 2 |
| Qwen2.5-72B-Instruct | 72.7 |
| Qwen2.5-7B-Instruct | 7.62 |
| aya-expanse-32b | 32 |
| aya-expanse-8b | 8 |
| bloom-560m | 0.5 |
| bloom-7b1 | 7 |
| falcon-7b-instruct | 7 |
| gemma-1.1-2b-it | 2.51 |
| gemma-1.1-7b-it | 8.54 |
| gemma-2-27b-it | 27.2 |
| gemma-2-2b-it | 2 |
| gemma-2-9b-it | 9.24 |
| gemma-7b-it | 7 |
| zephyr-7b-beta | 7 |

---

## Reuse notes

This repository releases the **derived results and supplementary artifacts** used in the analyses. It is intended to support reuse and follow-up investigations on benchmark structure, ranking behavior, and question-level effects.

When using these materials, please document any additional processing steps, filtering choices, or transformations applied to the released outputs.

---

## Related publication

Simeoni, Gaia, Soprano, Michael, Lunardi, Riccardo, Roitero, Kevin, and Mizzaro, Stefano (2026). *Analyzing AI Evaluation Benchmarks Through Information Retrieval and Network Science*. In *Advances in Information Retrieval (ECIR 2026)*, pp. 349–359. Springer, Cham. https://doi.org/10.1007/978-3-032-21300-6_25