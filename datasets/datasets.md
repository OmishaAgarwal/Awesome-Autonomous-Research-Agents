# Datasets and Benchmarks

This topic is measured primarily through agent/planning *benchmarks* rather than conventional training
datasets, so the entries below are the standard benchmark suites used across the papers in this
repository to expose and quantify planning-quality degradation.

- **GAIA**
  Source: Mialon et al., 2024 (Meta AI / Hugging Face). [Paper](https://arxiv.org/abs/2311.12983) ·
  [Leaderboard](https://huggingface.co/spaces/gaia-benchmark/leaderboard)
  Description: 466 real-world assistant questions requiring multi-step tool use and reasoning, rated by
  human difficulty.
  Use: Measures the gap between human (92%) and agent (historically ~15%) success on tasks that are
  conceptually simple but require coordinated multi-step planning.

- **SWE-bench**
  Source: Jimenez et al., 2024 (Princeton NLP). [Paper](https://arxiv.org/abs/2310.06770) ·
  [Project site](https://www.swebench.com/)
  Description: Real GitHub issues and their merged pull requests, pulled from popular Python
  repositories.
  Use: Tests long-horizon, multi-file code-planning ability; early frontier models resolved under 2% of
  issues, illustrating the planning gap in a coding-agent setting.

- **TravelPlanner**
  Source: Xie et al., 2024 (Ohio State University). [Paper](https://arxiv.org/abs/2402.01622) ·
  [Project site](https://osu-nlp-group.github.io/TravelPlanner/)
  Description: Multi-day travel-itinerary planning tasks requiring simultaneous satisfaction of many
  interdependent constraints (budget, transport, attractions, meals).
  Use: Isolates *joint* constraint-satisfaction failure — agents satisfy individual constraints but the
  final plan success rate collapses (0.6% for GPT-4) as constraint count grows.

- **PlanBench**
  Source: Valmeekam et al., 2023 (Arizona State University). [Paper](https://arxiv.org/abs/2206.10498) ·
  [Repository](https://github.com/karthikv792/LLMs-Planning)
  Description: Classical AI-planning domains (e.g., Blocksworld) with deterministic, fully observable
  state spaces and known optimal plans.
  Use: Controlled environment for separating genuine plan construction from retrieval of memorized
  commonsense plans, used as the basis for several lookahead-vs-step-wise-reasoning studies cited in
  this repository.

*Datasets in the conventional sense (e.g., labeled training corpora) are not the primary evidence base
for this topic; the above benchmark suites serve the equivalent evaluative role and are treated as the
dataset category per the assignment instructions.*
