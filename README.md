# AI Engineer 12-Week Learning Plan

**12-Week Roadmap | 2 Hours/Day | 6 Days/Week | 144 Total Hours**

Based on real 2026 job postings from LinkedIn, Indeed, EY, and ZipRecruiter.

## Progress Overview

| Week | Phase | Focus | Status |
|------|-------|-------|--------|
| 1-2 | Transformer Internals | Attention, architecture, Karpathy course | Not Started |
| 3-4 | Production RAG | Chunking, hybrid search, reranking, eval | Not Started |
| 5-6 | LLM Fine-Tuning | LoRA, QLoRA, dataset curation, evaluation | Not Started |
| 7-8 | Agent Systems | ReAct, LangGraph, MCP, tool use | Not Started |
| 9-10 | LLMOps & Evaluation | Langfuse, RAGAS, testing, monitoring | Not Started |
| 11-12 | Capstone Project | Build, deploy, launch a production AI product | Not Started |

---

## Phase 1: Transformer Internals & PyTorch (Weeks 1-2)

**Goal:** Understand what happens inside LLMs so you can debug, optimize, and discuss them in interviews.

### Week 1: Neural Networks from Scratch
- [Karpathy - Zero to Hero](https://karpathy.ai/zero-to-hero.html)
- [GitHub Repo](https://github.com/karpathy/nn-zero-to-hero)

| Day | Task | Done |
|-----|------|------|
| 1 | Lecture 1 (micrograd) - Build autograd engine from scratch | |
| 2 | Lecture 2 (makemore pt1) - Bigram language model, torch.Tensor basics | |
| 3 | Lecture 3 (makemore pt2) - MLP character-level model, training basics | |
| 4 | Lecture 4 (makemore pt3) - Activations, gradients, Batch Normalization | |
| 5 | Lecture 5 (makemore pt4) - Manual backprop without autograd | |
| 6 | Lecture 6 (WaveNet) - Deeper network, torch.nn internals | |

### Week 2: Transformers & GPT
- [Karpathy - Let's Build GPT](https://youtube.com/watch?v=kCc8FmEb1nY)
- [3Blue1Brown - Attention Explained](https://youtube.com/watch?v=eMlx5fFNoYc)

| Day | Task | Done |
|-----|------|------|
| 1 | Let's Build GPT (first half) - Self-attention, key/query/value | |
| 2 | Let's Build GPT (second half) - Complete implementation, train mini-GPT | |
| 3 | 3Blue1Brown attention video + "Attention Is All You Need" paper (sections 3.1-3.3) | |
| 4 | Tokenization - Karpathy's tokenizer video, BPE | |
| 5 | Hugging Face Transformers docs - Run inference with pre-trained model | |
| 6 | Consolidation - Rewrite attention from memory, draw transformer architecture | |

**Checkpoint:** Can explain attention, build a mini-GPT, and run HF models with PyTorch.

---

## Phase 2: Production RAG (Weeks 3-4)

**Goal:** Go from "I can build RAG" to "I can build RAG that works reliably at scale with proper evaluation."

### Week 3: Advanced RAG Architecture
- [DeepLearning.AI RAG Course](https://www.coursera.org/learn/retrieval-augmented-generation-rag)
- [Production RAG Guide](https://blog.premai.io/building-production-rag-architecture-chunking-evaluation-monitoring-2026-guide/)
- [Best Chunking Strategies](https://www.firecrawl.dev/blog/best-chunking-strategies-rag)

| Day | Task | Done |
|-----|------|------|
| 1 | RAG course Module 1-2 - Retrieval fundamentals, vector DBs, BM25 vs semantic search | |
| 2 | Chunking strategies deep dive - fixed-size, recursive, semantic chunking | |
| 3 | Hybrid search (dense + sparse with RRF) | |
| 4 | Cross-encoder reranking - ms-marco-MiniLM-L-6-v2 | |
| 5 | RAG course Module 3-4 - Query decomposition, agentic RAG | |
| 6 | Build complete RAG pipeline with Chroma/Qdrant + metadata filtering | |

### Week 4: RAG Evaluation & Production Patterns
- [RAGAS Documentation](https://docs.ragas.io)
- [Langfuse RAG Eval Guide](https://langfuse.com/guides/cookbook/evaluation_of_rag_with_ragas)

| Day | Task | Done |
|-----|------|------|
| 1 | Set up RAGAS evaluation - faithfulness, context relevancy, answer relevancy | |
| 2 | Create golden test set (50+ QA pairs), establish baseline metrics | |
| 3 | Experiment with chunking strategies, measure RAGAS impact | |
| 4 | Add Langfuse tracing - latency, token usage, cost per query | |
| 5 | Query routing + error handling for retrieval failures | |
| 6 | Write up RAG system as portfolio piece, push to GitHub | |

**Checkpoint:** Production-grade RAG with hybrid search, reranking, RAGAS eval, and Langfuse observability.

---

## Phase 3: LLM Fine-Tuning (Weeks 5-6)

**Goal:** Fine-tune a model with LoRA/QLoRA, evaluate properly, understand when fine-tuning beats RAG.

### Week 5: Fine-Tuning Fundamentals
- [freeCodeCamp 12h Fine-Tuning Course](https://www.freecodecamp.org/news/learn-how-to-fine-tune-llms-in-12-hours/)
- [Activeloop LLM Course](https://learn.activeloop.ai/courses/llms)
- [Hugging Face PEFT Docs](https://huggingface.co/docs/peft)

| Day | Task | Done |
|-----|------|------|
| 1 | PEFT foundations - Why full fine-tuning is overkill, LoRA math | |
| 2 | QLoRA and 4-bit quantization with bitsandbytes | |
| 3 | Dataset prep - Curate 500-1000 instruction-response pairs (Alpaca/ShareGPT/ChatML) | |
| 4 | Fine-tune Llama 3 8B with LoRA using trl + Unsloth | |
| 5 | Evaluate fine-tuned model - base vs fine-tuned comparison with metrics | |
| 6 | RLHF and DPO concepts - when to use DPO over SFT | |

### Week 6: Advanced Fine-Tuning & RAG vs Fine-Tuning

| Day | Task | Done |
|-----|------|------|
| 1 | Hyperparameter experiments - LoRA ranks (8,16,32), learning rates, target modules | |
| 2 | RAG vs fine-tuning comparison - quality, latency, cost | |
| 3 | Model merging - combine LoRA adapters, merge into base model | |
| 4 | Deploy fine-tuned model with FastAPI endpoint | |
| 5 | Push model to Hugging Face Hub with model card | |
| 6 | Write up fine-tuning project with eval results, push to GitHub | |

**Checkpoint:** Fine-tuned model with measurable improvement, deployed as API, with RAG comparison.

---

## Phase 4: Agent Systems (Weeks 7-8)

**Goal:** Build multi-step agents with tool use, error handling, and production-grade architecture.

### Week 7: Agent Fundamentals
- [DeepLearning.AI - AI Agents in LangGraph](https://www.deeplearning.ai/short-courses/ai-agents-in-langgraph/)
- [LangGraph Documentation](https://langchain-ai.github.io/langgraph/)
- [Anthropic MCP Documentation](https://modelcontextprotocol.io)

| Day | Task | Done |
|-----|------|------|
| 1 | ReAct pattern - Implement basic ReAct loop manually (no framework) | |
| 2 | LangGraph course - State machines for agents, first LangGraph agent | |
| 3 | Tool use - web search, code execution, calculator + failure handling | |
| 4 | MCP (Model Context Protocol) - Build simple MCP server, connect to agent | |
| 5 | Multi-step planning - Break complex queries into sub-tasks | |
| 6 | Add Langfuse observability to agent, visualize decision points | |

### Week 8: Production Agent Patterns

| Day | Task | Done |
|-----|------|------|
| 1 | PydanticAI vs LangGraph - Build same agent in both, compare | |
| 2 | Guardrails - input validation, output filtering, prompt injection detection | |
| 3 | Multi-agent system - research agent + writing agent with coordination | |
| 4 | Persistent memory with vector store across conversations | |
| 5 | Deploy agent as production service with rate limiting, error handling, cost tracking | |
| 6 | Write up agent project, document failure modes, push to GitHub | |

**Checkpoint:** Deployed multi-tool agent with MCP, observability, and documented failure handling.

---

## Phase 5: LLMOps & Evaluation (Weeks 9-10)

**Goal:** Master evaluation and monitoring that separate demo builders from production engineers.

### Week 9: Evaluation Frameworks
- [Langfuse Documentation](https://langfuse.com/guides)
- [RAGAS Documentation](https://docs.ragas.io)
- [DeepLearning.AI - Evaluating LLM Apps](https://www.deeplearning.ai/short-courses/building-evaluating-advanced-rag/)

| Day | Task | Done |
|-----|------|------|
| 1 | Langfuse self-hosted (Docker) - Connect to RAG and agent projects | |
| 2 | Golden test set (100 examples) + automated RAGAS evaluation | |
| 3 | LLM-as-judge - Langfuse evaluators for hallucination, relevance, toxicity | |
| 4 | Cost-per-request dashboard - token usage, latency p50/p95/p99, error rates | |
| 5 | A/B testing for prompts - two variants, measure performance | |
| 6 | DeepLearning.AI eval course - Systematic debugging (retrieval vs prompt vs generation) | |

### Week 10: Production Monitoring & Kubernetes
- [MLOps Zoomcamp](https://github.com/DataTalksClub/mlops-zoomcamp)
- [Kubernetes for AI/ML](https://www.freecodecamp.org/news/kubernetes-for-beginners/)

| Day | Task | Done |
|-----|------|------|
| 1 | MLOps Zoomcamp Module 1 - MLOps lifecycle for LLM systems | |
| 2 | Kubernetes basics - Deploy containerized LLM app to K8s | |
| 3 | Prometheus + Grafana monitoring - GPU utilization, latency, error rates | |
| 4 | CI/CD with GitHub Actions - Eval suite on every push | |
| 5 | Concept drift detection for RAG systems | |
| 6 | Consolidation - Wire everything: RAG + agent + Langfuse + monitoring + CI/CD | |

**Checkpoint:** Production monitoring, automated evaluation, CI/CD, provable system performance.

---

## Phase 6: Capstone Project (Weeks 11-12)

**Goal:** Build, deploy, and launch a real AI product demonstrating all skills from Phases 1-5.

### Project Options (Pick One)
- **Option A:** AI-Powered Document Intelligence Platform
- **Option B:** Domain-Specific AI Assistant with Fine-Tuned Model
- **Option C:** AI Code Review Agent with MCP

### Week 11: Build

| Day | Task | Done |
|-----|------|------|
| 1-2 | Architecture design, system diagram, project setup, CI/CD, monitoring | |
| 3-4 | Core implementation - RAG pipeline, agent logic, or fine-tuned model | |
| 5-6 | Evaluation harness - Golden test set, RAGAS, Langfuse, cost tracking | |

### Week 12: Deploy & Launch

| Day | Task | Done |
|-----|------|------|
| 1-2 | Deploy to cloud (GCP/AWS/DigitalOcean), Docker + CI/CD, monitoring dashboard | |
| 3-4 | Polish - README, demo video, blog post | |
| 5-6 | Launch - LinkedIn, Twitter/X, Hacker News, subreddits, portfolio | |

**Checkpoint:** Deployed, launched AI product with documentation, eval metrics, and public visibility.

---

## Daily Progress Log

Each day, commit your work with a log entry in `progress/weekXX/dayX.md`.

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
| Transformers | Karpathy - Zero to Hero | https://karpathy.ai/zero-to-hero.html |
| Transformers | 3Blue1Brown - Neural Networks | https://youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi |
| Transformers | Attention Is All You Need | https://arxiv.org/abs/1706.03762 |
| Transformers | Hugging Face NLP Course | https://huggingface.co/learn/nlp-course |
| RAG | DeepLearning.AI RAG Course | https://www.coursera.org/learn/retrieval-augmented-generation-rag |
| RAG | RAGAS Documentation | https://docs.ragas.io |
| Fine-Tuning | freeCodeCamp 12h Course | https://www.freecodecamp.org/news/learn-how-to-fine-tune-llms-in-12-hours/ |
| Fine-Tuning | Hugging Face PEFT Docs | https://huggingface.co/docs/peft |
| Fine-Tuning | Unsloth (2x faster) | https://github.com/unslothai/unsloth |
| Agents | DeepLearning.AI LangGraph | https://www.deeplearning.ai/short-courses/ai-agents-in-langgraph/ |
| Agents | MCP Documentation | https://modelcontextprotocol.io |
| Agents | PydanticAI Docs | https://ai.pydantic.dev |
| LLMOps | Langfuse | https://langfuse.com |
| LLMOps | MLOps Zoomcamp | https://github.com/DataTalksClub/mlops-zoomcamp |
| Roadmap | roadmap.sh/ai-engineer | https://roadmap.sh/ai-engineer |
