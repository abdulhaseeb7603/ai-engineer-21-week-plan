# AI Engineer 21-Week Learning Plan

**21-Week Roadmap | 2.5 Hours/Day | 6 Days/Week | ~315 Total Hours**

Based on real 2026 job postings from LinkedIn, Indeed, EY, and ZipRecruiter.
Timeline adjusted from original 12-week plan after researching actual course durations.
Includes a math foundations week for beginners with no linear algebra/calculus background.

## Progress Overview

| Weeks | Phase | Focus | Hours | Status |
|-------|-------|-------|-------|--------|
| 0 | Math Foundations | Linear algebra, calculus, Python/NumPy basics | ~15h | Not Started |
| 1-3 | Transformer Internals | Attention, architecture, Karpathy course | ~38h | Not Started |
| 4-7 | Production RAG | Chunking, hybrid search, reranking, eval | ~55h | Not Started |
| 8-11 | LLM Fine-Tuning | LoRA, QLoRA, dataset curation, evaluation | ~50h | Not Started |
| 12-14 | Agent Systems | ReAct, LangGraph, MCP, tool use | ~46h | Not Started |
| 15-17 | LLMOps & Evaluation | Langfuse, RAGAS, testing, monitoring, K8s | ~55h | Not Started |
| 18-20 | Capstone Project | Build, deploy, launch a production AI product | ~50h | Not Started |

> **Start applying for jobs at Week 12** (after RAG + Fine-Tuning). Don't wait until Week 20.

---

## Phase 0: Math & Python Foundations (Week 0) ~15h

**Goal:** Build just enough math intuition to follow Karpathy's lectures without constantly Googling. This is NOT a full math course -- it's targeted prep for the specific concepts you'll encounter in Weeks 1-3.

### Week 0: Math for Deep Learning
- [3Blue1Brown - Essence of Linear Algebra (~3.5h)](https://youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab)
- [3Blue1Brown - Essence of Calculus (~3h)](https://youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr)
- [Khan Academy - Matrices](https://www.khanacademy.org/math/precalculus/x9e81a4f98389efdf:matrices)
- [Python NumPy Tutorial (freeCodeCamp)](https://www.youtube.com/watch?v=QUT1VHiLmmI)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | 3B1B Essence of Linear Algebra: Ch 1-5. Vectors, linear combinations, spans, basis vectors. | 2.5h | |
| 2 | 3B1B Essence of Linear Algebra: Ch 6-10. Matrix multiplication, determinants, dot/cross products. | 2.5h | |
| 3 | 3B1B Essence of Linear Algebra: Ch 11-16. Eigenvectors, abstract vector spaces. Khan Academy matrix practice. | 2.5h | |
| 4 | 3B1B Essence of Calculus: Ch 1-5. Derivatives, chain rule, product rule, exponentials. | 2.5h | |
| 5 | 3B1B Essence of Calculus: Ch 6-11. Integration, higher-order derivatives, Taylor series. | 2.5h | |
| 6 | Python NumPy crash course. Practice: matrix ops, broadcasting, reshaping. Write a simple dot product + gradient by hand. | 2.5h | |

**What you need to remember for Karpathy's course:**
- **Vectors & matrices**: What they are, how to multiply them (this is ALL of neural networks)
- **Dot product**: How two vectors combine to produce a single number (this is attention)
- **Derivatives & chain rule**: How small changes propagate (this is backpropagation)
- **Softmax**: Turning numbers into probabilities (watch for this in Week 3)

> Don't stress about mastering everything. The goal is *recognition* -- when Karpathy says "we take the dot product of Q and K", you should think "oh, that's multiplying two vectors" rather than being lost.

**Phase 0 Checkpoint:** Can multiply matrices by hand, explain what a derivative measures, and use NumPy for basic array operations.

---

## Phase 1: Transformer Internals & PyTorch (Weeks 1-3) ~38h

**Goal:** Understand what happens inside LLMs so you can debug, optimize, and discuss them in interviews.

### Week 1: Neural Networks from Scratch (Part 1)
- [Karpathy - Zero to Hero](https://karpathy.ai/zero-to-hero.html)
- [GitHub Repo](https://github.com/karpathy/nn-zero-to-hero)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Lecture 1: Micrograd (2h30m video) - Watch first half, code along. Understand backprop basics. | 2.5h | |
| 2 | Lecture 1: Micrograd - Watch second half, complete autograd engine from scratch. | 2.5h | |
| 3 | Lecture 2: Makemore pt1 (1h57m video) - Watch and code along. Bigram model, torch.Tensor. | 2.5h | |
| 4 | Lecture 2: Makemore pt1 - Finish coding, experiment with the model. Language modeling basics. | 2.5h | |
| 5 | Lecture 3: Makemore pt2 MLP (1h15m video) - Watch and code along. MLP character model, training. | 2.5h | |
| 6 | Lecture 3: MLP - Finish implementation. Experiment with learning rate, train/dev/test splits. | 2.5h | |

### Week 2: Neural Networks from Scratch (Part 2)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Lecture 4: Makemore pt3 (1h55m video) - Watch first half. Forward pass activations, gradients. | 2.5h | |
| 2 | Lecture 4: Makemore pt3 - Watch second half. Batch Normalization, code along. | 2.5h | |
| 3 | Lecture 5: Makemore pt4 (56m video) - Manual backprop through the entire network. | 2.5h | |
| 4 | Lecture 6: WaveNet (56m video) - Build deeper network with tree-like structure. torch.nn internals. | 2.5h | |
| 5 | Review & consolidation - Re-implement micrograd from memory. Review all makemore parts. | 2.5h | |
| 6 | Exercises - Complete Karpathy's suggested exercises from lectures 1-6. | 2.5h | |

### Week 3: Transformers & GPT
- [Karpathy - Let's Build GPT (1h56m)](https://youtube.com/watch?v=kCc8FmEb1nY)
- [Karpathy - GPT Tokenizer (2h13m)](https://youtube.com/watch?v=zduSFxRajkE)
- [3Blue1Brown - Attention Explained (~25m)](https://youtube.com/watch?v=eMlx5fFNoYc)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Let's Build GPT (1h56m video) - Watch first half. Self-attention, key/query/value. Code along. | 2.5h | |
| 2 | Let's Build GPT - Watch second half. Complete implementation, train your mini-GPT. | 2.5h | |
| 3 | 3Blue1Brown attention video (25m) + Read "Attention Is All You Need" paper (sections 3.1-3.3). | 2.5h | |
| 4 | GPT Tokenizer video (2h13m) - Watch first half. Understand BPE, why tokenization matters. | 2.5h | |
| 5 | GPT Tokenizer - Watch second half. Run HF Transformers inference with pre-trained model. | 2.5h | |
| 6 | Consolidation - Rewrite attention from memory. Draw transformer architecture, explain each part. | 2.5h | |

**Phase 1 Checkpoint:** Can explain attention, build a mini-GPT, and run HF models with PyTorch.

---

## Phase 2: Production RAG (Weeks 4-7) ~55h

**Goal:** Go from "I can build RAG" to "I can build RAG that works reliably at scale with proper evaluation."

### Week 4: RAG Foundations (Coursera Course)
- [DeepLearning.AI RAG Course on Coursera (~20h total)](https://www.coursera.org/learn/retrieval-augmented-generation-rag)
- [Production RAG Guide](https://blog.premai.io/building-production-rag-architecture-chunking-evaluation-monitoring-2026-guide/)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | RAG Course: Module 1 - Intro to RAG, applications, architecture overview, intro to LLMs. | 2.5h | |
| 2 | RAG Course: Module 1 continued - Python setup, LLM calls, intro to information retrieval. | 2.5h | |
| 3 | RAG Course: Module 2 - Retriever architecture, keyword search (BM25). | 2.5h | |
| 4 | RAG Course: Module 2 continued - Semantic search, hybrid search fundamentals. | 2.5h | |
| 5 | RAG Course: Module 3 - ANN algorithms, vector databases. | 2.5h | |
| 6 | RAG Course: Module 3 continued - Chunking strategies, reranking. | 2.5h | |

### Week 5: RAG Course Completion + Chunking Deep Dive
- [Best Chunking Strategies (Firecrawl)](https://www.firecrawl.dev/blog/best-chunking-strategies-rag)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | RAG Course: Module 4 - Transformer architecture review, LLM sampling strategies. | 2.5h | |
| 2 | RAG Course: Module 4 continued - Prompt engineering for RAG. | 2.5h | |
| 3 | RAG Course: Module 5 - RAG evaluation strategies. | 2.5h | |
| 4 | RAG Course: Module 5 continued - Logging, monitoring, observability. Complete assignments. | 2.5h | |
| 5 | Chunking deep dive - Read Firecrawl guide. Implement fixed-size, recursive, semantic chunking. | 2.5h | |
| 6 | Implement hybrid search (dense + sparse with Reciprocal Rank Fusion). Compare to cosine only. | 2.5h | |

### Week 6: RAG Pipeline Build
- [RAGAS Documentation](https://docs.ragas.io)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Add cross-encoder reranking (ms-marco-MiniLM-L-6-v2). Measure precision improvement. | 2.5h | |
| 2 | Build complete RAG pipeline with your own documents. Set up Chroma or Qdrant. | 2.5h | |
| 3 | Add metadata filtering to pipeline. Test with different document types. | 2.5h | |
| 4 | Set up RAGAS evaluation - faithfulness, context relevancy, answer relevancy metrics. | 2.5h | |
| 5 | Create golden test set (50+ QA pairs). Establish baseline RAGAS metrics. | 2.5h | |
| 6 | Experiment with chunking strategies, measure RAGAS score impact. Document best strategy. | 2.5h | |

### Week 7: RAG Evaluation & Production Patterns
- [Langfuse RAG Eval Guide](https://langfuse.com/guides/cookbook/evaluation_of_rag_with_ragas)
- [Building & Evaluating Advanced RAG (1h55m)](https://www.deeplearning.ai/short-courses/building-evaluating-advanced-rag/)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Add Langfuse tracing to pipeline. Track latency, token usage, cost per query. | 2.5h | |
| 2 | DeepLearning.AI "Building & Evaluating Advanced RAG" short course (1h55m) - Watch + code along. | 2.5h | |
| 3 | Implement sentence-window retrieval and auto-merging retrieval from the course. | 2.5h | |
| 4 | Query routing: simple queries skip retrieval, complex queries get full RAG. Error handling. | 2.5h | |
| 5 | Write up RAG system as portfolio piece. Document architecture, eval results, tradeoffs. | 2.5h | |
| 6 | Polish RAG project README with architecture diagrams. Push to GitHub. | 2.5h | |

**Phase 2 Checkpoint:** Production-grade RAG with hybrid search, reranking, RAGAS eval, and Langfuse observability.

---

## Phase 3: LLM Fine-Tuning (Weeks 8-11) ~50h

**Goal:** Fine-tune a model with LoRA/QLoRA, evaluate properly, understand when fine-tuning beats RAG.

### Week 8: Fine-Tuning Theory (freeCodeCamp Course Part 1)
- [freeCodeCamp 12h Fine-Tuning Course](https://www.freecodecamp.org/news/learn-how-to-fine-tune-llms-in-12-hours/)
- [Hugging Face PEFT Docs](https://huggingface.co/docs/peft)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | freeCodeCamp course (12h total): Sections on LLM fundamentals, pretraining concepts. | 2.5h | |
| 2 | freeCodeCamp course: PEFT foundations - Why full fine-tuning is overkill. LoRA math. | 2.5h | |
| 3 | freeCodeCamp course: QLoRA and 4-bit quantization with bitsandbytes. | 2.5h | |
| 4 | freeCodeCamp course: Training setup, hyperparameters, data formatting. | 2.5h | |
| 5 | freeCodeCamp course: Hands-on fine-tuning walkthrough (part 1). | 2.5h | |
| 6 | freeCodeCamp course: Hands-on fine-tuning walkthrough (part 2). | 2.5h | |

### Week 9: Fine-Tuning Practice (freeCodeCamp Course Part 2 + Hands-On)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | freeCodeCamp course: RLHF and DPO concepts. Alignment methods. | 2.5h | |
| 2 | freeCodeCamp course: Advanced topics, evaluation, deployment. Complete remaining sections. | 2.5h | |
| 3 | Dataset preparation - Curate 500-1000 instruction-response pairs for your chosen domain. | 2.5h | |
| 4 | Dataset preparation continued - Format data (Alpaca/ShareGPT/ChatML). Quality review. | 2.5h | |
| 5 | Hands-on: Fine-tune Llama 3 8B with LoRA using trl + Unsloth on Colab/RunPod. | 2.5h | |
| 6 | Debug training run. Monitor loss curves. Adjust if needed. Run to completion. | 2.5h | |

### Week 10: Evaluation & Experimentation

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Evaluate fine-tuned model vs base model on your test set with proper metrics. | 2.5h | |
| 2 | Hyperparameter experiments - Try LoRA ranks (8, 16, 32), different learning rates. | 2.5h | |
| 3 | Try different target modules. Document impact on quality for each config. | 2.5h | |
| 4 | RAG vs fine-tuning: Run same task with your Phase 2 RAG system. Compare quality/latency/cost. | 2.5h | |
| 5 | Model merging - Combine LoRA adapters. Merge adapter back into base model. | 2.5h | |
| 6 | Study HF PEFT docs in depth. Understand adapter types beyond LoRA (IA3, prefix tuning). | 2.5h | |

### Week 11: Deployment & Documentation

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Deploy fine-tuned model with FastAPI endpoint. Test inference latency/throughput. | 2.5h | |
| 2 | Optimize inference - Try vLLM or TGI for faster serving. Benchmark. | 2.5h | |
| 3 | Push model to Hugging Face Hub. Write proper model card with eval results. | 2.5h | |
| 4 | Write up fine-tuning project. Document dataset, training, eval, RAG comparison. | 2.5h | |
| 5 | Polish project README with training curves, comparison charts. Push to GitHub. | 2.5h | |
| 6 | Review & consolidation - Revisit Phase 1-3. Start applying to jobs! | 2.5h | |

**Phase 3 Checkpoint:** Fine-tuned model with measurable improvement, deployed as API, with RAG comparison.

---

## Phase 4: Agent Systems (Weeks 12-14) ~46h

**Goal:** Build multi-step agents with tool use, error handling, and production-grade architecture.

### Week 12: Agent Fundamentals
- [DeepLearning.AI - AI Agents in LangGraph (1h32m)](https://www.deeplearning.ai/short-courses/ai-agents-in-langgraph/)
- [LangGraph Documentation](https://langchain-ai.github.io/langgraph/)
- [Anthropic MCP Documentation](https://modelcontextprotocol.io)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Study ReAct pattern theory. Implement a basic ReAct loop manually (no framework). | 2.5h | |
| 2 | DeepLearning.AI LangGraph course (1h32m) - Watch all lessons + code along. | 2.5h | |
| 3 | LangGraph course exercises. Build your first LangGraph agent from scratch. | 2.5h | |
| 4 | Add tool use: web search, code execution, calculator. Handle tool-call failures/retries. | 2.5h | |
| 5 | Study MCP (Model Context Protocol) docs. Understand architecture and why it matters. | 2.5h | |
| 6 | Build a simple MCP server. Connect it to your LangGraph agent. | 2.5h | |

### Week 13: Advanced Agent Patterns
- [PydanticAI Documentation](https://ai.pydantic.dev)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Multi-step planning agent - Break complex queries into sub-tasks, execute sequentially. | 2.5h | |
| 2 | Add Langfuse observability to agent. Visualize decision points, identify failure modes. | 2.5h | |
| 3 | Study PydanticAI docs. Build the same agent in PydanticAI. Compare DX and reliability. | 2.5h | |
| 4 | Implement guardrails: input validation, output filtering, prompt injection detection. | 2.5h | |
| 5 | Test guardrails with adversarial inputs. Document what gets caught and what doesn't. | 2.5h | |
| 6 | Build multi-agent system: research agent + writing agent with coordination/handoff. | 2.5h | |

### Week 14: Production Agents & Deployment

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Multi-agent continued - Handle coordination edge cases, error propagation. | 2.5h | |
| 2 | Add persistent memory to agent using vector store. Remember context across conversations. | 2.5h | |
| 3 | Deploy agent as production service. Add rate limiting, error handling. | 2.5h | |
| 4 | Add cost tracking per conversation. Monitor token usage patterns. | 2.5h | |
| 5 | Write up agent project. Document architecture, failure modes, solutions. | 2.5h | |
| 6 | Polish agent project README with architecture diagram. Push to GitHub. | 2.5h | |

**Phase 4 Checkpoint:** Deployed multi-tool agent with MCP, observability, and documented failure handling.

---

## Phase 5: LLMOps & Evaluation (Weeks 15-17) ~55h

**Goal:** Master evaluation and monitoring that separate demo builders from production engineers.

### Week 15: Evaluation Frameworks
- [Langfuse Documentation](https://langfuse.com/guides)
- [RAGAS Documentation](https://docs.ragas.io)
- [DeepLearning.AI - Evaluating LLM Apps (1h55m)](https://www.deeplearning.ai/short-courses/building-evaluating-advanced-rag/)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Set up Langfuse self-hosted (Docker). Troubleshoot setup. | 2.5h | |
| 2 | Connect Langfuse to your RAG and agent projects from previous phases. | 2.5h | |
| 3 | Build golden test set of 100 examples for your RAG system. | 2.5h | |
| 4 | Implement automated evaluation with RAGAS metrics on golden test set. | 2.5h | |
| 5 | LLM-as-judge: Set up Langfuse evaluators for hallucination, relevance, toxicity. | 2.5h | |
| 6 | Build cost-per-request dashboard. Track token usage, latency p50/p95/p99, error rates. | 2.5h | |

### Week 16: Advanced Evaluation + MLOps Foundations
- [MLOps Zoomcamp Module 1](https://github.com/DataTalksClub/mlops-zoomcamp)
- [DataCamp Langfuse Tutorial](https://www.datacamp.com/tutorial/langfuse)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | A/B testing for prompts - Run two variants, measure which performs better on eval set. | 2.5h | |
| 2 | DeepLearning.AI eval course - Systematic debugging: retrieval vs prompt vs generation. | 2.5h | |
| 3 | MLOps Zoomcamp Module 1 (part 1) - MLOps lifecycle, how it applies to LLM systems. | 2.5h | |
| 4 | MLOps Zoomcamp Module 1 (part 2) - Environment setup, experiment tracking. | 2.5h | |
| 5 | CI/CD with GitHub Actions - Build workflow that runs eval suite on every push. | 2.5h | |
| 6 | CI/CD continued - Add automated RAGAS scoring, fail build if metrics drop below threshold. | 2.5h | |

### Week 17: Docker, Kubernetes & Production Monitoring
- [freeCodeCamp Docker + K8s Course (4h)](https://www.freecodecamp.org/news/course-on-docker-and-kubernetes/)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Docker fundamentals - Containerize your RAG/agent app. Write Dockerfile, docker-compose. | 2.5h | |
| 2 | freeCodeCamp Docker + K8s course (4h) - Watch first half covering Docker. | 2.5h | |
| 3 | freeCodeCamp Docker + K8s course - Watch K8s sections. Deploy app to Minikube. | 2.5h | |
| 4 | Set up Prometheus + Grafana monitoring. Track request latency, error rates. | 2.5h | |
| 5 | Concept drift detection - How to know when RAG performance degrades over time. | 2.5h | |
| 6 | Consolidation - Wire everything: RAG + agent + Langfuse + monitoring + CI/CD pipeline. | 2.5h | |

**Phase 5 Checkpoint:** Production monitoring, automated evaluation, CI/CD, provable system performance.

---

## Phase 6: Capstone Project (Weeks 18-20) ~50h

**Goal:** Build, deploy, and launch a real AI product demonstrating all skills from Phases 1-5.

### Project Options (Pick One)
- **Option A:** AI-Powered Document Intelligence Platform - Upload docs, get Q&A, summaries, cross-doc analysis
- **Option B:** Domain-Specific AI Assistant - Fine-tuned model + RAG + agents in one domain (legal/medical/finance)
- **Option C:** AI Code Review Agent with MCP - Connect to GitHub, review PRs, identify bugs, suggest improvements

### Week 18: Architecture & Core Build

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Architecture design. System diagram. Define API contracts. | 2.5h | |
| 2 | Set up project structure, CI/CD pipeline, monitoring from day one. | 2.5h | |
| 3 | Core implementation - RAG pipeline or agent logic (part 1). | 2.5h | |
| 4 | Core implementation (part 2). | 2.5h | |
| 5 | Core implementation (part 3) - Integrate fine-tuned model if applicable. | 2.5h | |
| 6 | Core implementation (part 4) - Connect all components end-to-end. | 2.5h | |

### Week 19: Evaluation & Deployment

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Build evaluation harness - Golden test set for your capstone. | 2.5h | |
| 2 | Run RAGAS metrics, Langfuse tracing, cost tracking on capstone. | 2.5h | |
| 3 | Fix issues found during evaluation. Optimize performance. | 2.5h | |
| 4 | Deploy to cloud (GCP/AWS/DigitalOcean). Docker + CI/CD pipeline. | 2.5h | |
| 5 | Set up monitoring dashboard. Verify everything works in production. | 2.5h | |
| 6 | End-to-end testing in production. Fix remaining bugs. | 2.5h | |

### Week 20: Polish & Launch

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Write comprehensive README with architecture diagram, eval metrics. | 2.5h | |
| 2 | Record demo video showing the product in action. | 2.5h | |
| 3 | Write blog post about what you built and learned across 20 weeks. | 2.5h | |
| 4 | Write blog post continued. Create Twitter/X thread version. | 2.5h | |
| 5 | Launch - Share on LinkedIn, Twitter/X, Hacker News, relevant subreddits. | 2.5h | |
| 6 | Update portfolio. Update resume with all projects. Final retrospective. | 2.5h | |

**Phase 6 Checkpoint:** Deployed, launched AI product with documentation, eval metrics, and public visibility.

---

## Daily Progress Log

Each day, commit your work with a log entry in `progress/weekXX/dayX.md`.

Format:
```
## What I Learned
## What I Built / Code Written
## Challenges / Blockers
## Key Takeaways
## Tomorrow's Plan
```

---

## Course Duration Reference

Actual researched durations of every resource in this plan:

| Resource | Type | Duration |
|----------|------|----------|
| Karpathy: Micrograd | Video + code-along | ~2h 30m watch, ~5h with coding |
| Karpathy: Makemore pt1 | Video + code-along | 1h 57m watch, ~4h with coding |
| Karpathy: Makemore pt2 MLP | Video + code-along | 1h 15m watch, ~3h with coding |
| Karpathy: Makemore pt3 BatchNorm | Video + code-along | 1h 55m watch, ~4h with coding |
| Karpathy: Makemore pt4 Backprop | Video + code-along | 56m watch, ~2h with coding |
| Karpathy: WaveNet | Video + code-along | 56m watch, ~2h with coding |
| Karpathy: Let's Build GPT | Video + code-along | 1h 56m watch, ~4h with coding |
| Karpathy: GPT Tokenizer | Video + code-along | 2h 13m watch, ~4h with coding |
| 3Blue1Brown: Attention Explained | Video | ~25m |
| DeepLearning.AI RAG (Coursera) | Full course | ~20h (5h video + 15h exercises) |
| DeepLearning.AI: Advanced RAG | Short course | 1h 55m video + ~3h hands-on |
| DeepLearning.AI: LangGraph Agents | Short course | 1h 32m video + ~3h hands-on |
| freeCodeCamp: Fine-Tune LLMs | Video course | 12h video + hands-on practice |
| Activeloop LLM Course | Self-paced | ~40h (optional supplementary) |
| MLOps Zoomcamp (Module 1 only) | Video + homework | ~10-15h |
| freeCodeCamp: Docker + K8s | Video course | ~4h video + hands-on |
| RAGAS setup + eval | Hands-on | ~4h |
| Langfuse self-hosted setup | Hands-on | ~3-4h |

---

## Job Readiness Checklist

- [ ] Can explain transformer architecture and self-attention from first principles
- [ ] Can design a RAG system for 1M+ documents with chunking/retrieval/reranking tradeoffs
- [ ] Can fine-tune with LoRA and explain when fine-tuning beats RAG (and vice versa)
- [ ] Can debug prompt failures (retrieval vs prompt vs model vs context issue)
- [ ] Can explain MCP and build multi-tool agents with error handling
- [ ] 3+ GitHub repos with clear READMEs, architecture diagrams, and eval metrics
- [ ] At least 1 deployed project that real users can try
- [ ] Blog post or Twitter thread documenting learning journey

---

## Resources

| Category | Resource | Link |
|----------|----------|------|
| Math Foundations | 3Blue1Brown - Essence of Linear Algebra | https://youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab |
| Math Foundations | 3Blue1Brown - Essence of Calculus | https://youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr |
| Math Foundations | Khan Academy - Matrices | https://www.khanacademy.org/math/precalculus/x9e81a4f98389efdf:matrices |
| Transformers | Karpathy - Zero to Hero | https://karpathy.ai/zero-to-hero.html |
| Transformers | 3Blue1Brown - Neural Networks | https://youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi |
| Transformers | Attention Is All You Need | https://arxiv.org/abs/1706.03762 |
| Transformers | Hugging Face NLP Course | https://huggingface.co/learn/nlp-course |
| RAG | DeepLearning.AI RAG Course | https://www.coursera.org/learn/retrieval-augmented-generation-rag |
| RAG | RAGAS Documentation | https://docs.ragas.io |
| RAG | Firecrawl Chunking Guide | https://www.firecrawl.dev/blog/best-chunking-strategies-rag |
| RAG | Production RAG Guide | https://blog.premai.io/building-production-rag-architecture-chunking-evaluation-monitoring-2026-guide/ |
| Fine-Tuning | freeCodeCamp 12h Course | https://www.freecodecamp.org/news/learn-how-to-fine-tune-llms-in-12-hours/ |
| Fine-Tuning | Hugging Face PEFT Docs | https://huggingface.co/docs/peft |
| Fine-Tuning | Unsloth (2x faster) | https://github.com/unslothai/unsloth |
| Fine-Tuning | Activeloop LLM Course (optional) | https://learn.activeloop.ai/courses/llms |
| Agents | DeepLearning.AI LangGraph | https://www.deeplearning.ai/short-courses/ai-agents-in-langgraph/ |
| Agents | LangGraph Docs | https://langchain-ai.github.io/langgraph/ |
| Agents | MCP Documentation | https://modelcontextprotocol.io |
| Agents | PydanticAI Docs | https://ai.pydantic.dev |
| LLMOps | Langfuse | https://langfuse.com |
| LLMOps | Langfuse RAG Eval Guide | https://langfuse.com/guides/cookbook/evaluation_of_rag_with_ragas |
| LLMOps | MLOps Zoomcamp | https://github.com/DataTalksClub/mlops-zoomcamp |
| LLMOps | freeCodeCamp Docker + K8s | https://www.freecodecamp.org/news/course-on-docker-and-kubernetes/ |
| Roadmap | roadmap.sh/ai-engineer | https://roadmap.sh/ai-engineer |
