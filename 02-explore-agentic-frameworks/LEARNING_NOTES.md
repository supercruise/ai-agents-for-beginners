# Lesson 02 Learning Record — Explore AI Agent Frameworks

**Completed:** 2026-10-11  
**Assessment:** Short-answer quiz with applied design discussion  
**Status:** Completed with corrections incorporated

## Key understanding

AI agent frameworks provide structured support for building goal-driven, multi-step systems. In addition to model access, they can provide tool invocation, context and state management, task orchestration, feedback loops, and, where justified, coordination between specialized agents.

For the proposed preliminary bridge type, size, and location (TSL) assistant:

- Use Microsoft Agent Framework (MAF) to build and test agent logic, approved Python tools, and conversation workflows.
- Use Microsoft Foundry Agent Service when managed Azure deployment, scale, enterprise governance, and integrations such as Azure AI Search are needed.
- Prefer one bounded agent and deterministic calculation functions initially; introduce multiple agents only when distinct roles and clear handoffs offer a measurable benefit.

## Quiz questions, responses, and feedback

### 1. What problem does an AI agent framework solve that a general AI framework may not?

**Learner response:** An agent framework can use multiple agents that collaborate and coordinate. Agents can iterate, adapt, make decisions, and use flexible workflows.

**Feedback:** Correct. Agent frameworks support goal-driven, multi-step workflows and can coordinate specialized agents. They also add structured support for tools, context/state, planning, and task management beyond basic model access. Iteration does not automatically improve an agent: the system needs explicit feedback, evaluation, memory, or updates.

### 2. Name three capabilities agent frameworks commonly provide.

**Learner response:**

1. Agent collaboration and coordination.
2. Task automation and management.
3. Contextual understanding and adaptation.

**Feedback:** Correct. For the TSL assistant, task management can orchestrate retrieval and approved calculations, while context handling can retain validated project constraints. Multi-agent coordination should be added only when it provides a clear benefit.

### 3. Why are modular components useful during prototyping?

**Learner response:** Loosely coupled components are easier to test, replace, update, and expand individually than strongly coupled components.

**Feedback:** Strong answer. Modularity usually improves testability and safe iteration, although over-fragmentation can add integration complexity. For this project, it permits replacing a model connector, retrieval source, tool permission, or calculation function without rewriting the whole assistant.

### 4. When is a multi-agent design useful, and why should it not be used unnecessarily?

**Learner response:** It can be useful for complex and less well-scoped problems, allowing agents to be creative, flexible, and adaptive. A well-scoped, static problem does not benefit much from a multi-agent framework.

**Feedback:** The conclusion about static, deterministic workflows is correct: conventional automation or a bounded single agent is often better. A poorly scoped task should first be clarified, not automatically given more agents. Multi-agent design is justified when work has genuinely distinct roles, decomposable subproblems, useful parallelism, or clear handoffs—for example, separate retrieval, calculation, and review-preparation roles. It adds cost, latency, and coordination/error-propagation risk.

### 5. What is the role of a feedback loop? Does it retrain the model automatically?

**Learner response:** A feedback loop helps agents learn from interactions and improve; the learner was unsure whether it automatically retrains the model.

**Feedback:** A feedback loop can improve the **agent system**, but it does not automatically retrain the underlying model. It may trigger a revision after an evaluator finds missing citations, save a reviewed result to an approved knowledge store, reveal a tool-contract issue, or produce evaluation data for later governed changes to prompts, tools, retrieval, or model fine-tuning. For the TSL assistant, an engineer's correction should improve validation rules or retrieval behavior, not silently change an engineering calculation rule.

### 6. Compare MAF and Microsoft Foundry Agent Service.

**Learner response:** MAF is for building a production agent and rapid prototyping/pilots. Foundry Agent Service is for enterprise-scale solutions and works with services such as search and databases. Use MAF for smaller or pilot work and Foundry for more complex systems.

**Feedback:** Mostly correct. MAF is a production-ready SDK and is not limited to one agent or to prototypes; it supports agent logic, tools, conversation handling, Azure identity, and multi-agent workflows. Foundry Agent Service is the managed Azure platform for agent deployment, enterprise capabilities, and services such as Azure AI Search, Bing Search, and code execution. Recommended sequence: build and evaluate the TSL agent with MAF, then use Foundry Agent Service when managed deployment, scale, governance, and Azure integrations are required.

### 7. Explain the roles of an agent, tool, thread, message, and run.

**Learner response:**

- An agent contains an LLM, context, and tools to complete tasks and orchestration.
- Tools let an agent call functions or MCP servers; they are the agent's “hands.”
- A thread is a conversation record that tracks and traces interactions and can support performance review.
- The learner requested clarification about a run.

**Feedback:**

- **Agent:** A configured entity with a model, instructions, and available tools that handles a task.
- **Tool:** A bounded callable capability, such as a Python function, API integration, or other approved action.
- **Thread:** A container for the state and history of an interaction.
- **Message:** A unit of content added to a thread, such as a user request, tool result, response text, image, or file.
- **Run:** A specific execution of an agent against a thread. It processes relevant messages, may invoke tools, and generates new messages or other outputs. A run is an observable execution event, not hidden model “thinking.”

Example flow: create a thread for a preliminary-design request; add a message with validated project inputs; start a run for the TSL agent; allow it to call approved calculation tools; and add its source-cited preliminary report to the thread.

## Applied design challenge — starting direction

The minimum viable TSL assistant should use a bounded agent instruction, validated project inputs, deterministic calculation tools, and a source-cited preliminary output. It must label all results as preliminary, disclose assumptions and uncertainty, flag missing or conflicting inputs, and require responsible-engineer review before any design decision or issued document.

## Next step

Proceed to Lesson 03: Understanding AI Agentic Design Patterns. Evaluate which patterns best fit the TSL assistant, beginning with the simplest safe workflow before considering planning, multi-agent coordination, or reflection loops.
