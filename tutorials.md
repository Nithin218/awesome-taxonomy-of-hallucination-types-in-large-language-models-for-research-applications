# Tutorials and Learning Resources

A curated collection of tutorials, documentation, and learning resources for understanding, detecting, and mitigating hallucination in large language models, with an emphasis on research and scholarly-communication workflows.

The accompanying taxonomy paper highlights the importance of independent verification, retrieval grounding, uncertainty estimation, and human-in-the-loop workflows when using LLMs for research.

---

## Contents

- [Hallucination Research](#hallucination-research)
- [Prompt Engineering](#prompt-engineering)
- [Citation Verification](#citation-verification)
- [Crossref](#crossref)
- [PubMed](#pubmed)
- [Scholarly Literature Search](#scholarly-literature-search)
- [Recommended Learning Path](#recommended-learning-path)

---

## Hallucination Research

### Survey of Hallucination in Natural Language Generation

**Ji et al. (2023)**

A broad survey covering hallucination across summarization, dialogue, question answering, data-to-text generation, and machine translation.

- **Paper:** [ACM Digital Library](https://doi.org/10.1145/3571730)
- **arXiv:** [arXiv:2202.03629](https://arxiv.org/abs/2202.03629)

**Useful for:** Understanding the foundational definitions of hallucination, including the intrinsic/extrinsic distinction.

---

### A Survey on Hallucination in Large Language Models

**Huang et al. (2025)**

A comprehensive survey focused specifically on hallucination in LLMs, including taxonomy, causes, detection, mitigation, challenges, and open questions.

- **Paper:** [ACM Digital Library](https://doi.org/10.1145/3703155)
- **arXiv:** [arXiv:2311.05232](https://arxiv.org/abs/2311.05232)

**Useful for:** Understanding the factuality-versus-faithfulness framework used in the taxonomy paper.

---

### A Survey of Hallucination in Large Foundation Models

**Rawte et al. (2023)**

A survey covering hallucination in large foundation models.

- **Paper:** [arXiv:2309.05922](https://arxiv.org/abs/2309.05922)

**Useful for:** Broader background on hallucination beyond text-only LLMs.

---

## Prompt Engineering

### DAIR.AI Prompt Engineering Guide

A practical guide covering prompting techniques and principles for working with large language models.

- **Guide:** [DAIR.AI Prompt Engineering Guide](https://www.promptingguide.ai/)

**Useful for:** Learning how prompt design can influence model behavior and reliability.

> Prompting should not be treated as a substitute for independent factual or citation verification. The taxonomy paper notes that model self-verification remains only partially reliable.

---

## Citation Verification

Citation verification is especially important for research applications because a citation can be syntactically plausible while referring to a nonexistent or unrelated work.

### DOI

Use DOI resolution to check whether a DOI exists and resolves to the claimed scholarly work.

- **DOI Foundation:** [DOI.org](https://www.doi.org/)

**Useful for checking:**
- Whether a DOI resolves.
- Whether the resolved work matches the cited paper.
- Whether the DOI belongs to a different article.

---

### Crossref

Crossref provides bibliographic metadata and APIs that can be used to verify scholarly references.

- **Crossref:** [Crossref.org](https://www.crossref.org/)
- **Crossref REST API:** [api.crossref.org](https://api.crossref.org/)

**Useful for checking:**
- Title
- Authors
- Publication year
- Journal or conference
- DOI
- Bibliographic metadata

The taxonomy paper specifically identifies database-integrated citation verification as an important future direction.

---

### PubMed

PubMed is a major biomedical literature database and is particularly useful for checking medical and life-science citations.

- **PubMed:** [pubmed.ncbi.nlm.nih.gov](https://pubmed.ncbi.nlm.nih.gov/)
- **PubMed API documentation:** [NCBI E-utilities](https://www.ncbi.nlm.nih.gov/books/NBK25501/)

**Useful for checking:**
- Whether a biomedical paper exists.
- Article title and authors.
- Journal and publication information.
- PMID and related metadata.

---

## Scholarly Literature Search

### Semantic Scholar

Semantic Scholar provides scholarly literature search and metadata that can be used as a secondary verification source.

- **Semantic Scholar:** [semanticscholar.org](https://www.semanticscholar.org/)
- **API:** [Semantic Scholar API](https://api.semanticscholar.org/)

**Useful for:**
- Finding papers.
- Cross-checking metadata.
- Discovering related research.
- Checking author and citation information.

For high-integrity citation verification, bibliographic databases should be used as independent evidence rather than relying solely on an LLM's generated citation.

---

## Recommended Learning Path

For someone beginning research on LLM hallucination, the resources can be studied in this order:

### Step 1 — Understand hallucination

Start with:

1. Ji et al. — *Survey of Hallucination in Natural Language Generation*
2. Huang et al. — *A Survey on Hallucination in Large Language Models*
3. Rawte et al. — *A Survey of Hallucination in Large Foundation Models*

### Step 2 — Learn detection

Study:

1. **SelfCheckGPT** — consistency-based detection.
2. **FActScore** — atomic fact verification.
3. **HaluEval** — benchmark-based evaluation.
4. **Semantic uncertainty** — uncertainty-based detection.
5. **FAVA** — fine-grained detection and editing.

The taxonomy paper groups these into consistency-based, decomposition-based, and uncertainty-based detection approaches.

### Step 3 — Learn mitigation

Study:

1. **RAG** — grounding generation in external evidence.
2. **FAVA** — detect and edit hallucinated spans.
3. Specialized factuality training.
4. Decoding-time interventions.
5. Self-verification strategies.

Remember that RAG reduces hallucination but does not guarantee faithfulness to retrieved evidence.

### Step 4 — Apply it to research

Focus on:

- Citation fabrication
- Citation metadata mismatch
- Finding misattribution
- Numerical/statistical hallucination
- Methodological/reasoning hallucination
- Domain-specific hallucination

### Step 5 — Verify citations independently

For every AI-generated reference:

1. Search the title/author in a scholarly database.
2. Resolve the DOI if one is provided.
3. Compare the title, authors, venue, and year.
4. Open the actual paper.
5. Verify that the paper supports the claim being attributed to it.

This final step is particularly important because the existence of a real citation does not prove that the cited paper supports the statement.

---

## Related Resources

- [Taxonomy Paper](hallucination_taxonomy_paper.docx)
- [Datasets](datasets.md)
- [Tools and Libraries](tools.md)
- [GitHub Implementations](github-repositories.md)
- [References](references.md)
