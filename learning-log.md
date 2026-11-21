# AI Engineering Academy — Learning Log

> **Objective:** Become an independent, job-ready AI Engineer before starting a separate Cloud Engineering specialization.
>
> **Learning repository:** `MrGray17/ai-engineering-learning` (theory, exercises, assessments, resources, progress).
>
> **Practical project:** [AI Coding Agent Platform](https://github.com/MrGray17/AI-coding-agent-platform) (implementation and project delivery, tracked separately).
>
> **Last updated:** 2026-11-21

---

## 1. How to use this log

This is the source of truth for **demonstrated learning progress**, not simply a list of topics mentioned in conversation.

### Status definitions

- **Not started** — Not taught or assessed yet.
- **Introduced** — Explained, demonstrated or assigned, but comprehension has not been verified.
- **Understood with guidance** — Learner correctly reasons through an explanation or exercise with some hints.
- **Independently explained and applied** — Learner independently explains the mechanism, predicts behavior, identifies limitations and applies it to a new problem.

**Rule:** Never advance a status based solely on reading, watching a video or receiving an explanation. Record the evidence that justifies the status change.

### Learning protocol

**Understand → Predict → Attempt → Hint → Explain → Test → Review → Transfer → Retrieve**

- Introduce one focused concept at a time.
- Prefer learner predictions and independent attempts before hints or solutions.
- Require a teach-back, transfer exercise, or other evidence of understanding.
- Revisit old topics periodically with retrieval questions.
- Record misconceptions, corrections, assessment results, and next actions.
- Keep the scope on **AI Engineering first**. Cloud-specific study starts after AI Engineering readiness is established.
- Update this file during active learning sessions when progress is demonstrated or an assessment changes the record. Updates do not run automatically outside a session.

---

## 2. Baseline and goal

### Starting background

- Software engineering student.
- Existing programming/backend familiarity: Python, Java, TypeScript, Spring Boot, PostgreSQL, Git, Docker.
- Starting AI background: approximately zero foundational knowledge in AI, ML, deep learning, LLMs and agents.
- Motivating application: a Python-based AI coding agent that may evolve into a reliable, observable, sandboxed platform.
- Learning goal: independent engineering reasoning, not dependence on AI-generated code.

### Readiness standard

AI Engineering readiness will be assessed through independent demonstrations of the ability to:

1. Explain AI, ML, deep learning, LLMs and agent-system mechanisms.
2. Build robust LLM applications, retrieval systems, and tool-using agents.
3. Design evaluations; measure correctness, quality, latency, cost, and reliability.
4. Diagnose failures and address prompt injection, tool permissions, execution isolation, and recovery.
5. Design and defend production-oriented AI system architecture, with working tests and operational evidence.

**Important:** Completing lessons or the checklist is not in itself proof of job readiness. Final practical assessment and technical defense are required.

---

## 3. Conceptual progress

| Stage | Topic | Status | Evidence |
|---|---|---|---|
| 0 | AI vs traditional rule-based software | Introduced | Lesson 0.1 explanation; learner assessment pending |
| 0 | Artificial Intelligence (definition and scope) | Introduced | Lesson 0.1 explanation; learner assessment pending |
| 0 | Machine Learning (learning from data) | Introduced | Lesson 0.1 explanation; learner assessment pending |
| 0 | Deep Learning (multi-layer neural networks) | Introduced | Lesson 0.1 explanation; learner assessment pending |
| 0 | Large Language Models (learned language modeling) | Introduced | Lesson 0.1 explanation; learner assessment pending |
| 0 | Model, features, parameters, training vs inference, loss | Introduced | Lesson 0.2 explained and interactive parameter-fitting demonstration; assessment pending |
| 0 | Datasets, features, labels, splits, generalization and leakage | Introduced | Lesson 0.3 explanation and assessment assigned; understanding pending |
| 0 | Neural-network training, loss, gradient descent | Not started | — |
| 0 | Transformers and attention | Not started | — |
| 0 | Tokenization, context windows, sampling | Not started | — |
| 0 | Pretraining, fine-tuning, reinforcement learning | Not started | — |
| 0 | Inference mechanics, latency, throughput, cost | Not started | — |
| 1 | LLM APIs, prompting, structured outputs, streaming | Not started | — |
| 1 | Function and tool calling fundamentals | Not started | — |
| 2 | Agent vs workflow vs chatbot; execution loops | Not started | — |
| 2 | Agent state, tools, budgets, failure handling | Not started | — |
| 3 | Embeddings, vector similarity, semantic search | Not started | — |
| 3 | RAG, reranking, context engineering, memory | Not started | — |
| 4 | Evals, benchmarks, graders, experimental design | Not started | — |
| 4 | Statistical uncertainty and regression evaluation | Not started | — |
| 5 | Reliability, retries, durable execution, recovery | Not started | — |
| 5 | Prompt injection, permissions, sandboxing | Not started | — |
| 6 | AI backend architecture, queues, concurrency | Not started | — |
| 6 | Distributed AI execution and persistence | Not started | — |
| 7 | AI observability, traces, performance, deployment basics | Not started | — |
| 7 | Model serving and inference cost optimization | Not started | — |
| 8 | Advanced agents, MCP, multi-agent systems | Not started | — |
| 8 | Local inference, quantization, LoRA, fine-tuning | Not started | — |
| Final | Independent AI Engineering capstone and defense | Not started | — |

**Scope note:** AI-specific production engineering remains in scope. General AWS/cloud certifications, Terraform, Kubernetes administration, and broader Cloud Engineering are deferred.

---

## 4. Lesson journal

### 2026-11-21 — Stage 0, Lesson 0.1

**Lesson:** What exactly are AI, Machine Learning, Deep Learning, and LLMs?

**Status:** Introduced — **not passed yet**.

**Concepts presented:**
- Why explicitly written rules can be difficult for perception and language problems.
- AI as a broad field; learning is not required for every AI system.
- ML as learning useful behavior from examples.
- DL as machine learning using multi-layer neural networks.
- Modern LLMs as neural language models that generate token sequences.
- Distinction between model training and using the trained model for inference (initial introduction only).
- How learned model behavior differs from conventional software; why external tools and validation matter for coding agents.

**Assigned understanding checks (no recorded learner answer yet):**
1. A decision-tree model learns from labeled bug reports to predict severity. Which of AI, ML, DL, and LLM apply? Defend each inclusion/exclusion.
2. Compare a chess engine using manually designed search/evaluation with a chess neural network trained from positions. Explain what qualifies as AI, ML, and DL.
3. Explain in your own words why AI-generated code needs execution and validation instead of being trusted automatically.

**Assessment outcome:** Pending. No independent understanding demonstrated yet.

**Next action:** Learner answers Lesson 0.1 assessment; examiner challenges reasoning, records evidence, and only then decides whether to advance.

---

### 2026-11-21 — Stage 0, Lesson 0.2

**Lesson:** What is a model, and how does a machine actually learn?

**Status:** Introduced — **not passed yet**.

**Concepts presented:**
- Input feature and output prediction; a mathematical model such as `y_hat = w*x + b`.
- Parameters (weight and bias) change the model's behavior.
- Historical labeled examples; adjusting parameters to fit them.
- Error, mean squared error (MSE), and loss as signals for improving predictions.
- Training adjusts parameters; inference uses learned parameters.
- Initial idea of generalization: fitting the training examples does not ensure accuracy on unseen situations.

**Interactive exercise provided:** Fit a taxi-fare model using sliders for `w` and `b` on three examples (1 km → 3 MAD, 2 km → 5 MAD, 3 km → 7 MAD), observe MSE and predict a 4 km fare.

**Assessment outcome:** Partial correct answer: learner stated the taxi model 'learned incomplete' when the unseen night surcharge made the 4 km fare 12 MAD rather than the 9 MAD prediction. This correctly identifies an incomplete learned relationship. The response did not yet explain the missing nighttime feature or demonstrate transfer independently; mastery remains unverified.

**Next action:** Predict behavior for altered weights and a new example; distinguish training from inference; explain why zero training loss is not enough for deployment. Keep the Lesson 0.1 understanding check pending as well.

---

### 2026-11-21 — Stage 0, Lesson 0.3

**Lesson:** Training data, features and labels; generalization and train/validation/test splits.

**Status:** Introduced — **assessment pending**.

**Concepts presented:**
- Samples, features and labels in supervised machine learning.
- Memorization vs learning a generalizable relationship.
- Training, validation and test sets; why performance on previously seen data is insufficient.
- Data leakage, representative sampling, chronological and group-aware splits.
- Fitting a pattern under one condition may fail under a changed real-world condition.

**Understanding check:** Learner should propose where a nighttime surcharge belongs, diagnose misleading train/test evaluation, and explain what must change to improve the model. Do not mark independent mastery until reasoning and transfer are shown.

---

## 5. Reading and study resources

Use resources selectively as assigned. Completing them does not change mastery status.

### Beginning

- [MIT 6.S191 — Introduction to Deep Learning](https://introtodeeplearning.com/)
- [3Blue1Brown — Neural Networks](https://www.3blue1brown.com/topics/neural-networks)
- [Google Machine Learning Crash Course](https://developers.google.com/machine-learning/crash-course)
- [Andrej Karpathy — Neural Networks: Zero to Hero](https://karpathy.ai/zero-to-hero.html)
- [Hugging Face — LLM Course](https://huggingface.co/learn/llm-course/chapter1/1)

### Later

- [Stanford CS336 — Language Modeling from Scratch](https://cs336.stanford.edu/)
- [micrograd](https://github.com/karpathy/micrograd)
- [LLMs from Scratch](https://github.com/rasbt/LLMs-from-scratch)
- [Hugging Face Agents Course](https://huggingface.co/learn/agents-course/en/unit0/introduction)
- [mini-SWE-agent](https://github.com/SWE-agent/mini-swe-agent)
- [Inspect AI](https://inspect.aisi.org.uk/)
- [SWE-bench](https://github.com/SWE-bench/SWE-bench)
- [OWASP GenAI Security Project](https://genai.owasp.org/)

---

## 6. Assessment and retrieval history

| Date | Topic | Assessment | Outcome | Evidence / correction |
|---|---|---|---|---|
| 2026-11-21 | AI vs ML vs DL vs LLM | Lesson 0.1 reasoning questions assigned | Pending | No answers assessed yet |
| 2026-11-21 | Model parameters, training, inference and MSE | Taxi model generalization question | Partially correct | Learner correctly said 'it learned incomplete'; missing-feature explanation and transfer pending |
| 2026-11-21 | Dataset, features, labels and train/validation/test splits | Lesson 0.3 reasoning exercise assigned | Pending | Lesson introduced; understanding not assessed |

---

## 7. Next session

**Resume at:** Stage 0, Lesson 0.3 — answer generalization and dataset-split reasoning exercise. Lessons 0.1 and 0.2 mastery checks still pending.

**Immediate task:** Explain train/validation/test separation and data leakage using a fresh scenario; revisit the Lesson 0.1 classification question and Lesson 0.2 training/inference distinction through later cumulative retrieval.

**Promotion criteria:** Correct classifications; clear explanation of what is learned versus programmed; successful transfer to a new example; recognition of key limits. If hints are required, record **Understood with guidance**, not independent mastery.
