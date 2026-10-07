# Lesson 01 Learning Record — Intro to AI Agents

**Completed:** 2026-10-06  
**Assessment:** Short-answer quiz  
**Provisional score:** 8/10

## Key understanding

An agent can combine an LLM, context, and tools to pursue a defined goal. Unlike a single prompt-response chatbot, it can use relevant context, select and call tools, sequence actions, observe results, and adjust its approach. Improvement is not automatic: it requires deliberately designed feedback, evaluation, memory, or updates.

Core capabilities identified for an effective agent:

- Read and manage relevant context, such as conversation history and approved knowledge sources.
- Access tools to take bounded actions and complete tasks.
- Reason or plan, choose actions, and evaluate the outcome.
- Work toward a specific success criterion.
- Operate within safety boundaries and escalate high-consequence decisions to a qualified human.

## Proposed bridge-engineering agent

### Use case

An assistant for preliminary bridge type, size, and location (TSL) studies. It supports engineers by gathering validated project constraints, selecting approved workflows, invoking deterministic Python calculation functions, and generating a traceable preliminary-design report.

Example: after a validated span length and girder type are supplied, the agent may call an approved Python function to estimate a preliminary girder depth. A simplified illustrative rule might be a 100-foot span divided by 50, producing a 2-foot preliminary depth.

### Goal

Help an engineer prepare a preliminary bridge-design study efficiently while keeping the engineer responsible for design decisions.

### Candidate inputs

- Environmental report
- Right-of-way information
- Bridge location and validated geometry
- Design criteria and applicable requirements
- Geotechnical, hydraulic, seismic, and other project constraints when applicable

### Allowed actions

- Read approved, scoped project data and references.
- Call approved, deterministic Python functions for preliminary calculations.
- Produce a preliminary report that shows inputs, assumptions, calculations, sources, and uncertainty.
- Flag missing, conflicting, or out-of-range data for engineer review.

### Safety boundary

The assistant must not independently determine final type, size, or location; approve or stamp a design; alter issued documents; or present a preliminary calculation as final engineering judgment. All results must be clearly labeled as preliminary and require review by the responsible professional engineer.

## Quiz feedback

### 1. Agent versus chatbot

The response correctly identified context, tools, decision-making, and iterative workflows as important differences. To complete the definition, an agent also needs a defined goal and a control loop: decide, act, observe, and adjust.

### 2. Core capabilities

The response correctly included context, tool access, and iteration. Added capabilities are explicit goals/success criteria, planning/action selection, outcome evaluation, and human escalation/safety boundaries.

### 3. Suitable agent task

The TSL preliminary-design assistant is a strong use case. The agent should not infer critical engineering inputs from location alone; it must validate geometry and consider the project constraints that govern the calculation.

### 4. Task not suitable for autonomous delegation

The observation that a deterministic workflow may be better implemented as conventional automation than an agent is correct. For autonomous delegation specifically, final bridge type/size/location selection, approval, or stamping is unsuitable because it requires professional judgment, code interpretation, accountability, and reconciliation of incomplete or conflicting evidence.

### 5. Value of human approval

The response correctly identified the licensed professional engineer's review role. The reviewer should validate inputs, calculations, citations, governing requirements, omissions, and safety implications—not only whether generated prose appears reasonable.

### 6. Risks of a vague goal

The response correctly identified ambiguity about the requested task and tool-selection/hallucination risks. A specific success criterion also bounds scope, gives the agent a stopping condition, and makes results evaluable.

## Next step

Proceed to Lesson 02: Exploring AI Agentic Frameworks. Compare frameworks against the needs of the proposed TSL assistant: deterministic-tool integration, document retrieval, traceability, human approval, Microsoft Foundry compatibility, and deployment controls.
