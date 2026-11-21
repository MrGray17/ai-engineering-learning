# AI Engineering Academy — Roadmap

> **Career objective:** Become an independent, job-ready **AI Engineer** first. Begin a separate **Cloud / AI Infrastructure** specialization only after passing the AI Engineering readiness assessment.
>
> **Academy model:** Teacher-led, self-contained lessons from first principles; public courses, papers, docs, and source code are references, not required independent prerequisites.
>
> **Learning record:** [learning-log.md](./learning-log.md) — evidence of actual progress, not merely lessons delivered.
>
> **Implementation project:** [AI Coding Agent Platform](https://github.com/MrGray17/AI-coding-agent-platform) — project work stays in its own conversation/repository.
>
> **Source roadmap:** User-provided one-page **roadmap.sh — AI Engineer** PDF, reviewed 2026-11-21; see [interactive roadmap](https://roadmap.sh/ai-engineer).
>
> **Roadmap version:** 1.0 — 2026-11-21. A plan, not evidence of achievement.

---

## 1. Destination: What kind of AI Engineer?

A **software-oriented AI Engineer** who can:
- Understand model behavior rather than treating LLMs as magic.
- Build LLM-based applications, retrieval systems, and tool-using agents.
- Design evaluations and use data to improve quality.
- Engineer safety, security, cost control, and failure recovery.
- Deploy and operate a production-oriented AI application with appropriate observability.
- Independently read API documentation, research papers, and open-source code.
- Explain decisions and trade-offs in a professional technical interview.

This path is **not** primarily data science, ML research, or building frontier models from scratch. Nevertheless, foundational ML, deep learning, mathematical intuition, and hands-on model internals are mandatory. They make an AI engineer able to reason instead of just wiring together APIs.

**Not in scope yet:** cloud certification programs, general cloud architecture, AWS/Azure specialization, Kubernetes administration, Terraform, and unrelated infrastructure breadth. We will study *only the minimum deployment, containers, APIs, Linux, networking, and systems practices needed to engineer AI applications*. General Cloud Engineering comes later.

---

## 2. How this roadmap relates to the supplied roadmap.sh PDF

The uploaded PDF's main sequence is:

1. Introduction — AI Engineer vs ML Engineer; AI vs AGI; LLMs; inference/training; embeddings; RAG; agents; prompt engineering.
2. Using pretrained models — benefits, limitations, model options, context limits, knowledge cutoffs.
3. OpenAI API and prompting — model APIs, tokens, costs, prompt writing, fine-tuning.
4. AI safety and ethics — prompt injection, privacy, bias/fairness, adversarial testing, input/output constraints.
5. Open-source AI — models, Hugging Face, local inference with Ollama.
6. Embeddings and vector databases — semantic search, similarity, available providers.
7. RAG — chunking, embeddings, retrieval, generation, SDKs, frameworks.
8. AI agents — use cases, ReAct-style reasoning, manual tool integration and frameworks.
9. Multimodal AI — image, audio, video, generation and understanding.
10. Developer tools — AI code editors and code completion.

**We retain all core areas but strengthen the foundations, evaluation, reliability, security, and professional engineering standards.** Product names are examples, not a checklist of vendors to memorize. It is unnecessary to learn every listed vector database, provider, or framework.

### Important updates to the PDF

- The diagram references the **OpenAI Assistants API**. It was **sunset on August 26, 2026**. Study current APIs such as the Responses API instead; learn transferable API patterns rather than obsolete endpoints. [Migration guide](https://platform.openai.com/docs/assistants/migration).
- The diagram focuses heavily on *using* pretrained models. Our academy adds **why and how ML, deep learning, Transformers, and LLM inference work**.
- The diagram underemphasizes **evaluation engineering, reproducible experiments, model failure analysis, tool permissions, durable agent execution, observability, and production readiness**. These are essential, so they are core stages.
- Tools/frameworks should be learned **after** understanding their underlying mechanisms.
- Secure identity/permissions require proper application controls. Simply adding end-user identifiers to a prompt is not a substitute for authorization and access controls.

---

## 3. Prerequisites and learning principles

### Already available

- Python programming and some backend development experience.
- Working knowledge of Git, HTTP/JSON basics, SQL/PostgreSQL, and Docker.
- An AI Coding Agent Platform repository initialized with Python tooling.

### Taught when needed

- Python numerical computation and simple data structures for ML.
- Vectors, matrices, matrix multiplication, derivatives, the chain rule, gradients, probability and probability distributions.
- Autograd, neural-network training, tensors, optimization.
- API contracts, evaluation methodology, and production practices specific to AI.

### Mandatory learning loop

**Understand → Predict → Attempt → Hint → Explain → Test → Review → Transfer → Retrieve**

Every major topic must include:
1. The problem it solves.
2. Intuition and visuals.
3. Internal mechanism.
4. Concrete worked example or small Python experiment.
5. Trade-offs, limits, and failure cases.
6. Independent exercise with a prediction before the answer.
7. Teach-back and transfer challenge.

**No mastery by attendance:** Reading a lesson, watching a video, copying code, or passing a multiple-choice quiz alone does not prove independent competence.

---

## 4. Main curriculum — in dependency order

Legend: [ ] not started, [~] introduced (verified status lives in learning-log.md).

### Stage 0 — AI, ML, Deep Learning, and LLM Foundations

**Outcome:** Explain how learning-based systems work, why LLMs behave as they do, and what their fundamental limits are.

- [~] 0.1 AI vs ML vs deep learning vs LLMs; symbolic/rule-based AI vs learned models. **Introduced; learner assessment pending.**
- [ ] 0.2 What a model is; training vs inference; parameters vs hyperparameters.
- [ ] 0.3 Learning from examples: features, targets, datasets, train/validation/test splits.
- [ ] 0.4 Loss functions, optimization, gradient descent, learning rate, and overfitting.
- [ ] 0.5 Essential math: vectors, matrices, dot product, derivatives, chain rule, probability.
- [ ] 0.6 Neurons, weights, bias, activations, layers, forward passes.
- [ ] 0.7 Backpropagation and automatic differentiation; build a tiny neural network.
- [ ] 0.8 Language modeling and next-token prediction; why predictions can generalize.
- [ ] 0.9 Tokens and tokenizers; embeddings; positions and sequence structure.
- [ ] 0.10 Transformer architecture; attention, self-attention, and feed-forward blocks.
- [ ] 0.11 Pretraining, supervised fine-tuning, preference/post-training and reinforcement-learning concepts.
- [ ] 0.12 Decoding: temperature, top-p, sampling, context windows, hallucinations.
- [ ] 0.13 Reasoning-capable vs other models; model limitations and uncertainty.
- [ ] 0.14 Latency, throughput, token costs, and the distinction between local inference and API inference.

**Assessment gate:** Explain learned weights and inference from first principles; predict how changing data, sampling, and context affects behavior; interpret a small training experiment; analyze at least one failure case. Build or examine a minimal neural network sufficiently deeply to explain its parameter updates.

**Core references:**
- [Google Machine Learning Crash Course](https://developers.google.com/machine-learning/crash-course)
- [3Blue1Brown neural networks](https://www.3blue1brown.com/topics/neural-networks)
- [MIT 6.S191](https://introtodeeplearning.com/)
- [Karpathy Zero to Hero](https://karpathy.ai/zero-to-hero.html)
- [micrograd](https://github.com/karpathy/micrograd)
- [Hugging Face LLM Course](https://huggingface.co/learn/llm-course/chapter1/1)

### Stage 1 — LLM Application & Prompt Engineering

**Outcome:** Reliably integrate models into software, understand the request/response path, and produce validated outputs.

- [ ] 1.1 What happens across an LLM API call: client, server, authentication, HTTP, JSON, request/response.
- [ ] 1.2 Conversation messages, roles, instructions, hierarchy, and untrusted content.
- [ ] 1.3 Zero-shot, few-shot, decomposition, constraints, prompt design trade-offs.
- [ ] 1.4 Structured outputs: JSON Schema, validation, recovery on invalid results.
- [ ] 1.5 Function/tool calling: model proposal vs application execution.
- [ ] 1.6 Streaming, partial responses, cancellation, timeout and backpressure.
- [ ] 1.7 Model selection, routing, latency/cost/quality comparison, provider abstraction.
- [ ] 1.8 Prompt versioning, reproducible experiments, API errors and secrets handling.
- [ ] 1.9 Pretrained vs fine-tuned models; when prompting is sufficient.

**Assessment gate:** Explain the entire LLM request lifecycle; design robust validated inputs/outputs; distinguish model output from trusted program state; diagnose malformed responses and service failures.

**References:** [OpenAI API documentation](https://platform.openai.com/docs/), [OpenAI Cookbook](https://github.com/openai/openai-cookbook), [Hugging Face](https://huggingface.co/docs).

### Stage 2 — Agents & Harness Engineering

**Outcome:** Explain and independently design a transparent, controllable tool-using agent.

- [ ] 2.1 Chatbots vs workflows vs agents; when NOT to use an agent.
- [ ] 2.2 The agent loop: observe → model decision → tool call → execute → observe → stop/continue.
- [ ] 2.3 Tool schemas, tool registries, dispatch, validation and result handling.
- [ ] 2.4 State machines; session, run, task, and persistent state.
- [ ] 2.5 Plans, ReAct, reflection, feedback, and their limitations.
- [ ] 2.6 Budgets: steps, tokens, time, money, retries; stopping conditions.
- [ ] 2.7 Safe file and shell tooling; boundaries between model and host.
- [ ] 2.8 Failure modes: incorrect tools, malformed arguments, loops, partial completion.
- [ ] 2.9 Framework vs custom harness; when abstractions help or hinder.

**Assessment gate:** From a blank design, describe a complete agent loop with bounded execution and failure handling. Diagnose a stuck or unsafe agent by tracing actions and state. Compare an agent to a deterministic workflow.

**References:** [Anthropic — Building Effective Agents](https://www.anthropic.com/research/building-effective-agents), [Hugging Face Agents Course](https://huggingface.co/learn/agents-course/en/unit0/introduction), [mini-SWE-agent](https://github.com/SWE-agent/mini-swe-agent).

### Stage 3 — Context Engineering, Embeddings, Retrieval, and RAG

**Outcome:** Supply models with relevant, trustworthy information efficiently rather than dumping unfiltered context.

- [ ] 3.1 Context windows, tokens, relevance, truncation, compaction and summarization.
- [ ] 3.2 What embeddings represent; vector arithmetic, similarity measures, limitations.
- [ ] 3.3 Embedding models, semantic search, indexing and nearest-neighbor retrieval.
- [ ] 3.4 Vector search tools: FAISS, pgvector, Chroma/Qdrant as examples; **choose one**, not all.
- [ ] 3.5 Document ingestion: parsing, splitting/chunking, metadata, access controls.
- [ ] 3.6 RAG flow: retrieve → filter/rerank → assemble context → generate → verify.
- [ ] 3.7 Retrieval quality: recall, precision, reranking, groundedness and citations.
- [ ] 3.8 RAG vs fine-tuning vs long context vs tool access.
- [ ] 3.9 Conversational history, working memory, durable agent memory, long-running tasks.
- [ ] 3.10 Context poisoning, stale documents, authorization and data leakage.

**Assessment gate:** Defend a retrieval architecture; identify why a grounded answer failed; compare retrieval configurations with a test set and explain when no RAG system is needed.

**References:** [pgvector](https://github.com/pgvector/pgvector), [FAISS](https://github.com/facebookresearch/faiss), [Sentence Transformers](https://www.sbert.net/).

### Stage 4 — Evaluation Engineering

**Outcome:** Replace opinions and demo impressions with reproducible evidence about model and agent quality.

- [ ] 4.1 What is being evaluated: model, prompt, retrieval, tool use, end-to-end task.
- [ ] 4.2 Evaluation datasets, representative tasks, ground truth, correctness oracles.
- [ ] 4.3 Deterministic tests vs probabilistic evaluations; repeat trials.
- [ ] 4.4 Exact checks, programmatic graders, LLM-as-judge and grading bias.
- [ ] 4.5 Agent traces, action-sequence analysis, failure taxonomies.
- [ ] 4.6 Statistical uncertainty, comparison design, leakage and confounders.
- [ ] 4.7 SWE-bench, other benchmarks, and why leaderboard scores are insufficient.
- [ ] 4.8 Reliability vs cost: success rate, latency distribution, cost per successful task.
- [ ] 4.9 Regression tests and evaluation in the development lifecycle.
- [ ] 4.10 Red-teaming and adversarial evaluation.

**Assessment gate:** Design a representative evaluation suite; compare two systems fairly; state uncertainty and limitations; classify failures; recommend a change supported by measurements.

**References:** [Inspect AI](https://inspect.aisi.org.uk/), [SWE-bench](https://github.com/SWE-bench/SWE-bench), [OpenAI Evals](https://github.com/openai/evals).

### Stage 5 — AI Reliability, Security, and Safety

**Outcome:** Control uncertain models and dangerous side effects in the presence of errors, malicious inputs and partial failures.

- [ ] 5.1 Rate limits, timeouts, retries, exponential backoff and jitter.
- [ ] 5.2 Idempotency, checkpointing, resumable runs and durable execution.
- [ ] 5.3 Tool permission models, least privilege, user approvals, policy enforcement.
- [ ] 5.4 Prompt injection: instructions embedded in untrusted files, web pages and tool results.
- [ ] 5.5 Data privacy, secrets, access control, and tenant separation.
- [ ] 5.6 Sandboxed code execution and resource isolation.
- [ ] 5.7 Output validation, unsafe actions, audit logs and incident scenarios.
- [ ] 5.8 Threat modeling, adversarial tests, supply-chain and model risks.
- [ ] 5.9 Human-in-the-loop, uncertainty escalation, rollback and safe failure.

**Assessment gate:** Threat-model a coding agent, block unauthorized tool actions, recover safely from a crash, and explain why prompt instructions alone are not an effective security boundary.

**References:** [OWASP GenAI Security](https://genai.owasp.org/), [MITRE ATLAS](https://atlas.mitre.org/), [NIST AI RMF](https://www.nist.gov/itl/ai-risk-management-framework).

### Stage 6 — AI Backend & Platform Engineering

**Outcome:** Design the application and execution architecture needed for a reliable AI service.

- [ ] 6.1 Synchronous API requests vs asynchronous, long-running agent jobs.
- [ ] 6.2 API / service / repository boundaries and business-state ownership.
- [ ] 6.3 Queues, workers, concurrency, task scheduling and backpressure.
- [ ] 6.4 Database transactions, durable state, idempotency and failure recovery.
- [ ] 6.5 Model gateways, routing, caches, circuit breakers and budgets.
- [ ] 6.6 Concurrent agent sessions and isolated execution workspaces.
- [ ] 6.7 Service-to-service contracts; data consistency and replay.
- [ ] 6.8 Trade-offs: single process vs separate workers; simple vs distributed.

**Assessment gate:** Design a multi-user AI service with task persistence, bounded costs and crash recovery. Defend exactly where durable state lives and what happens under retries or duplicate requests.

**References:** [Temporal Python](https://docs.temporal.io/develop/python), [OpenHands](https://github.com/OpenHands/OpenHands).

### Stage 7 — Production AI Engineering, Observability, and Inference Operations

**Outcome:** Understand and operate AI software under realistic load and failure conditions. This is AI-specific production competence, **not yet the Cloud specialization**.

- [ ] 7.1 Containerized AI application and minimal deployment fundamentals.
- [ ] 7.2 Structured logs, metrics, traces, spans and trace propagation.
- [ ] 7.3 AI traces: prompts, model choices, tokens, tool invocations and outcomes.
- [ ] 7.4 Latency analysis: TTFT, total duration, queueing and tool delays.
- [ ] 7.5 Throughput, concurrency, load tests, saturation and resource bottlenecks.
- [ ] 7.6 Inference serving basics: batching, cache, quantization and GPU memory.
- [ ] 7.7 Cost attribution, token budgets, model routing and optimization.
- [ ] 7.8 Operational runbooks, incident response and regression monitoring.
- [ ] 7.9 Quality/latency/cost trade-offs and deployment acceptance criteria.

**Assessment gate:** Investigate a slow or failing system with traces and metrics; propose a measurable fix and demonstrate its effect. Explain operational risk and costs.

**References:** [OpenTelemetry Python](https://opentelemetry.io/docs/languages/python/), [Arize Phoenix](https://github.com/Arize-ai/phoenix), [vLLM](https://github.com/vllm-project/vllm).

### Stage 8 — Advanced AI Systems, Open Source, and Multimodal

**Outcome:** Extend beyond a single text-model API without losing engineering discipline.

- [ ] 8.1 Open-weight vs closed model ecosystems; licenses and deployment trade-offs.
- [ ] 8.2 Hugging Face Hub and Transformers; local inference with Ollama.
- [ ] 8.3 Quantization and model-serving architecture; inference optimization.
- [ ] 8.4 Fine-tuning, PEFT/LoRA, datasets, experimental controls and when NOT to tune.
- [ ] 8.5 Multimodal inputs/outputs: image, audio, video, speech, OCR and structured perception.
- [ ] 8.6 Model Context Protocol (MCP): resources, tools, boundaries and trust.
- [ ] 8.7 Multi-agent architectures, orchestration, specialization and communication.
- [ ] 8.8 Planning approaches, long-horizon tasks, delegated execution and failure.
- [ ] 8.9 Reading modern research papers, unfamiliar codebases, and implementation trade-offs.

**Assessment gate:** Choose between API and local inference for a real scenario, justify or reject fine-tuning, design a multimodal capability, and assess whether additional agents actually improve performance.

**References:** [Hugging Face Hub](https://huggingface.co/docs/hub), [Ollama](https://github.com/ollama/ollama), [MCP Python SDK](https://github.com/modelcontextprotocol/python-sdk), [Stanford CS336](https://cs336.stanford.edu/), [nanochat](https://github.com/karpathy/nanochat).

---

## 5. Practical milestones and evidence

**Theory happens in this Academy conversation.** Architecture, application implementation, Git work, and project debugging happen in the separate project conversation. We still connect the ideas through assessments and examples.

| Milestone | Demonstrable artifact / outcome | Proves |
|---|---|---|
| M0 — Fundamentals | Independently explain and test a tiny learning model | ML/DL understanding |
| M1 — Model API | Small Python LLM client with validated responses and failure cases | API and LLM integration |
| M2 — Tool calling | Bounded tool-use loop with typed schemas and auditable events | Harness mechanics |
| M3 — Context/RAG | Search and answer over a corpus with access controls and retrieval tests | Retrieval quality |
| M4 — Evaluations | Dataset, graders, repeated trials and a comparison report | Empirical engineering |
| M5 — Safe agent | Limited-permission tools, injection tests and recoverable execution | Security/reliability |
| M6 — AI service | Persistent jobs, concurrent sessions, and failure recovery | Backend/system design |
| M7 — Operations | Traces, metrics, load tests, cost and latency measurements | Production readiness |
| M8 — Advanced capability | Justified multimodal, local-model, or fine-tuning extension | Appropriate specialization |
| Final — Independent capstone | Production-oriented AI system + tests + runbook + technical defense | Job-readiness evidence |

Milestones are **evidence targets**, not a claim that completed repository features imply competence. Some may be demonstrated within the AI Coding Agent Platform; additional small standalone exercises and assessments are required.

---

## 6. Readiness examination: when can I call myself an AI Engineer?

No arbitrary completion date. A **junior-level readiness** claim requires passing all six categories below with independent evidence:

1. **Foundations:** Explain training, inference, attention, tokenization, embeddings, sampling and limitations without notes.
2. **Implementation:** Design and build an LLM application, a RAG capability and a tool-using agent with clear contracts.
3. **Evaluation:** Define success, construct a representative benchmark, compare alternatives, explain uncertainty, and analyze failures.
4. **Reliability/security:** Demonstrate safe permissions, input/output validation, bounded tool execution, prompt-injection defenses, retries and crash recovery.
5. **Operations:** Measure p50/p95 latency, success rate, token/cost usage and failure modes; use traces to diagnose an incident.
6. **Professional judgment:** Complete an unfamiliar engineering problem and defend design decisions, trade-offs, tests and documentation in an interview-style examination.

**Capstone expectations:** reproducible setup; architecture document; threat model; evaluation dataset; automated tests; trace examples; measured performance; documented limitations; independent explanation.

A capstone cannot be passed by copying an AI-generated solution or by giving a demonstration that hasn't been tested.

**After the final assessment is passed:** start a separate Cloud / AI Infrastructure specialization (AWS/Azure/GCP, IAM, networks, Terraform, Kubernetes, platform/SRE operations, GPU clusters and large-scale serving). Do not conflate the two tracks.

---

## 7. Resources: how they will be used

The Academy teacher is the **primary instructional source**. External resources are selected to deepen or verify individual lessons; the learner should not need to finish whole external courses unassisted.

### Foundation teaching
- [Google ML Crash Course](https://developers.google.com/machine-learning/crash-course)
- [3Blue1Brown](https://www.3blue1brown.com/topics/neural-networks)
- [MIT Introduction to Deep Learning](https://introtodeeplearning.com/)
- [Karpathy Zero to Hero](https://karpathy.ai/zero-to-hero.html)
- [Dive into Deep Learning](https://d2l.ai/)

### Source code study
- [micrograd](https://github.com/karpathy/micrograd) — backpropagation.
- [LLMs from Scratch](https://github.com/rasbt/LLMs-from-scratch) — language-model internals.
- [mini-SWE-agent](https://github.com/SWE-agent/mini-swe-agent) — coding agent loop.
- [OpenHands](https://github.com/OpenHands/OpenHands) — larger AI engineering system.
- [pgvector](https://github.com/pgvector/pgvector) — embeddings in PostgreSQL.
- [vLLM](https://github.com/vllm-project/vllm) — inference operations.

### Production and evaluation
- [Hugging Face Agents Course](https://huggingface.co/learn/agents-course/en/unit0/introduction)
- [Inspect AI](https://inspect.aisi.org.uk/)
- [SWE-bench](https://github.com/SWE-bench/SWE-bench)
- [OWASP GenAI](https://genai.owasp.org/)
- [OpenTelemetry](https://opentelemetry.io/docs/)

As the ecosystem changes, verify current official documentation before recommending exact model names, endpoints, prices, SDK signatures, or deprecation timelines.

---

## 8. Learning-log synchronization rules

- **Roadmap:** Intended sequence, expected outcomes, assessment gates; not a completion report.
- **learning-log.md:** What has been taught, what the student actually demonstrated, misconceptions, assessments, and immediate next action.
- Update the learning log **after meaningful active lessons, exercises, or assessments**; do not invent automatic background updates.
- Status vocabulary:
  - **Not started**
  - **Introduced**
  - **Understood with guidance**
  - **Independently explained and applied**
- Give evidence and date whenever status changes.
- Review and revise this roadmap if evidence suggests that sequence, depth, or prerequisites should change.

### Current position (2026-11-21)

**Stage 0, Lesson 0.1 — AI vs ML vs Deep Learning vs LLMs.** Explanation delivered; understanding assessment **pending**. No concept marked independently mastered.

**Next learning action:** Learner responds to the bug-report decision-tree / chess-engine classification exercise, explains the reasoning, and completes a transfer check before moving to Lesson 0.2.
