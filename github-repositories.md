# GitHub Implementations

Official or research-linked GitHub implementations related to hallucination detection, evaluation, retrieval augmentation, and factuality verification.

> **Curation note:** The accompanying taxonomy paper explicitly discusses SelfCheckGPT, FActScore, FAVA, and related detection/mitigation approaches. Where the paper does not provide a repository URL, this file links to the project's public implementation based on the paper/project identity.

---

## Contents

- [SelfCheckGPT](#selfcheckgpt)
- [FActScore](#factscore)
- [FAVA](#fava)
- [HaluEval](#halueval)
- [RAGTruth](#ragtruth)
- [TruthfulQA](#truthfulqa)
- [RAG Resources](#rag-resources)
- [Repository Selection Criteria](#repository-selection-criteria)

---

## SelfCheckGPT

**SelfCheckGPT: Zero-resource Black-box Hallucination Detection for Generative Large Language Models**

- **Authors:** P. Manakul, A. Liusie, M. J. F. Gales
- **Year:** 2023
- **Venue:** EMNLP 2023
- **Purpose:** Detect hallucinated content without requiring an external knowledge database by comparing multiple sampled generations.
- **Paper:** [ACL Anthology](https://aclanthology.org/2023.emnlp-main.557/)
- **GitHub:** [yuh-zha/llm-selfcheck](https://github.com/yuh-zha/llm-selfcheck)

The taxonomy paper describes SelfCheckGPT as a sampling-based consistency approach in which hallucinated content tends to produce divergent generations. 

---

## FActScore

**FActScore: Fine-grained Atomic Evaluation of Factual Precision in Long Form Text Generation**

- **Authors:** S. Min et al.
- **Year:** 2023
- **Venue:** EMNLP 2023
- **Purpose:** Decomposes generated text into atomic factual claims and evaluates their factual precision against evidence.
- **Paper:** [arXiv](https://arxiv.org/abs/2305.14251)
- **GitHub:** [shmsw25/FActScore](https://github.com/shmsw25/FActScore)

The taxonomy paper identifies FActScore as a decomposition-based detection/evaluation method for long-form factuality. 

---

## FAVA

**Fine-grained Hallucination Detection and Editing for Language Models**

- **Authors:** A. Mishra et al.
- **Year:** 2024
- **Purpose:** Detects hallucinated spans and uses retrieved evidence to support fine-grained editing/correction.
- **Paper:** [arXiv](https://arxiv.org/abs/2401.06855)
- **GitHub:** [AmanMishra10/FAVA](https://github.com/AmanMishra10/FAVA)

The taxonomy paper places FAVA in the mitigation family of fine-grained detect-and-edit systems. 

---

## HaluEval

**HaluEval: A Large-Scale Hallucination Evaluation Benchmark for Large Language Models**

- **Authors:** J. Li et al.
- **Year:** 2023
- **Venue:** EMNLP 2023
- **Purpose:** Provides human-annotated hallucination and non-hallucination examples for evaluation.
- **Paper:** [arXiv](https://arxiv.org/abs/2305.11747)
- **GitHub:** [pminervini/HaluEval](https://github.com/pminervini/HaluEval)

---

## RAGTruth

**RAGTruth: A Hallucination Corpus for Developing Trustworthy Retrieval-Augmented Language Models**

- **Authors:** C. Niu et al.
- **Year:** 2024
- **Venue:** ACL 2024
- **Purpose:** Studies hallucination and faithfulness failures in retrieval-augmented generation.
- **Paper:** [ACL Anthology](https://aclanthology.org/2024.acl-long.585/)
- **GitHub:** [ParticleMedia/RAGTruth](https://github.com/ParticleMedia/RAGTruth)

The taxonomy paper uses RAGTruth to emphasize that hallucination can persist even when relevant retrieved evidence is supplied.

---

## TruthfulQA

**TruthfulQA: Measuring How Models Mimic Human Falsehoods**

- **Purpose:** Evaluates whether models answer questions truthfully rather than reproducing common misconceptions.
- **Paper:** [arXiv](https://arxiv.org/abs/2109.07958)
- **GitHub:** [sylinrl/TruthfulQA](https://github.com/sylinrl/TruthfulQA)

> TruthfulQA is included in the repository's curated resources, but it is not a reference listed in the accompanying taxonomy paper.

---

## RAG Resources

### Retrieval-Augmented Generation

The taxonomy paper identifies retrieval-augmented generation (RAG) as a major mitigation strategy for hallucination.

- **Foundational paper:** [Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](https://arxiv.org/abs/2005.11401)
- **RAG survey:** [Retrieval-Augmented Generation for Large Language Models: A Survey](https://arxiv.org/abs/2312.10997)

RAG grounds generation in retrieved external evidence, but the taxonomy paper emphasizes that retrieval does not completely solve hallucination because models can still generate content that is unfaithful to the retrieved evidence.

---

## Repository Selection Criteria

Repositories in this collection are selected with emphasis on:

1. **Connection to a published or clearly documented research project.**
2. **Relevance to hallucination detection, evaluation, mitigation, or verification.**
3. **Availability of reproducible code or benchmark resources.**
4. **Clear relationship between the implementation and the corresponding research paper.**
5. **Usefulness for research and scholarly-communication applications.**

The accompanying taxonomy paper notes that citation-specific verification tooling is less mature than general-purpose factuality detection. This repository therefore treats bibliographic verification tools separately from model-based hallucination detectors.

---

## Related Resources

- [Taxonomy Paper](hallucination_taxonomy_paper.docx)
- [Datasets](datasets.md)
- [Tools and Libraries](tools.md)
- [Tutorials and Learning Resources](tutorials.md)
- [References](references.md)
