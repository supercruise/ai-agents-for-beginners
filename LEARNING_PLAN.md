# AI Agents for Beginners — Learning Plan

**Status:** Draft — tailor after learner check-in
**Started:** 2026-10-05
**Last tailored:** 2026-10-06
**Course:** `AI Agents for Beginners` (Lessons 00–18)

## Course map

This repository teaches agent development with Python, Jupyter notebooks, Microsoft Agent Framework (MAF), and Microsoft Foundry. The recommended sequence begins with foundations, then introduces agent design patterns and practical capabilities, and finishes with production, deployment, local execution, and security.

| Milestone                 | Lessons | Outcome                                                                                        | Checkpoint                                 |
| ------------------------- | ------- | ---------------------------------------------------------------------------------------------- | ------------------------------------------ |
| 0. Environment            | 00      | A working Python/Jupyter environment and a chosen model-provider setup                         | Run a starter notebook or validate imports |
| 1. Foundations            | 01–03  | Explain what agents are, when to use them, and how core patterns differ                        | Quiz 1 + one-page design sketch            |
| 2. Agent capabilities     | 04–06  | Build or reason about tool use, agentic RAG, and trustworthy behavior                          | Quiz 2 + improve a small agent design      |
| 3. Orchestration          | 07–09  | Select planning, multi-agent, or metacognitive approaches deliberately                         | Quiz 3 + pattern-selection exercise        |
| 4. Production literacy    | 10–13  | Describe evaluation/production concerns, protocols, context engineering, and memory            | Quiz 4 + production readiness review       |
| 5. Framework and delivery | 14–18  | Apply MAF and make informed choices about computer use, deployment, local agents, and security | Capstone + Quiz 5                          |

## Default session rhythm

Use this only as a starting point; it will be adjusted for available time and experience.

1. Read the lesson README and watch its short video.
2. Write three notes: one key idea, one trade-off, and one question.
3. Run the corresponding notebook when account access and credentials are available; otherwise, read it actively and trace the control flow.
4. Complete a short retrieval quiz without notes.
5. Add a dated entry to the progress log below, including what was confusing.

Suggested session length: 60–90 minutes. A full lesson usually spans one or two sessions, depending on notebook setup and depth of experimentation.

## 10-week applied schedule

This schedule assumes **10 hours per week**, Microsoft Foundry access, and a mix of concepts, coding, and design practice. It is intentionally organized around outcomes rather than trying to give every lesson identical time. Reserve the final 30–60 minutes each week for the weekly knowledge check and progress-log update.

| Week | Lessons and focus                                     | Practical work                                                                                          | Evidence of progress                                            |
| ---- | ----------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| 1    | 00–01: setup and agent fundamentals                  | Configure the environment; run a starter notebook; write a bridge-workflow agent proposal               | Environment checklist; proposal; baseline Quiz 1 questions 1–2 |
| 2    | 02–03: frameworks and design patterns                | Compare two architecture choices for the proposal and defend one                                        | Pattern-selection design challenge; complete Quiz 1             |
| 3    | 04: tool use                                          | Implement or trace a narrowly scoped tool and document its schema, permissions, and failure behavior    | Tool contract and adversarial test cases                        |
| 4    | 05–06: agentic RAG and trustworthy agents            | Create a small, sanitized document corpus; require citations and design guardrails                      | Retrieval evaluation set; complete Quiz 2                       |
| 5    | 07–09: planning, multi-agent systems, and reflection | Choose the simplest orchestration for the capstone and add an escalation/review step                    | Architecture decision record; complete Quiz 3                   |
| 6    | 10: production agents                                 | Define offline evaluation cases, metrics, and observability requirements                                | Evaluation plan and test dataset outline                        |
| 7    | 11–13: protocols, context, and memory                | Design a context budget, memory policy, and integration boundary                                        | Context/memory design challenge; complete Quiz 4                |
| 8    | 14–15: MAF and computer use                          | Implement or inspect the capstone's core MAF workflow; assess whether browser/computer use is justified | Working vertical slice or a documented rationale not to use CUA |
| 9    | 16–17: scalable and local agents                     | Choose a deployment model and test a constrained end-to-end workflow                                    | Deployment decision record; smoke-test notes                    |
| 10   | 18: security and capstone review                      | Threat-model the assistant; run the final evaluation suite; present the result                          | Capstone brief/demo; complete Quiz 5                            |

**Time budget each week:** about 2 hours reading/video, 4 hours notebook/code exploration, 2.5 hours capstone work, 1 hour assessment/review, and 0.5 hours documentation. Weeks 4, 7, and 10 may shift more time toward the capstone.

## Provisional roadmap

### Phase 0 — Setup and orientation

- [ ] Read `00-course-setup/README.md`.
- [X] Confirm Python 3.12+ and Jupyter are available.
- [X] Use Microsoft Foundry as the course provider. *(Confirmed 2026-10-06.)*
- [ ] Record the first runnable notebook and any setup blockers.

### Phase 1 — What makes an agent?

- [X] Lesson 01: Intro to AI Agents and Agent Use Cases.
- [ ] Lesson 02: Exploring AI Agentic Frameworks.
- [ ] Lesson 03: Understanding AI Agentic Design Patterns.
- [ ] Deliverable: write a 5–8 sentence proposal for a bridge-engineering work task: user, goal, inputs, actions/tools, success measure, and risks.

### Phase 2 — Give agents useful, safe capabilities

- [ ] Lesson 04: Tool Use Design Pattern.
- [ ] Lesson 05: Agentic RAG.
- [ ] Lesson 06: Building Trustworthy AI Agents.
- [ ] Deliverable: revise the Phase 1 proposal with one tool, one knowledge source, at least two guardrails, and an evaluation case.

### Phase 3 — Coordinate reasoning and work

- [ ] Lesson 07: Planning Design Pattern.
- [ ] Lesson 08: Multi-Agent Design Pattern.
- [ ] Lesson 09: Metacognition Design Pattern.
- [ ] Deliverable: make a decision table that explains when a single agent, planning agent, multi-agent system, or reflection loop is appropriate for the proposal.

### Phase 4 — Make an agent dependable in practice

- [ ] Lesson 10: AI Agents in Production.
- [ ] Lesson 11: Using Agentic Protocols (MCP, A2A, and NLWeb).
- [ ] Lesson 12: Context Engineering for AI Agents.
- [ ] Lesson 13: Managing Agentic Memory.
- [ ] Deliverable: write a compact production brief covering evaluation, observability, context strategy, memory boundaries, and protocol integrations.

### Phase 5 — Build, ship, and secure

- [ ] Lesson 14: Exploring Microsoft Agent Framework.
- [ ] Lesson 15: Building Computer Use Agents.
- [ ] Lesson 16: Deploying Scalable Agents.
- [ ] Lesson 17: Creating Local AI Agents.
- [ ] Lesson 18: Securing AI Agents.
- [ ] Capstone: implement or thoroughly design a focused bridge-engineering work assistant. Include its architecture, tool contracts, safety controls, evaluation cases, deployment/local rationale, and an explicit threat model.

## Applied direction — bridge engineering

**Learner goal:** Use AI agents effectively at work.
**Domain:** AEC civil engineering, with emphasis on bridge engineering.
**Starting level:** Very comfortable with technical work; detailed Python/Jupyter/API baseline to confirm.
**Availability:** 10 hours per week.
**Platform access:** Microsoft Foundry is available.
**Learning balance:** Mix of concepts, coding, and design practice.
**Assessment preference:** Short-answer conceptual quizzes plus coding and design challenges.

### Recommended capstone: Bridge project information assistant

Build or design an assistant for a constrained, reviewable task such as answering questions over approved project documents (specifications, inspection notes, calculation narratives, standards excerpts licensed for this use, RFIs, or submittals). It should cite the governing source and section, distinguish supplied evidence from inference, state uncertainty, and route consequential judgments to the responsible engineer.

This is intentionally **not** an autonomous design or approval agent. It must not make final engineering decisions, stamp work, modify issued documents, or substitute for the engineer of record. The learning value is in building sound retrieval, tool use, context, evaluation, security, and human-review practices around high-consequence information.

### Candidate mini-projects

Choose one after Phase 1; all support the course sequence.

1. **Specification/RFI navigator:** Retrieve relevant clauses and draft a source-cited response for engineer review.
2. **Inspection-note triage assistant:** Classify and summarize supplied field notes, identify missing information, and create a review queue—without determining structural adequacy.
3. **Submittal comparison assistant:** Compare a supplier submittal against a provided requirement checklist and flag potential discrepancies for human disposition.
4. **Standards research assistant:** Search an approved, licensed document set and produce a traceable research brief; never present generated text as a governing code interpretation.

### Domain evaluation criteria

- **Traceability:** Every substantive claim links to an approved source and exact location where possible.
- **Faithfulness:** The assistant does not invent requirements, sources, units, loads, or calculations.
- **Safety boundary:** It clearly escalates design decisions, conflicts, incomplete evidence, and life-safety implications to a qualified human.
- **Confidentiality:** Access is scoped to the project and organization; sensitive project data does not enter unapproved services.
- **Usability:** Responses are concise enough to support an engineer's review workflow, with uncertainty and assumptions visible.

## Knowledge checks

Take each quiz closed-book first. A useful target is **80% plus an explanation of any missed answer**. We will replace or extend these questions as lessons are completed.

### Challenge format

Each weekly practical challenge is assessed with a short review: explain the design, identify a failure mode, and show the test or evidence that supports the decision. A coding challenge may be completed in a notebook; a design challenge may be a concise Markdown decision record. Code quality is less important than deliberate scope, traceability, tests, and a safe human-review boundary.

### Quiz 1 — Foundations (after Lessons 01–03)

1. In your own words, what distinguishes an AI agent from a single prompt-response interaction?
2. Give one example where an agent is a poor fit and explain why.
3. A system must decompose a goal into ordered, dependent steps. Which broad design pattern is most relevant, and what could go wrong without verification?
4. What two criteria would you use to choose an agentic framework for a new project?
5. Sketch an agent for a personal or work task. Identify its goal, available actions, and a measurable definition of success.

### Quiz 2 — Capabilities and trust (after Lessons 04–06)

1. Why should a tool’s input/output contract be explicit rather than described only informally in a prompt?
2. Contrast ordinary retrieval-augmented generation with agentic RAG.
3. Name two risks introduced when an agent can call external tools, and one mitigation for each.
4. A retrieved source conflicts with a user’s instruction. What should the agent do before acting, and why?
5. Write one evaluation case that tests whether an agent refuses or safely handles a risky request.

### Quiz 3 — Orchestration (after Lessons 07–09)

1. When can a multi-agent system add complexity without improving outcomes?
2. What is the role of a planning loop, and how should execution feedback change the plan?
3. What does metacognition contribute to an agent workflow?
4. Select the simplest appropriate architecture for each: a deterministic form-filling workflow; a research task needing revision; a task with independent specialist domains. Defend each choice.
5. What signals would tell you an orchestration design is failing?

### Quiz 4 — Production and context (after Lessons 10–13)

1. What is the difference between an offline evaluation and production monitoring?
2. Why is context engineering more than adding more tokens to a prompt?
3. Give one situation suited to short-term memory and one suited to durable memory. What privacy concern applies to each?
4. What problem do protocols such as MCP or A2A address?
5. Define one quality metric and one safety metric for your proposed agent.

### Quiz 5 — Delivery and security (after Lessons 14–18)

1. What factors would make you choose a local agent instead of a hosted deployment?
2. Why do computer-use agents require tighter safeguards than text-only agents?
3. Identify three attack surfaces in an agent that uses external tools and retrieved content.
4. Propose one least-privilege rule for a tool-using agent.
5. Describe your capstone’s architecture and explain how its evaluation, deployment approach, and security controls work together.

## Progress log

| Date       | Lesson / activity                                  | Evidence of learning                                                                              | Quiz score / notes        | Next step                                          |
| ---------- | -------------------------------------------------- | ------------------------------------------------------------------------------------------------- | ------------------------- | -------------------------------------------------- |
| 2026-10-05 | Plan created after reviewing the repository README | Identified the course structure: setup; fundamentals; patterns; production; MAF/delivery/security | Baseline not yet assessed | Tailor pace, goal, experience, and platform access |

## Learner profile — to complete together

- **Primary goal:** Use agents effectively at work.
- **Concrete project or domain:** AEC civil engineering, especially bridge engineering.
- **Current Python/Jupyter experience:** Learner reports being very comfortable (specific baseline to confirm).
- **Current AI/LLM/agent experience:**
- **Hours available per week and preferred session length:** 10 hours per week; session length to confirm.
- **Target completion date (if any):**
- **Preferred learning balance:** Mix of concepts, coding, and project work.
- **Access to Azure/Microsoft Foundry or another compatible provider:** Microsoft Foundry available.
- **Preferred assessment style:** Short-answer concept quizzes plus coding and design challenges.
- **Accessibility, language, or scheduling needs:**
- **Definition of success at the end of the course:**

## Plan changes

Record substantive changes here so the schedule reflects reality.

| Date       | Change                                                                    | Reason                                                                      |
| ---------- | ------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| 2026-10-05 | Created initial milestone plan                                            | Awaiting learner profile                                                    |
| 2026-10-06 | Chose an applied bridge-engineering direction and safety-bounded capstone | Learner wants to use agents at work and reports high technical comfort      |
| 2026-10-06 | Added a 10-week, 10-hour-per-week blended schedule                        | Microsoft Foundry access; concept, coding, and design assessments requested |
