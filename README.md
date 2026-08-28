# Awesome LLM Hallucination in Research Applications

A curated collection of research papers, datasets, tools, implementations, and learning resources on **hallucination in large language models (LLMs), with a focus on research and scholarly-communication applications** — including citation fabrication, finding misattribution, and citation-integrity verification.

This repository accompanies an AI-assisted research paper on the same topic and documents the curation and verification process, including an independent citation-integrity audit of every reference used.

---

## Contents
- [Overview](#overview)
- [AI-Assisted Research Paper](#ai-assisted-research-paper)
- [Citation Integrity Audit](#citation-integrity-audit)
- [Survey Papers](#survey-papers)
- [Foundational Papers](#foundational-papers)
- [Recent Research](#recent-research)
- [Datasets](#datasets)
- [Tools and Libraries](#tools-and-libraries)
- [GitHub Implementations](#github-implementations)
- [Tutorials and Learning Resources](#tutorials-and-learning-resources)
- [Repository Structure](#repository-structure)
- [License](#license)

---

## Overview

Large language models are increasingly used across the research lifecycle — literature synthesis, hypothesis generation, citation retrieval, and manuscript drafting. Their tendency to produce fluent but unfounded content, known as **hallucination**, poses a distinct threat to research integrity: fabricated citations, misattributed findings, and invented statistics can enter the scholarly record with a false appearance of credibility.

This repository organizes the literature and tooling around three questions:

1. **What kinds of hallucination occur**, and how should they be classified? (See the [taxonomy paper](#ai-assisted-research-paper).)
2. **How prevalent is it in research-relevant contexts?** Reported rates vary substantially depending on model, domain, topic familiarity, and evaluation methodology. Examples are discussed in [Walters & Wilder (2023)](#foundational-and-research-papers), [Chelli et al. (2024)](#foundational-and-research-papers), [Dahl et al. (2024)](#foundational-and-research-papers), and [Linardon et al. (2025)](#foundational-and-research-papers).
3. **How can it be detected, mitigated, and independently verified before it reaches a published paper?** See [Tools and Libraries](#tools-and-libraries) and the [Citation Integrity Audit](#citation-integrity-audit).

Key problems covered in this collection include fabricated bibliographic citations, metadata mismatches, finding misattribution, numerical/statistical hallucination, methodological/reasoning hallucination, and domain-specific professional hallucination. Major technical directions include zero-resource detection (**SelfCheckGPT**), atomic fact verification (**FActScore**), fine-grained detect-and-edit systems (**FAVA**), retrieval-augmented generation (**RAG**), and domain-specific benchmarking such as **HaluEval** and **Med-HALT**.

---

## AI-Assisted Research Paper

### A Taxonomy of Hallucination Types in Large Language Models for Research Applications

A synthesis of the hallucination literature into a three-axis taxonomy — foundational distinctions (intrinsic/extrinsic, factuality/faithfulness), content-level categories (entity, relational, invented, contradictory, unverifiable, incomplete), and research-specific manifestations (citation fabrication, finding misattribution, numerical/statistical hallucination, methodological/reasoning hallucination, and domain-specific professional hallucination). The paper also reviews detection, mitigation, challenges, and future research directions.

[View Paper](hallucination_taxonomy_paper.docx)

---

## Citation Integrity Audit

Before references were included in the accompanying research paper, they were checked against authoritative bibliographic sources and secondary scholarly sources. The audit report documents the verification methodology, summary results, and per-reference checks.

**Result: 25/25 references verified. 0 fabricated. 0 metadata mismatches.**

[View Audit](Lab_1_AI_Assisted_Citation_Integrity_Audit-2.pdf)

---

## Survey Papers

| Paper | Year | Venue | Link |
|---|---:|---|---|
| [Survey of Hallucination in Natural Language Generation](https://doi.org/10.1145/3571730) — Ji et al. | 2023 | ACM Computing Surveys | [DOI](https://doi.org/10.1145/3571730) |
| [A Survey on Hallucination in Large Language Models](https://doi.org/10.1145/3703155) — Huang et al. | 2025 | ACM Transactions on Information Systems | [DOI](https://doi.org/10.1145/3703155) |
| [A Survey of Hallucination in Large Foundation Models](https://doi.org/10.48550/arXiv.2309.05922) — Rawte et al. | 2023 | arXiv | [arXiv](https://arxiv.org/abs/2309.05922) |

---

## Foundational Papers

| Paper | Year | Venue | Link |
|---|---:|---|---|
| [On Faithfulness and Factuality in Abstractive Summarization](https://doi.org/10.18653/v1/2020.acl-main.173) — Maynez et al. | 2020 | ACL | [DOI](https://doi.org/10.18653/v1/2020.acl-main.173) |
| [Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](https://doi.org/10.48550/arXiv.2005.11401) — Lewis et al. | 2020 | NeurIPS | [DOI/arXiv](https://doi.org/10.48550/arXiv.2005.11401) |
| [Language Models (Mostly) Know What They Know](https://doi.org/10.48550/arXiv.2207.05221) — Kadavath et al. | 2022 | arXiv | [arXiv](https://arxiv.org/abs/2207.05221) |
| [Calibrated Language Models Must Hallucinate](https://doi.org/10.48550/arXiv.2311.14648) — Kalai & Vempala | 2024 | arXiv | [arXiv](https://arxiv.org/abs/2311.14648) |

---

## Foundational and Research Papers

| Paper | Year | Main Topic | Link |
|---|---:|---|---|
| [SelfCheckGPT: Zero-resource Black-box Hallucination Detection for Generative Large Language Models](https://doi.org/10.18653/v1/2023.emnlp-main.557) — Manakul et al. | 2023 | Consistency-based detection | [DOI](https://doi.org/10.18653/v1/2023.emnlp-main.557) |
| [FActScore: Fine-grained Atomic Evaluation of Factual Precision in Long Form Text Generation](https://arxiv.org/abs/2305.14251) — Min et al. | 2023 | Atomic fact verification | [arXiv](https://arxiv.org/abs/2305.14251) |
| [HaluEval: A Large-Scale Hallucination Evaluation Benchmark for Large Language Models](https://arxiv.org/abs/2305.11747) — Li et al. | 2023 | Hallucination benchmark | [arXiv](https://arxiv.org/abs/2305.11747) |
| [Fine-grained Hallucination Detection and Editing for Language Models](https://doi.org/10.48550/arXiv.2401.06855) — Mishra et al. | 2024 | Detection and editing / FAVA | [arXiv](https://arxiv.org/abs/2401.06855) |
| [Semantic Uncertainty: Linguistic Invariances for Uncertainty Estimation in Natural Language Generation](https://arxiv.org/abs/2302.09664) — Kuhn et al. | 2023 | Semantic uncertainty | [arXiv](https://arxiv.org/abs/2302.09664) |
| [Hallucination Rates and Reference Accuracy of ChatGPT and Bard for Systematic Reviews](https://doi.org/10.2196/53164) — Chelli et al. | 2024 | Citation reliability | [DOI](https://doi.org/10.2196/53164) |
| [Fabrication and Errors in the Bibliographic Citations Generated by ChatGPT](https://doi.org/10.1038/s41598-023-41032-5) — Walters & Wilder | 2023 | Citation fabrication | [DOI](https://doi.org/10.1038/s41598-023-41032-5) |
| [Exploring the Boundaries of Reality: Investigating the Phenomenon of Artificial Intelligence Hallucination in Scientific Writing through ChatGPT References](https://doi.org/10.7759/cureus.37432) — Athaluri et al. | 2023 | Scientific citation hallucination | [DOI](https://doi.org/10.7759/cureus.37432) |
| [High Rates of Fabricated and Inaccurate References in ChatGPT-generated Medical Content](https://doi.org/10.7759/cureus.39238) — Bhattacharyya et al. | 2023 | Medical citation hallucination | [DOI](https://doi.org/10.7759/cureus.39238) |
| [A Preliminary Investigation of Fake Peer-reviewed Citations and References Generated by ChatGPT](https://doi.org/10.1080/00330124.2023.2190373) — Day | 2023 | Citation fabrication | [DOI](https://doi.org/10.1080/00330124.2023.2190373) |
| [Influence of Topic Familiarity and Prompt Specificity on Citation Fabrication in Mental Health Research Using Large Language Models](https://doi.org/10.2196/80371) — Linardon et al. | 2025 | Topic familiarity and citation fabrication | [DOI](https://doi.org/10.2196/80371) |
| [Large Legal Fictions: Profiling Legal Hallucinations in Large Language Models](https://doi.org/10.1093/jla/laae003) — Dahl et al. | 2024 | Legal hallucination | [DOI](https://doi.org/10.1093/jla/laae003) |
| [Hallucination-free? Assessing the Reliability of Leading AI Legal Research Tools](https://doi.org/10.48550/arXiv.2405.20362) — Magesh et al. | 2024 | RAG and legal research | [arXiv](https://arxiv.org/abs/2405.20362) |
| [Med-HALT: Medical Domain Hallucination Test for Large Language Models](https://aclanthology.org/2023.conll-1.25/) — Pal et al. | 2023 | Medical hallucination benchmark | [ACL Anthology](https://aclanthology.org/2023.conll-1.25/) |
| [RAGTruth: A Hallucination Corpus for Developing Trustworthy Retrieval-Augmented Language Models](https://aclanthology.org/2024.acl-long.585/) — Niu et al. | 2024 | RAG hallucination dataset | [ACL Anthology](https://aclanthology.org/2024.acl-long.585/) |
| [Artificial Hallucinations in ChatGPT: Implications in Scientific Writing](https://doi.org/10.7759/cureus.35179) — Alkaissi & McFarlane | 2023 | Scientific writing | [DOI](https://doi.org/10.7759/cureus.35179) |
| [Survey of Hallucination in Natural Language Generation](https://doi.org/10.1145/3571730) — Ji et al. | 2023 | General hallucination survey | [DOI](https://doi.org/10.1145/3571730) |
| [A Survey of Hallucination in Large Foundation Models](https://doi.org/10.48550/arXiv.2309.05922) — Rawte et al. | 2023 | Foundation-model hallucination survey | [arXiv](https://arxiv.org/abs/2309.05922) |
| [A Survey on Hallucination in Large Language Models: Principles, Taxonomy, Challenges, and Open Questions](https://doi.org/10.1145/3703155) — Huang et al. | 2025 | LLM hallucination survey | [DOI](https://doi.org/10.1145/3703155) |
| [Retrieval-Augmented Generation for Large Language Models: A Survey](https://doi.org/10.48550/arXiv.2312.10997) — Gao et al. | 2024 | RAG survey | [arXiv](https://arxiv.org/abs/2312.10997) |

---

## Recent Research

The paper identifies several active directions:

- **Detection:** SelfCheckGPT, FActScore, HaluEval, semantic uncertainty, and fine-grained verification.
- **Mitigation:** retrieval-augmented generation, fine-grained detect-and-edit systems, specialized factuality training, decoding interventions, and self-verification.
- **Research-specific reliability:** citation fabrication, finding misattribution, numerical/statistical hallucination, methodological/reasoning hallucination, and professional-domain hallucination.
- **Open problems:** research-oriented benchmarks, database-integrated citation verification, provenance-aware generation, calibration and abstention, cross-domain/cross-lingual validation, and human-AI verification workflows.

The accompanying paper emphasizes that RAG can reduce hallucination but does **not** eliminate failures of faithfulness to retrieved evidence. fileciteturn0file0L285-L303

---

## Datasets

The repository currently highlights five datasets/benchmark resources discussed in the research:

1. **HaluEval** — large-scale hallucination evaluation benchmark.
2. **TruthfulQA** — benchmark for truthful question answering.
3. **RAGTruth** — hallucination corpus for retrieval-augmented language models.
4. **Med-HALT** — medical-domain hallucination benchmark.
5. **FAVA-Data** — data associated with fine-grained hallucination detection and editing.

See [`datasets.md`](datasets.md) for the curated dataset descriptions and links.

---

## Tools and Libraries

The repository currently highlights:

- **SelfCheckGPT** — sampling-based, zero-resource hallucination detection.
- **FActScore** — atomic fact-level factuality evaluation.
- **FAVA** — fine-grained hallucination detection and editing.
- **Crossref API** — bibliographic metadata verification.
- **Semantic Scholar API** — scholarly literature retrieval and cross-checking.
- **DOI.org resolver** — DOI resolution and metadata validation.

The paper notes that citation-specific verification remains comparatively dependent on manual or semi-automated checking against bibliographic databases. fileciteturn0file0L281-L284

---

## GitHub Implementations

Official implementations associated with the research papers can be listed in [`github-repositories.md`](github-repositories.md).

The paper specifically discusses SelfCheckGPT, FActScore, FAVA, and related verification approaches; repository links should point to the corresponding official implementations where available.

---

## Tutorials and Learning Resources

Curated learning resources are listed in [`tutorials.md`](tutorials.md), including resources for:

- LLM hallucination research
- Prompt engineering
- Citation verification
- Crossref documentation
- PubMed documentation
- Scholarly literature retrieval

---

## Repository Structure

```text
awesome-llm-hallucination-research/
├── README.md
├── LICENSE
├── hallucination_taxonomy_paper.docx
├── Lab_1_AI_Assisted_Citation_Integrity_Audit-2.pdf
├── references.md
├── datasets.md
├── tools.md
├── github-repositories.md
└── tutorials.md
```

---

## License

Repository content (README, audit, curation notes) is released under the **MIT License** ([LICENSE](LICENSE)). Linked papers, datasets, and third-party repositories retain their own original licenses — see each entry for details. No copyrighted paper PDFs are redistributed in this repository; papers are linked to their DOI, publisher page, or arXiv/ACL Anthology record.
