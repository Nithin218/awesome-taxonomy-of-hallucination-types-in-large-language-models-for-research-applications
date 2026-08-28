# Datasets and Benchmarks

A curated list of datasets and benchmark resources for evaluating, detecting, and studying hallucination in large language models, with an emphasis on research and scholarly-communication applications.

The accompanying taxonomy paper discusses hallucination detection and benchmarking across general-domain, retrieval-augmented, medical, and fine-grained hallucination settings. It also identifies the need for research-oriented benchmarks covering citation fabrication, finding misattribution, and numerical hallucination. 

---

## Contents

- [HaluEval](#halueval)
- [TruthfulQA](#truthfulqa)
- [RAGTruth](#ragtruth)
- [Med-HALT](#med-halt)
- [FAVA-Data](#fava-data)
- [Research Gaps](#research-gaps)

---

## HaluEval

**HaluEval: A Large-Scale Hallucination Evaluation Benchmark for Large Language Models**

- **Authors:** J. Li, X. Cheng, W. X. Zhao, J.-Y. Nie, J.-R. Wen
- **Year:** 2023
- **Venue:** EMNLP 2023
- **Purpose:** Large-scale evaluation of hallucinated and non-hallucinated model outputs.
- **Application:** General-purpose hallucination detection and benchmarking.
- **Paper:** [arXiv:2305.11747](https://arxiv.org/abs/2305.11747)
- **DOI:** Not listed in the accompanying taxonomy paper.

The taxonomy paper identifies HaluEval as a large, human-annotated benchmark for hallucination evaluation. 

---

## TruthfulQA

**TruthfulQA: Measuring How Models Mimic Human Falsehoods**

- **Purpose:** Evaluates whether language models produce truthful answers rather than reproducing common misconceptions or falsehoods.
- **Application:** Truthfulness and factuality evaluation.
- **Resource:** [TruthfulQA on GitHub](https://github.com/sylinrl/TruthfulQA)
- **Paper:** [TruthfulQA on arXiv](https://arxiv.org/abs/2109.07958)

> Note: TruthfulQA is included in this repository's curated dataset list, but the accompanying taxonomy paper does not provide a bibliographic entry for it. The links above are provided as the dataset's public resources.

---

## RAGTruth

**RAGTruth: A Hallucination Corpus for Developing Trustworthy Retrieval-Augmented Language Models**

- **Authors:** C. Niu, Y. Wu, J. Zhu, S. Xu, K. Shum, R. Zhong, J. Song, T. Zhang
- **Year:** 2024
- **Venue:** ACL 2024
- **Purpose:** Provides a corpus for studying hallucination in retrieval-augmented generation (RAG).
- **Application:** Detection and analysis of hallucinations that occur even when relevant retrieved evidence is provided.
- **Paper:** [ACL Anthology](https://aclanthology.org/2024.acl-long.585/)
- **Dataset/Project:** [RAGTruth GitHub repository](https://github.com/ParticleMedia/RAGTruth)

The taxonomy paper uses RAGTruth as evidence that hallucination can persist under retrieval augmentation because generated content may remain unfaithful to retrieved evidence. 

---

## Med-HALT

**Med-HALT: Medical Domain Hallucination Test for Large Language Models**

- **Authors:** A. Pal, L. K. Umapathi, M. Sankarasubbu
- **Year:** 2023
- **Venue:** CoNLL 2023
- **Purpose:** Benchmarks hallucination in medical-domain question answering.
- **Evaluation focus:** Reasoning-based and memory-based medical hallucination.
- **Paper:** [ACL Anthology](https://aclanthology.org/2023.conll-1.25/)

The taxonomy paper identifies Med-HALT as a domain-specific benchmark for medical hallucination and uses it as an example of high-stakes professional-domain evaluation.

---

## FAVA-Data

**FAVA-Data — Fine-grained Hallucination Detection and Editing**

- **Associated paper:** A. Mishra, A. Asai, V. Balachandran, Y. Wang, Y. Tsvetkov, G. Neubig, G. Hajishirzi
- **Year:** 2024
- **Purpose:** Supports fine-grained hallucination detection and editing.
- **Application:** Identifying hallucinated spans and retrieving evidence that can be used to correct them.
- **Paper:** [arXiv:2401.06855](https://arxiv.org/abs/2401.06855)

The accompanying taxonomy paper describes FAVA as a fine-grained retrieval-augmented detection-and-editing approach and identifies FAVA-Data among the repository's curated resources.

---

## Research Gaps

Existing hallucination benchmarks are valuable but do not fully cover the failure modes that matter in scholarly research.

The taxonomy paper specifically identifies the need for **research-oriented benchmarks** covering:

- **Citation fabrication** — generating nonexistent papers, authors, venues, or identifiers.
- **Finding misattribution** — citing a real paper while incorrectly describing its findings.
- **Numerical and statistical hallucination** — fabricated sample sizes, p-values, confidence intervals, effect sizes, or summary statistics.
- **Methodological and reasoning hallucination** — fabricated or internally inconsistent research procedures and reasoning chains.
- **Domain-specific professional hallucination** — failures in specialized areas such as legal and medical research.

The paper notes that existing benchmarks such as HaluEval and FActScore were developed primarily for general-domain or biography-style generation and do not directly evaluate citation fabrication, numerical hallucination, or literature-review generation. This motivates the development of dedicated scholarly-research benchmarks.

---

## Dataset Selection Notes

These resources cover complementary aspects of hallucination:

| Resource | Primary Focus | Domain |
|---|---|---|
| **HaluEval** | General hallucination evaluation | General |
| **TruthfulQA** | Truthfulness and factuality | General |
| **RAGTruth** | Hallucination under retrieval augmentation | RAG / General |
| **Med-HALT** | Medical hallucination | Medical |
| **FAVA-Data** | Fine-grained detection and editing | General / RAG |

For research and scholarly-communication systems, these benchmarks should be complemented by dedicated evaluations of **citation correctness, source attribution, numerical accuracy, and evidence faithfulness**.

---

## Related Resources

- [Taxonomy Paper](hallucination_taxonomy_paper.docx)
- [References](references.md)
- [Tools and Libraries](tools.md)
- [GitHub Implementations](github-repositories.md)
