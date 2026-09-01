# Awesome Planning-Quality Degradation in Long-Horizon Autonomous Research Agents

A curated collection of research papers, benchmarks/datasets, tools, implementations, and learning
resources on **planning-quality degradation** in long-horizon LLM-based autonomous agents — with a
particular focus on autonomous research agents (agents that perform literature review, experimentation,
and manuscript writing with limited human supervision).

This repository extends my AI-Tools-for-Research coursework (Topic T13, MCL2026006) by organizing the
AI-assisted paper I generated, the citation-integrity audit I performed on it, and a curated set of
independently verified resources on the same topic.

## Contents

- [Overview](#overview)
- [AI-Assisted Research Paper](#ai-assisted-research-paper)
- [Citation Integrity Audit](#citation-integrity-audit)
- [Curated Research Papers](#curated-research-papers)
  - [Survey Papers](#survey-papers)
  - [Foundational Papers](#foundational-papers)
  - [Benchmarks and Evaluation](#benchmarks-and-evaluation)
  - [Context and Memory Effects](#context-and-memory-effects)
  - [Error Compounding and Hallucination](#error-compounding-and-hallucination)
  - [Multi-Agent and Cross-Module Failure](#multi-agent-and-cross-module-failure)
  - [Autonomous Research Agents](#autonomous-research-agents)
- [Datasets and Benchmarks](#datasets-and-benchmarks)
- [Tools and Libraries](#tools-and-libraries)
- [GitHub Implementations](#github-implementations)
- [Tutorials and Learning Resources](#tutorials-and-learning-resources)
- [License](#license)

## Overview

As large language model (LLM) agents are given increasingly long-horizon, open-ended work — reviewing
literature, designing experiments, running code, and drafting manuscripts — a specific and separable
capability breaks down before raw task accuracy does: the agent's ability to form, revise, and execute a
coherent **plan** across many interdependent steps. This is distinct from a simple accumulation of
per-step errors.

Evidence for this "planning-quality degradation" comes from several directions: benchmarks such as GAIA,
SWE-bench, and TravelPlanner show a large gap between component-level competence and end-to-end
planning success; controlled studies show that context growth alone degrades model performance
("context rot," "lost in the middle"); autoregressive generation allows small errors to compound and
snowball across a trajectory; step-wise reasoning behaves as a greedy policy that under-weights delayed
consequences; and multi-agent/multi-module systems propagate a single root-cause failure into cascading
downstream errors. For autonomous **research** agents specifically, this problem is compounded by
methodological drift — benchmark-selection bias, data leakage, and post-hoc selection — that can produce
a fluent, well-formatted, but scientifically invalid output.

This repository collects the papers, benchmarks, tools, and implementations that document this
phenomenon and the mitigations proposed for it (explicit lookahead search, hierarchical subgoal
decomposition, structured context/memory management, and reflection-based self-correction), along with
open research gaps: standardized long-horizon research-workflow benchmarks, mechanistic accounts of
context effects, and planning-quality metrics that are separable from raw task success.

## AI-Assisted Research Paper

**Planning-Quality Degradation in Long-Horizon Autonomous Research Agents**
Generated with Claude (Sonnet 5) on 21 August 2026 as part of Lab 1 of this course.

[View Paper](paper/AI_Assisted_Research_Paper.pdf)

The paper synthesizes evidence for planning-quality degradation across five interacting mechanisms
(context-induced degradation, autoregressive error compounding, myopic step-wise reasoning, cross-module
failure propagation, and research-specific methodological drift), reviews current mitigations, and
proposes a research agenda.

## Citation Integrity Audit

Before curating this repository, all 27 references in the AI-generated paper were inventoried, and a
systematic sample of 10 references (first 3, last 3, and 4 spread through the middle, per the
prescribed sampling method) was independently verified against arXiv, publisher pages, and DOI/Crossref
records rather than accepted at face value. All 10 audited references were classified **A — Verified**
(publication exists, all checked metadata correct), giving an Authenticity Score of **100/100** and a
pre-verification prediction accuracy of 80%. Full methodology and evidence are in the audit worksheet.

[View Audit](citation-audit/Citation_Integrity_Audit.pdf)

Only references that passed this verification process (or are independently well-known, canonical
systems/tools in this field) are included in the curated lists below.

## Curated Research Papers

See [references/references.md](references/references.md) for the full list of 27 papers, organized into
the categories below with one-line relevance notes.

### Survey Papers
Broad syntheses of LLM agent architecture and planning.

### Foundational Papers
The core reasoning/acting/planning frameworks (Chain-of-Thought, ReAct, Tree of Thoughts, Reflexion,
LLM-Modulo, PlanBench) that later work builds on or critiques.

### Benchmarks and Evaluation
GAIA, SWE-bench, TravelPlanner, METR's time-horizon methodology, and the contested "Illusion of
Thinking" debate.

### Context and Memory Effects
Evidence that context length and position, independent of task difficulty, degrade agent and monitor
performance ("lost in the middle," "context rot," MemGPT, Voyager).

### Error Compounding and Hallucination
How small errors propagate and snowball across autoregressive generation.

### Multi-Agent and Cross-Module Failure
Large-scale failure-mode taxonomies for multi-agent systems and single-agent module pipelines.

### Autonomous Research Agents
Systems that automate the research pipeline itself, and audits of their methodological integrity.

*(Full annotated list with authors, venue, year, and identifiers: see*
*[references/references.md](references/references.md).)*

## Datasets and Benchmarks

See [datasets/datasets.md](datasets/datasets.md). This topic is benchmark-driven rather than
data-driven, so the "datasets" category here consists of the standard agent/planning benchmarks used to
measure planning-quality degradation (GAIA, SWE-bench, TravelPlanner, PlanBench).

## Tools and Libraries

See [tools/tools.md](tools/tools.md) for agent-orchestration frameworks and memory-management libraries
relevant to building and debugging long-horizon agents.

## GitHub Implementations

See [implementations/github-repositories.md](implementations/github-repositories.md) for official
reference implementations of the papers cited above.

## Tutorials and Learning Resources

See [tutorials/tutorials.md](tutorials/tutorials.md) for authoritative documentation, guides, and
lectures on building and evaluating long-horizon LLM agents.

## License

The original content of this repository (README text, categorization, descriptions, and the audit
worksheet) is released under the [MIT License](LICENSE). Linked external papers, tools, and datasets
retain their own original licenses/copyrights; no third-party copyrighted paper PDFs are redistributed
here — only links to publisher/arXiv/DOI records.
