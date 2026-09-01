# Tools and Libraries

Agent-orchestration frameworks, memory-management libraries, and evaluation tooling relevant to building
or debugging long-horizon LLM agents and studying planning-quality degradation.

- **LangChain / LangGraph**
  [langchain.com](https://www.langchain.com/) · [Docs](https://python.langchain.com/)
  Widely used framework for chaining LLM calls, tools, and memory; LangGraph adds explicit
  graph-structured control flow useful for modeling multi-step agent plans.

- **LlamaIndex**
  [llamaindex.ai](https://www.llamaindex.ai/) · [Docs](https://docs.llamaindex.ai/)
  Data-framework for connecting LLMs to external knowledge and managing retrieval context — relevant to
  mitigating context-induced degradation.

- **AutoGen**
  [microsoft.github.io/autogen](https://microsoft.github.io/autogen/) ·
  [GitHub](https://github.com/microsoft/autogen)
  Microsoft's framework for building multi-agent conversational systems; useful reference architecture
  for studying cross-agent failure propagation.

- **CrewAI**
  [crewai.com](https://www.crewai.com/) · [GitHub](https://github.com/crewAIInc/crewAI)
  Role-based multi-agent orchestration framework; a practical example of the multi-module/multi-agent
  architecture pattern discussed in Cemri et al. (2025).

- **Letta (formerly MemGPT)**
  [letta.com](https://www.letta.com/) · [GitHub](https://github.com/letta-ai/letta)
  Reference implementation of the MemGPT virtual-memory-style context management approach for stateful,
  long-running agents.

*(Each tool above is included because it directly implements or supports one of the mitigation
strategies — orchestration, retrieval/context management, or multi-agent coordination — discussed in
Section 4 of the AI-assisted paper.)*
