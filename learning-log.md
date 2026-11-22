# AI Engineering Academy — Learning Log

> **Objective:** Become an independent, job-ready AI Engineer before starting a separate Cloud Engineering specialization.
>
> **Learning repository:** `MrGray17/ai-engineering-learning` (theory, exercises, assessments, resources, progress).
>
> **Practical project:** [AI Coding Agent Platform](https://github.com/MrGray17/AI-coding-agent-platform) (implementation and project delivery, tracked separately).
>
> **Last updated:** 2026-11-22

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
| 0 | Datasets, features, labels, splits, generalization and leakage | Understood with guidance (partial) | Correctly proposed train/validation/test split after hint; test-set contamination and leakage transfer check pending |
| 0 | Loss optimization and gradient descent (initial scalar example) | Introduced | Lesson 0.4 explained with one-parameter taxi model; prediction and teach-back pending |
| 0 | Partial derivatives, gradient vectors, multi-parameter updates | Introduced | Lesson 0.5 worked two-parameter taxi model; independent calculation pending |
| 0 | Artificial neuron, weighted sum, bias, ReLU activation | Introduced | Lesson 0.6; independent prediction/teach-back pending |
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

**Understanding check (follow-up response):** Learner first said 'nope it might be overfittin' (correct suspicion, without evidence), then correctly proposed 'split the dataset to training validating and test' when asked how to evaluate fairly. This identifies the essential evaluation structure, but has not yet justified the purpose of each subset or how repeated test-set-based model changes compromise independence. **Status: Understood with guidance (for data splitting); independent application pending.**

---

### 2026-11-21 — Clarification: validation vs testing; what 'change the model' means

**Learner question:** "I don't understand the difference between the validation and test, also what do you mean by change your model"

**Evidence:** Learner previously correctly proposed a training/validation/test split after a hint, but explicitly reports uncertainty about the purpose of validation vs a final held-out test and what model improvement involves. Treat this as a meaningful gap; do not mark independent mastery.

**Clarification covered:**
- Training data is used to learn weights/parameters.
- Validation is used during development to choose and improve model architecture, features, hyperparameters and training procedures.
- A held-out test set is used for a final, less-biased estimate after model selection; repeatedly tuning against it contaminates the evaluation.
- Distinguish a training algorithm adjusting parameters from an engineer changing a model or its hyperparameters.

**Next assessment:** Ask learner to apply these distinctions to a new example before advancing.

---

### 2026-11-21 — Clarification: both validation and test data are unseen during weight training

**Learner question:** "still dont get it, both validation and test sets are new to the model"

**Evaluation:** Correct observation: both datasets are withheld from direct parameter training. The confusion is between *not training weights on data* and *not using evaluation feedback to influence development*.

**Clarification taught:**
- Training data directly influences learned parameters.
- Validation data influences model selection, hyperparameters, input features and other engineering choices *indirectly*; repeated validation-guided revisions can overfit to validation.
- Test data must remain independent of those development choices so it can provide an estimate of generalization.
- Once engineers change the model in response to test scores, they have effectively used the test set for validation; a fresh independent test is needed for the revised model.
- Example: model A scores 65% on validation; engineer adds attendance feature, trains model B and sees 88% validation; selected model B scores 81% on untouched test (illustrative numbers).

**Mastery status:** Not independently explained yet; direct comprehension check pending. Learner's correction was valuable and accurate.

---

### 2026-11-21 — Stage 0, Lesson 0.4: Gradient descent intuition and first update

**Status:** Introduced, not independently assessed.

**Teaching focus:**
- Return to a single labeled example: x=1 km, actual fare y=3 MAD.
- Hold bias b=1 fixed, leaving one learnable weight w; prediction is y_hat=w+1.
- Squared-error loss L(w)=(w-2)^2; derivative dL/dw=2(w-2).
- Gradient descent update: w_new=w-learning_rate*gradient.
- Worked example: start w=0, gradient=-4, learning rate 0.25, new w=1, loss drops 4→1. Repeating yields w=1.5, loss=0.25.
- Learning rate as update-size control; too large can cause overshoot or divergence. One-example simplified illustration; multi-parameter and mini-batch training later.
- Interactive experiment and prediction check included.

**Assessment:** Pending; learner must independently predict sign/direction and calculate next update with a different w.

---

### 2026-11-21 — Learner reports understanding of validation vs test distinction

Learner response: "now I get it, alright lets continue learning". Record **self-reported understanding**, not an independent teach-back or transfer check. Earlier validation/test reasoning remains guided; revisit in later cumulative retrieval.

---

### 2026-11-22 — Stage 0, Lesson 0.5: Multiple parameters and gradients

**Status:** Introduced — no independent demonstration yet.

**Reason for lesson:** Progress beyond the single-weight gradient descent case toward understanding how neural networks update many parameters.

**Concepts presented:**
- A simple model has both a weight and bias: `y_hat = w*x + b`.
- For sample `x=2`, `y=5`, use squared error `L=(2w+b-5)^2`.
- A **partial derivative** measures how loss changes when one parameter changes while others are fixed.
- Derivatives: `dL/dw = 2*(y_hat-y)*x`, `dL/db = 2*(y_hat-y)`.
- A **gradient** is the collection of these derivatives; apply the update rule to each parameter.
- Worked start `w=1, b=0`: prediction 2, loss 9, derivatives (-12,-6). At learning rate 0.05, new parameters `w=1.6,b=0.3`, prediction 3.5, loss 2.25.
- One training example is not enough to uniquely determine both parameters; many choices satisfy `2w+b=5`. Low training loss does not guarantee generalization.
- Interactive multi-parameter gradient descent example and one transfer question assigned.

**Assessment:** Pending. Also retain Lesson 0.4 single-parameter calculation as an unverified retrieval item.

---

### 2026-11-22 — Clarification: weight, bias, multiple parameters, and learning rate

**Learner's confusion (explicit):** Asked what learning rate is and how it is chosen, what multiple parameters are, interpreted `w` as finding a fare relationship such as doubling, and asked what bias means.

**Clarification provided:**
- From fares 3, 5, 7, 9 at distances 1, 2, 3, 4 km, the fare increases by **2** per additional kilometer; this is additive (+2), not doubling (×2). In `y_hat=w*x+b`, `w=2` is the slope/per-kilometer charge.
- `b=1` is an intercept; interpreted in the toy taxi scenario as a fixed starting fee. In general, bias is an additive offset, not necessarily a real-world fee.
- `w` and `b` are already two **learnable parameters**. Adding a nighttime indicator with its own weight gives three parameters (`w1,w2,b`).
- The **learning rate** `eta` is a training **hyperparameter**: a control on step size in `w_new=w-eta*gradient`; unlike weights and biases it is normally chosen/tuned, often with validation and observation of stability/training speed.
- Example at `w=0`, gradient -4: learning rates .10, .25, .50, 1.00 produce updated weights 0.4, 1, 2, 4. Larger is not always better.
- Important distinction: the chosen initial weight and bias in worked examples are pedagogical; actual training learns suitable values.

**Assessment:** No new independent answer yet. Mark the detailed distinction **Introduced / clarification needed**, not mastered. Ask learner to identify weight, bias, and learning rate from a fresh pricing example before introducing more gradients.

---

### 2026-11-22 — Stage 0, Lesson 0.6: The first artificial neuron

**Status:** Introduced; no independent assessment yet.

**Learner request:** Asked to move forward after a targeted clarification of weights, bias, and learning rate. These prerequisites are **not** marked mastered without teach-back.

**Concepts taught:**
- A neuron receives numerical inputs, multiplies each by its own weight, adds the terms and an additive bias: `z = w1*x1 + w2*x2 + b`.
- Illustrative spam-signal model: suspicious-phrase count and trusted-sender flag; positive and negative weights contribute differently.
- An activation function transforms the weighted sum. ReLU: `max(0,z)`.
- Nonlinearity allows multilayer networks to represent relationships that cannot be collapsed into one affine transformation.
- Toy activation score is not automatically a probability; actual models and interpretations depend on objectives and architectures.
- Training learns weights/biases; learning rate controls parameter adjustment *during training*, not neuron inference.

**Assessment pending:** Predict the weighted sum and ReLU output for a changed input, and explain the difference between weights, bias, and learning rate. No mastery assumed.

---

### 2026-11-22 — Clarification: why nonlinear activations matter

**Learner question:** Did not understand why stacking linear/affine weighted sums cannot represent more complex relationships, or why ReLU helps.

**Explanation provided:** 
- The composition of affine transformations remains affine: if `h=2x+1` and `y=3h+4`, then `y=6x+7`. Therefore, adding purely affine layers does not increase function-shape expressiveness.
- ReLU `max(0,z)` can introduce a change of slope (a kink). E.g. `h=ReLU(2x-2)`, `y=3h+1` gives output 1 for `x<=1`, and `6x-5` when `x>1`; this is not one straight line.
- Both weights and biases still matter; activations make composition nonlinear, enabling more complex functions.
- Independent comprehension check pending; do not promote mastery for receiving this explanation.

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
| 2026-11-21 | Dataset, features, labels and train/validation/test splits | Lesson 0.3 student-exam follow-up | Understood with guidance (partial) | Rejected in-sample accuracy, recognized possible overfitting, and proposed train/validation/test split after hint. Test-reuse thought experiment pending. |

| 2026-11-21 | Gradient descent first parameter update | Lesson 0.4 worked example; new-value prediction assigned | Pending | No learner gradient calculation or mechanism teach-back yet |

---

| 2026-11-22 | Partial derivatives and gradient-vector updates | Lesson 0.5 two-parameter calculation and transfer check | Pending | Lesson introduced; no independent answer submitted |

| 2026-11-22 | Artificial neuron, weighted sums and ReLU | Lesson 0.6 prediction assignment | Pending | Neuron explanation delivered; no independent response |

---

## 7. Next session

**Resume at:** Stage 0, Lesson 0.6 — explain why affine-only layers collapse into a single affine operation, and how ReLU changes the shape; previous gradient learning checks remain open.

**Immediate task:** Explain why `h=2x+1, y=3h+4` can become one equation but `h=ReLU(2x-2), y=3h+1` cannot be described by one straight line. Follow with a small numeric prediction and prior retrieval checks.

**Promotion criteria:** Correct classifications; clear explanation of what is learned versus programmed; successful transfer to a new example; recognition of key limits. If hints are required, record **Understood with guidance**, not independent mastery.
