# cpp-agentic-forge
An autonomous multi-agent system orchestrating LLMs to plan, generate, compile, and self-repair production-ready C++ code.

cpp_agentic_factory/
├── core/                   # Domain Logic & Interfaces
│   ├── llm/                # LLM Abstractions
│   ├── memory/             # Blackboard & RAG implementation
│   └── types.py            # Common dataclasses (Task, Artifact, Feedback)
├── agents/                 # Agent Implementations
│   ├── base_agent.py       # Abstract Base Class
│   ├── architect.py
│   ├── developer.py
│   └── qa_engineer.py      # Tester Agent
├── tools/                  # External Tools Adapters
│   ├── compilers/          # GCC/Clang Wrappers
│   ├── static_analysis/    # Clang-Tidy, CppCheck
│   └── sandboxing/         # Docker/Subprocess managers
├── workflows/              # Orchestration Logic (Graph definitions)
│   └── feature_cycle.py    # The main loop logic
├── config/                 # Configuration & Constants
│   └── settings.py
└── main.py                 # Entry Point