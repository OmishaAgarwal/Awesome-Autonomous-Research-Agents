# Curated Research Papers

All entries below are drawn from the AI-generated paper's reference list. A systematic 10-paper sample
(first 3, last 3, and 4 spread through the middle of the bibliography) was independently verified via
arXiv/DOI/publisher records as part of the citation-integrity audit (see `citation-audit/`); all 10
audited entries were classified **Verified**. Entries are organized by subtopic, not by their original
bibliography order.

Format follows: **Title** — Authors, Year, Venue — [Link] — one-line relevance note.

## Survey Papers

- **A Survey on Large Language Model Based Autonomous Agents**
  Wang, L., Ma, C., Feng, X., et al., 2024, *Frontiers of Computer Science*, 18(6), 186345.
  [DOI](https://doi.org/10.1007/s11704-024-40231-1)
  Broad survey of LLM agent architectures; frames task decomposition, memory, and reflection as
  recurring but incomplete solutions to long-horizon reliability.

- **Understanding the Planning of LLM Agents: A Survey**
  Huang, X., Liu, W., Chen, X., et al., 2024, arXiv:2402.02716.
  [arXiv](https://arxiv.org/abs/2402.02716)
  Survey specifically of LLM agent *planning* methods; used to motivate that no existing approach fully
  resolves horizon-length degradation.

## Foundational Papers

- **Chain-of-Thought Prompting Elicits Reasoning in Large Language Models**
  Wei, J., Wang, X., Schuurmans, D., et al., 2022, NeurIPS 2022. [arXiv](https://arxiv.org/abs/2201.11903)
  Establishes intermediate-reasoning prompting as the basis for later agent reasoning frameworks.

- **ReAct: Synergizing Reasoning and Acting in Language Models**
  Yao, S., Zhao, J., Yu, D., et al., 2023, ICLR 2023. [arXiv](https://arxiv.org/abs/2210.03629)
  Interleaves reasoning traces with executable actions; foundational agent control loop.

- **Tree of Thoughts: Deliberate Problem Solving with Large Language Models**
  Yao, S., Yu, D., Zhao, J., et al., 2023, NeurIPS 2023. [arXiv](https://arxiv.org/abs/2305.10601)
  Generalizes single-chain reasoning into search with lookahead/backtracking.

- **Reflexion: Language Agents with Verbal Reinforcement Learning**
  Shinn, N., Cassano, F., Berman, E., et al., 2023, NeurIPS 2023. [arXiv](https://arxiv.org/abs/2303.11366)
  Verbal self-critique as a lightweight substitute for weight updates; basis for reflection-based
  mitigation strategies.

- **LLMs Can't Plan, But Can Help Planning in LLM-Modulo Frameworks**
  Kambhampati, S., Valmeekam, K., Guan, L., et al., 2024, ICML 2024. [arXiv](https://arxiv.org/abs/2402.01817)
  Argues LLMs require external verifiers for genuine planning; central critique motivating this topic.

- **PlanBench: An Extensible Benchmark for Evaluating LLMs on Planning and Reasoning About Change**
  Valmeekam, K., Marquez, M., Olmo, A., et al., 2023, NeurIPS 2023 Datasets & Benchmarks Track.
  [arXiv](https://arxiv.org/abs/2206.10498)
  Controlled classical-planning benchmark separating genuine plan construction from memorized plans.

## Benchmarks and Evaluation

- **GAIA: A Benchmark for General AI Assistants**
  Mialon, G., Fourrier, C., Swift, C., et al., 2024, ICLR 2024. [arXiv](https://arxiv.org/abs/2311.12983)
  Human-easy, multi-step assistant tasks; shows a large human-vs-agent success gap (92% vs 15%).

- **SWE-bench: Can Language Models Resolve Real-World GitHub Issues?**
  Jimenez, C. E., Yang, J., Wettig, A., et al., 2024, ICLR 2024. [arXiv](https://arxiv.org/abs/2310.06770)
  Real-world multi-file coordination benchmark; early models resolved under 2% of issues.

- **TravelPlanner: A Benchmark for Real-World Planning with Language Agents**
  Xie, J., Zhang, K., Chen, J., et al., 2024, ICML 2024. [arXiv](https://arxiv.org/abs/2402.01622)
  Multi-constraint itinerary planning; isolates joint constraint-satisfaction failure specifically.

- **Measuring AI Ability to Complete Long Tasks**
  Kwa, T., West, B., Becker, J., et al., 2025, NeurIPS 2025. [arXiv](https://arxiv.org/abs/2503.14499)
  METR's time-horizon methodology; quantifies the exponential growth in agent task-length capability.

- **The Illusion of Thinking: Understanding the Strengths and Limitations of Reasoning Models via the
  Lens of Problem Complexity**
  Shojaee, P., Mirzadeh, I., Alizadeh, K., et al., 2025, arXiv:2506.06941.
  [arXiv](https://arxiv.org/abs/2506.06941)
  Reports abrupt planning-accuracy collapse in reasoning models beyond a complexity threshold.

- **Comment on "The Illusion of Thinking"**
  Lawsen, A., 2025, arXiv:2506.09250. [arXiv](https://arxiv.org/abs/2506.09250)
  Counter-argument that the collapse reflects output-token/evaluation-harness limits, not reasoning
  failure — included to show the field's measurement disputes are still active.

## Context and Memory Effects

- **Lost in the Middle: How Language Models Use Long Contexts**
  Liu, N. F., Lin, K., Hewitt, J., et al., 2024, *TACL*, 12, 157–173.
  [DOI](https://doi.org/10.1162/tacl_a_00638)
  U-shaped positional-retrieval effect in long contexts; foundational context-degradation evidence.

- **Context Rot: How Increasing Input Tokens Impacts LLM Performance**
  Hong, K., Troynikov, A., & Huber, J., 2025, Chroma Technical Report.
  [Report](https://research.trychroma.com/context-rot)
  Large-scale evaluation across 18 frontier models showing non-uniform accuracy degradation with input
  length.

- **MemGPT: Towards LLMs as Operating Systems**
  Packer, C., Wooders, S., Lin, K., et al., 2023, arXiv:2310.08560. [arXiv](https://arxiv.org/abs/2310.08560)
  Virtual-memory-style bounded context management for agents.

- **Voyager: An Open-Ended Embodied Agent with Large Language Models**
  Wang, G., Xie, Y., Jiang, Y., et al., 2023, arXiv:2305.16291. [arXiv](https://arxiv.org/abs/2305.16291)
  Persistent external skill library decoupling competence from context-window size.

- **Classifier Context Rot: Monitor Performance Degrades with Context Length**
  Martin, S., & Roger, F., 2026, arXiv:2605.12366. [arXiv](https://arxiv.org/abs/2605.12366)
  Shows context-induced degradation also impairs LLM-based *oversight* of long agent transcripts.

## Error Compounding and Hallucination

- **Beyond Exponential Decay: Rethinking Error Accumulation in Large Language Models**
  Arbuzov, M. L., Bei, S., Dong, Z., Kalaev, D., & Shvets, A., 2025, arXiv:2505.24187.
  [arXiv](https://arxiv.org/abs/2505.24187)
  Empirical scaling behavior of compounding errors across rollout length.

- **How Language Model Hallucinations Can Snowball**
  Zhang, M., Press, O., Merrill, W., Liu, A., & Smith, N. A., 2023/2024, ICML 2024.
  [arXiv](https://arxiv.org/abs/2305.13534)
  Shows models justify early mistakes with further false claims they can otherwise recognize as false.

## Multi-Agent and Cross-Module Failure

- **Why Do Multi-Agent LLM Systems Fail?**
  Cemri, M., Pan, M. Z., Yang, S., et al., 2025, arXiv:2503.13657. [arXiv](https://arxiv.org/abs/2503.13657)
  Annotates 1,600+ traces across 7 frameworks (41–86.7% failure rates); 14-mode failure taxonomy (MAST).

- **Where LLM Agents Fail and How They Can Learn From Failures**
  Zhu, K., Liu, Z., Li, B., et al., 2025, arXiv:2509.25370. [arXiv](https://arxiv.org/abs/2509.25370)
  Module-level (memory/reflection/planning/action) error-propagation study across ALFWorld, GAIA,
  WebShop.

- **Why Reasoning Fails to Plan: A Planning-Centric Analysis of Long-Horizon Decision Making in LLM
  Agents**
  Wang, Z., Wu, F., Wang, H., et al., 2026, arXiv:2601.22311. [arXiv](https://arxiv.org/abs/2601.22311)
  Shows step-wise reasoning behaves as a greedy policy; proposes FLARE lookahead/value-propagation
  mitigation.

## Autonomous Research Agents

- **The AI Scientist: Towards Fully Automated Open-Ended Scientific Discovery**
  Lu, C., Lu, C., Lange, R. T., et al., 2024, arXiv:2408.06292. [arXiv](https://arxiv.org/abs/2408.06292)
  End-to-end automated ideation/experimentation/writing/review pipeline.

- **Agent Laboratory: Using LLM Agents as Research Assistants**
  Schmidgall, S., Su, Y., Wang, Z., et al., 2025, ACL 2025 Findings, 5977–6043.
  [arXiv](https://arxiv.org/abs/2501.04227)
  Structured literature-review/experimentation/report-writing pipeline with human-in-the-loop.

- **The More You Automate, the Less You See: Hidden Pitfalls of AI Scientist Systems**
  Luo, Z., Kasirzadeh, A., & Shah, N. B., 2025, NeurIPS 2025. [arXiv](https://arxiv.org/abs/2509.08713)
  Audits two open-source AI-scientist systems for benchmark-selection bias, data leakage, metric misuse,
  and post-hoc selection — the direct source for the "methodological drift" mechanism.
