# awesome-taxonomy-of-hallucination-types-in-large-language-models-for-research-applications
A taxonomy categorizing hallucination types in large language models, with a focus on their causes, characteristics, and implications for research applications.
# Awesome LLM Hallucination in Research Applications

A curated collection of research papers, datasets, tools, implementations, and learning resources on the topic of **hallucination in large language models, with a focus on research and scholarly-communication applications** — including citation fabrication, finding misattribution, and citation-integrity verification.

This repository accompanies an AI-assisted research paper on the same topic and documents the full curation and verification process, including an independent citation-integrity audit of every reference used.

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

Large language models (LLMs) are increasingly used across the research lifecycle — literature synthesis, hypothesis generation, citation retrieval, and manuscript drafting. Their tendency to produce fluent but unfounded content, known as **hallucination**, poses a distinct threat to research integrity: fabricated citations, misattributed findings, and invented statistics can enter the scholarly record with a false appearance of credibility.

This repository organizes the literature and tooling around three questions:

1. **What kinds of hallucination occur**, and how should they be classified? (See the [taxonomy paper](#ai-assisted-research-paper).)
2. **How prevalent is it in research-relevant contexts?** Documented rates range from single digits up to 88% depending on model, domain, and topic familiarity — see [Chelli et al. (2024)](references/references.md), [Dahl et al. (2024)](references/references.md), and [Linardon et al. (2025)](references/references.md).
3. **How can it be detected, mitigated, and independently verified before it reaches a published paper?** See [Tools](#tools-and-libraries) and the [Citation Integrity Audit](#citation-integrity-audit).

Key problems covered in this collection include: fabricated bibliographic citations (real-looking authors, journals, and DOIs attached to nonexistent papers), metadata mismatches (a real DOI pointing to the wrong article), finding misattribution (citing a real paper for a conclusion it did not reach), and the persistence of hallucination even under retrieval-augmented generation. Major directions covered include zero-resource detection (SelfCheckGPT), atomic fact verification (FActScore), fine-grained detect-and-edit systems (FAVA), and domain-specific benchmarking (legal and medical hallucination studies).

---

## AI-Assisted Research Paper

**A Taxonomy of Hallucination Types in Large Language Models for Research Applications**

A synthesis of the hallucination literature into a three-axis taxonomy — foundational distinctions (intrinsic/extrinsic, factuality/faithfulness), content-level categories (entity, relational, invented, contradictory, unverifiable, incomplete), and research-specific manifestations (citation fabrication, finding misattribution, numerical/statistical hallucination, methodological/reasoning hallucination, domain-specific professional hallucination) — grounded in 25 independently verified sources.

[View Paper](paper/AI_Assisted_Research_Paper.docx)

---

## Citation Integrity Audit

Before any reference was added to this repository or the accompanying paper, it was independently checked against an authoritative source (publisher page, DOI/Crossref, PubMed, or the paper's own GitHub repository) and a secondary source (Semantic Scholar, ACL Anthology, or a university research portal). The full methodology, summary statistics, and a per-reference verification table are documented in the audit report.

**Result: 25/25 references verified. 0 fabricated. 0 metadata mismatches.**

[View Audit](citation-audit/Citation_Integrity_Audit.pdf)

---

## Survey Papers

| Paper | Year | Venue |
|---|---|---|
| [Survey of Hallucination in Natural Language Generation](references/references.md#survey-and-review-papers) — Ji et al. | 2023 | ACM Computing Surveys |
| [A Survey on Hallucination in Large Language Models](references/references.md#survey-and-review-papers) — Huang et al. | 2025 | ACM TOIS |
| [A Survey of Hallucination in Large Foundation Models](references/references.md#survey-and-review-papers) — Rawte et al. | 2023 | arXiv |

Full entries with abstracts and DOIs: [`references/references.md`](references/references.md#survey-and-review-papers)

## Foundational Papers

| Paper | Year | Venue |
|---|---|---|
| [On Faithfulness and Factuality in Abstractive Summarization](references/references.md#foundational-papers) — Maynez et al. | 2020 | ACL |
| [Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](references/references.md#foundational-papers) — Lewis et al. | 2020 | NeurIPS |
| [Calibrated Language Models Must Hallucinate](references/references.md#foundational-papers) — Kalai & Vempala | 2024 | arXiv |
| [Language Models (Mostly) Know What They Know](references/references.md#foundational-papers) — Kadavath et al. | 2022 | arXiv |

Full entries: [`references/references.md`](references/references.md#foundational-papers)

## Recent Research

Includes detection/mitigation methods (SelfCheckGPT, FActScore, FAVA), benchmarks (HaluEval, TruthfulQA, RAGTruth, Med-HALT), and domain applications (legal hallucination, medical citation fabrication, mental-health topic-familiarity effects).

Full categorized list: [`references/references.md`](references/references.md)

---

## Datasets

5 verified datasets — HaluEval, TruthfulQA, RAGTruth, Med-HALT, FAVA-Data — each with source, description, application, and link.

[View Datasets](datasets/datasets.md)

## Tools and Libraries

6 verified tools — SelfCheckGPT, FActScore, FAVA, Crossref API, Semantic Scholar API, DOI.org resolver.

[View Tools](tools/tools.md)

## GitHub Implementations

8 verified official implementations tied to specific published papers, selected for documentation quality, maintenance activity, and reproducibility.

[View Implementations](implementations/github-repositories.md)

## Tutorials and Learning Resources

5 verified resources — curated paper lists, the DAIR.AI Prompt Engineering Guide, and official Crossref/PubMed documentation used for citation verification.

[View Tutorials](tutorials/tutorials.md)

---

## Repository Structure

```
awesome-llm-hallucination-research/
├── README.md
├── LICENSE
├── paper/
│   └── AI_Assisted_Research_Paper.docx
├── citation-audit/
│   └── Citation_Integrity_Audit.pdf
├── references/
│   └── references.md
├── datasets/
│   └── datasets.md
├── tools/
│   └── tools.md
├── implementations/
│   └── github-repositories.md
└── tutorials/
    └── tutorials.md
```

---

## License

Repository content (README, audit, curation notes) is released under the [MIT License](LICENSE). Linked papers, datasets, and third-party repositories retain their own original licenses — see each entry for details. No copyrighted paper PDFs are redistributed in this repository; all papers are linked to their DOI, publisher page, or arXiv record.
