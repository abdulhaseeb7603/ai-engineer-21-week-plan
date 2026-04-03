# AI Engineer 25-Week Learning Plan

**25-Week Roadmap | 2.5 Hours/Day | 6 Days/Week | ~405 Total Hours**

Based on real 2026 job postings from LinkedIn, Indeed, EY, and ZipRecruiter.
Timeline adjusted from original 12-week plan after researching actual course durations.
Includes 2 math foundations weeks for beginners with no linear algebra/calculus background.

## Progress Overview

| Weeks | Phase | Focus | Hours | Status |
|-------|-------|-------|-------|--------|
| 0A-0B | Math Foundations | Linear algebra, calculus, Python/NumPy basics | ~30h | Not Started |
| 1-4 | Transformer Internals | Attention, architecture, Karpathy course | ~55h | Not Started |
| 5-9 | Production RAG | Chunking, hybrid search, reranking, eval | ~65h | Not Started |
| 10-13 | LLM Fine-Tuning | LoRA, QLoRA, dataset curation, evaluation | ~55h | Not Started |
| 14-17 | Agent Systems | ReAct, LangGraph, MCP, tool use | ~55h | Not Started |
| 18-21 | LLMOps & Evaluation | Langfuse, RAGAS, testing, monitoring, K8s | ~55h | Not Started |
| 22-25 | Capstone Project | Build, deploy, launch a production AI product | ~55h | Not Started |

> **Start applying for jobs at Week 15** (after RAG + Fine-Tuning). Don't wait until Week 25.

---

## Phase 0: Math & Python Foundations (Weeks 0A-0B) ~30h

**Goal:** Build just enough math intuition to follow Karpathy's lectures without constantly Googling. This is NOT a full math course -- it's targeted prep for the specific concepts you'll encounter in Weeks 1-3.

### Week 0A: Linear Algebra for Deep Learning
- [3Blue1Brown - Essence of Linear Algebra (2h 34m total, 16 videos)](https://youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab)
- [Khan Academy - Matrices](https://www.khanacademy.org/math/precalculus/x9e81a4f98389efdf:matrices)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | 3B1B Linear Algebra Ch 1-3: Vectors, linear combinations, spans, linear transformations. Watch, pause, rewatch confusing parts. Take notes. | 2.5h | |
| 2 | 3B1B Linear Algebra Ch 4-6: Matrix multiplication as composition, 3D transformations, determinants. | 2.5h | |
| 3 | 3B1B Linear Algebra Ch 7-9: Inverse matrices, column/null space, nonsquare matrices, dot products. | 2.5h | |
| 4 | 3B1B Linear Algebra Ch 10-13: Cross products, Cramer's rule, change of basis. | 2.5h | |
| 5 | 3B1B Linear Algebra Ch 14-16: Eigenvectors, eigenvalues, abstract vector spaces. | 2.5h | |
| 6 | Khan Academy matrix practice: multiply matrices by hand (2x2, 3x3). Practice until it feels natural. | 2.5h | |

### Week 0B: Calculus + Python/NumPy for Deep Learning
- [3Blue1Brown - Essence of Calculus (3h total, 12 videos)](https://youtube.com/playlist?list=PLZHQObOWTQDMsr9K-rj53DwVRMYO3t5Yr)
- [Python NumPy Tutorial (freeCodeCamp)](https://www.youtube.com/watch?v=QUT1VHiLmmI)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | 3B1B Calculus Ch 1-3: The essence of calculus, paradox of the derivative, derivative formulas through geometry. | 2.5h | |
| 2 | 3B1B Calculus Ch 4-6: Visualizing the chain rule, product rule, derivatives of exponentials. The chain rule is THE most important part -- this is backpropagation. | 2.5h | |
| 3 | 3B1B Calculus Ch 7-9: Limits, integration, higher-order derivatives. | 2.5h | |
| 4 | 3B1B Calculus Ch 10-12: Taylor series, what they don't teach in calculus. Rewatch chain rule (Ch 4) if needed. | 2.5h | |
| 5 | Python NumPy crash course: arrays, matrix ops, broadcasting, reshaping, indexing, random. | 2.5h | |
| 6 | Practice day: multiply matrices in NumPy, compute a derivative by hand, implement a simple gradient descent in 10 lines of Python. | 2.5h | |

**What you need to remember for Karpathy's course:**
- **Vectors & matrices**: What they are, how to multiply them (this is ALL of neural networks)
- **Dot product**: How two vectors combine to produce a single number (this is attention)
- **Derivatives & chain rule**: How small changes propagate (this is backpropagation)
- **Softmax**: Turning numbers into probabilities (watch for this in Week 3)

> Don't stress about mastering everything. The goal is *recognition* -- when Karpathy says "we take the dot product of Q and K", you should think "oh, that's multiplying two vectors" rather than being lost.

**Phase 0 Checkpoint:** Can multiply matrices by hand, explain what a derivative measures, and use NumPy for basic array operations.

---

## Phase 1: Transformer Internals & PyTorch (Weeks 1-4) ~55h

**Goal:** Understand what happens inside LLMs so you can debug, optimize, and discuss them in interviews.

### Week 1: Micrograd + Makemore pt1
- [Karpathy - Zero to Hero](https://karpathy.ai/zero-to-hero.html)
- [GitHub Repo](https://github.com/karpathy/nn-zero-to-hero)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Micrograd (2h30m video) - Watch first half, pause and take notes. Don't code yet. | 2.5h | |
| 2 | Micrograd - Watch second half. Understand full backprop flow. | 2.5h | |
| 3 | Micrograd - Now code along from scratch. Build autograd engine yourself. | 2.5h | |
| 4 | Makemore pt1 (1h57m video) - Watch full lecture. Understand bigram model and torch.Tensor. | 2.5h | |
| 5 | Makemore pt1 - Code along. Implement bigram language model from scratch. | 2.5h | |
| 6 | Makemore pt1 - Experiment with the model. Try different parameters. Understand train/dev splits. | 2.5h | |

### Week 2: Makemore pt2-4 (MLP, BatchNorm, Backprop)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Makemore pt2 MLP (1h15m) - Watch and code along. Shorter lecture, fits in one session. | 2.5h | |
| 2 | Makemore pt2 MLP - Finish implementation. Experiment with learning rate, splits. | 2.5h | |
| 3 | Makemore pt3 (1h55m) - Watch first half. Activations, gradients. | 2.5h | |
| 4 | Makemore pt3 - Watch second half. Batch Normalization. Code along. | 2.5h | |
| 5 | Makemore pt4 (56m) - Manual backprop. Watch the video. This is the HARDEST lecture. | 2.5h | |
| 6 | Makemore pt4 - Actually do the manual backprop exercises. Take your time. Rewatch parts. | 2.5h | |

### Week 3: WaveNet, GPT, Attention
- [Karpathy - Let's Build GPT (1h56m)](https://youtube.com/watch?v=kCc8FmEb1nY)
- [3Blue1Brown - Attention Explained (~25m)](https://youtube.com/watch?v=eMlx5fFNoYc)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | WaveNet (56m) - Watch and code along. Deeper network with tree structure. | 2.5h | |
| 2 | Review day - Re-implement micrograd from memory. Complete Karpathy suggested exercises. | 2.5h | |
| 3 | Let's Build GPT (1h56m) - Watch first half. Self-attention, key/query/value. | 2.5h | |
| 4 | Let's Build GPT - Watch second half. Code along. Train your mini-GPT. | 2.5h | |
| 5 | Let's Build GPT - Finish implementation. Experiment with hyperparameters. Get it training. | 2.5h | |
| 6 | 3Blue1Brown attention video (25m) + spend remaining time reading "Attention Is All You Need" paper sections 3.1-3.3 slowly. | 2.5h | |

### Week 4: Tokenization, HF Transformers, Consolidation
- [Karpathy - GPT Tokenizer (2h13m)](https://youtube.com/watch?v=zduSFxRajkE)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | "Attention Is All You Need" paper - Continue reading. Draw diagrams. Understand architecture. | 2.5h | |
| 2 | GPT Tokenizer (2h13m) - Watch first half. Understand BPE, why tokenization matters. | 2.5h | |
| 3 | GPT Tokenizer - Watch second half. Code along with the implementation. | 2.5h | |
| 4 | Hugging Face Transformers docs - Install, run inference with a pre-trained model. Explore the API. | 2.5h | |
| 5 | Hugging Face continued - Try different models, understand tokenizers, pipeline API. | 2.5h | |
| 6 | Final consolidation - Rewrite attention mechanism from memory. Draw the full transformer architecture on paper and explain every component. | 2.5h | |

**Phase 1 Checkpoint:** Can explain attention, build a mini-GPT, and run HF models with PyTorch.

---

## Phase 2: Production RAG (Weeks 5-9) ~65h

**Goal:** Go from "I can build RAG" to "I can build RAG that works reliably at scale with proper evaluation."

### Week 5: RAG Course Part 1 (Coursera)
- [DeepLearning.AI RAG Course on Coursera (~20h total)](https://www.coursera.org/learn/retrieval-augmented-generation-rag)
- [Production RAG Guide](https://blog.premai.io/building-production-rag-architecture-chunking-evaluation-monitoring-2026-guide/)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | RAG Course: Module 1 - Intro to RAG, applications, architecture overview. | 2.5h | |
| 2 | RAG Course: Module 1 continued - Python setup, LLM calls, information retrieval basics. | 2.5h | |
| 3 | RAG Course: Module 2 - Retriever architecture, keyword search (BM25). | 2.5h | |
| 4 | RAG Course: Module 2 continued - Semantic search, hybrid search fundamentals. | 2.5h | |
| 5 | RAG Course: Module 2 exercises - Complete coding assignments. Don't rush these. | 2.5h | |
| 6 | RAG Course: Module 3 - ANN algorithms, vector databases. | 2.5h | |

### Week 6: RAG Course Part 2 + Chunking
- [Best Chunking Strategies (Firecrawl)](https://www.firecrawl.dev/blog/best-chunking-strategies-rag)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | RAG Course: Module 3 continued - Chunking strategies, reranking. | 2.5h | |
| 2 | RAG Course: Module 4 - Transformer architecture review, LLM sampling strategies. | 2.5h | |
| 3 | RAG Course: Module 4 continued - Prompt engineering for RAG. Complete exercises. | 2.5h | |
| 4 | RAG Course: Module 5 - RAG evaluation strategies, logging, monitoring. | 2.5h | |
| 5 | RAG Course: Module 5 continued - Complete all remaining assignments and quizzes. | 2.5h | |
| 6 | Chunking deep dive - Read Firecrawl guide. Implement fixed-size chunking on a real doc set. | 2.5h | |

### Week 7: RAG Pipeline Build
- [RAGAS Documentation](https://docs.ragas.io)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Implement recursive chunking. Compare to fixed-size on your documents. | 2.5h | |
| 2 | Implement semantic chunking. Compare all three strategies side by side. | 2.5h | |
| 3 | Implement hybrid search (dense + sparse with Reciprocal Rank Fusion). | 2.5h | |
| 4 | Add cross-encoder reranking (ms-marco-MiniLM-L-6-v2). Measure precision improvement. | 2.5h | |
| 5 | Set up Chroma or Qdrant vector database. Get it running locally. | 2.5h | |
| 6 | Build your RAG pipeline - connect chunking + vector DB + retrieval + LLM generation. | 2.5h | |

### Week 8: RAG Evaluation
- [RAGAS Documentation](https://docs.ragas.io)
- [Langfuse Cloud (free tier)](https://langfuse.com)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Add metadata filtering to pipeline. Test with different document types. | 2.5h | |
| 2 | Set up RAGAS evaluation. Install, configure, understand the metrics. | 2.5h | |
| 3 | Create golden test set - write 15-20 high-quality QA pairs (quality over quantity). | 2.5h | |
| 4 | Create more test pairs - expand to 30+ pairs. Run first RAGAS evaluation. | 2.5h | |
| 5 | Experiment with different chunking strategies and measure RAGAS score impact. | 2.5h | |
| 6 | Sign up for Langfuse Cloud (free tier). Add basic tracing to your pipeline. | 2.5h | |

### Week 9: RAG Production Patterns + Portfolio
- [Langfuse RAG Eval Guide](https://langfuse.com/guides/cookbook/evaluation_of_rag_with_ragas)
- [Building & Evaluating Advanced RAG (1h55m)](https://www.deeplearning.ai/short-courses/building-evaluating-advanced-rag/)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Langfuse tracing deep dive - Track latency, token usage, cost per query. | 2.5h | |
| 2 | DLAI "Building & Evaluating Advanced RAG" (1h55m) - Watch the course. Take notes. | 2.5h | |
| 3 | DLAI course - Code along. Implement sentence-window retrieval. | 2.5h | |
| 4 | Implement auto-merging retrieval. Compare retrieval strategies with RAGAS. | 2.5h | |
| 5 | Query routing: simple queries skip retrieval, complex queries get full RAG. Add error handling. | 2.5h | |
| 6 | Write up RAG system as portfolio piece. Document architecture, eval results, tradeoffs. Push to GitHub. | 2.5h | |

**Phase 2 Checkpoint:** Production-grade RAG with hybrid search, reranking, RAGAS eval, and Langfuse tracing.

---

## Phase 3: LLM Fine-Tuning (Weeks 10-13) ~55h

**Goal:** Fine-tune a model with LoRA/QLoRA, evaluate properly, understand when fine-tuning beats RAG.

### Week 10: Fine-Tuning Theory (freeCodeCamp Part 1)
- [freeCodeCamp 12h Fine-Tuning Course](https://www.freecodecamp.org/news/learn-how-to-fine-tune-llms-in-12-hours/)
- [Hugging Face PEFT Docs](https://huggingface.co/docs/peft)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | freeCodeCamp (12h total): LLM fundamentals and pretraining concepts. Watch ~2h, take notes. | 2.5h | |
| 2 | freeCodeCamp: PEFT foundations. Why full fine-tuning is overkill. LoRA math (low-rank decomposition). | 2.5h | |
| 3 | freeCodeCamp: QLoRA and 4-bit quantization with bitsandbytes. How QLoRA enables training on consumer GPU. | 2.5h | |
| 4 | freeCodeCamp: Training setup, hyperparameters, data formatting concepts. | 2.5h | |
| 5 | freeCodeCamp: Hands-on fine-tuning walkthrough (part 1). Watch and take notes. | 2.5h | |
| 6 | freeCodeCamp: Hands-on fine-tuning walkthrough (part 2). Continue watching. | 2.5h | |

### Week 11: Fine-Tuning Theory (Part 2) + Environment Setup

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | freeCodeCamp: RLHF and DPO concepts. Alignment methods. When to use DPO over SFT. | 2.5h | |
| 2 | freeCodeCamp: Advanced topics, evaluation, deployment. Complete remaining video sections. | 2.5h | |
| 3 | freeCodeCamp: Review - rewatch any confusing parts. Read HF PEFT docs alongside. | 2.5h | |
| 4 | Environment setup day - Set up Google Colab Pro or RunPod. Install trl, Unsloth, bitsandbytes. Test that GPU training works with a tiny model. Debug CUDA/dependency issues. | 2.5h | |
| 5 | Dataset preparation - Browse existing datasets on HF Hub. Find a domain-specific dataset to adapt. Understand Alpaca/ShareGPT/ChatML formats. | 2.5h | |
| 6 | Dataset preparation - Filter and format 200-500 instruction-response pairs from existing data. Add 50-100 custom pairs for your domain. | 2.5h | |

### Week 12: Hands-On Fine-Tuning + Evaluation

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Fine-tune Llama 3 8B with LoRA using trl + Unsloth. Follow a tutorial step by step. | 2.5h | |
| 2 | Monitor training - Watch loss curves, debug if needed. Let training complete. | 2.5h | |
| 3 | Evaluate fine-tuned model vs base model on your test set with proper metrics. | 2.5h | |
| 4 | Hyperparameter experiments - Try LoRA rank 8 vs 16 vs 32. Document impact. | 2.5h | |
| 5 | Try different learning rates and target modules. Document what works best. | 2.5h | |
| 6 | RAG vs fine-tuning: Run the same task with your Phase 2 RAG. Compare quality, latency, cost. | 2.5h | |

### Week 13: Deployment + Documentation

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Model merging - Merge LoRA adapter back into base model. Understand the process. | 2.5h | |
| 2 | Deploy fine-tuned model with a simple FastAPI endpoint. Get basic inference working. | 2.5h | |
| 3 | Test inference latency and throughput. Try basic optimizations. | 2.5h | |
| 4 | Push model to Hugging Face Hub. Write a proper model card with eval results. | 2.5h | |
| 5 | Write up fine-tuning project. Document dataset, training process, eval results, RAG comparison. | 2.5h | |
| 6 | Polish project README with training curves and charts. Push to GitHub. START APPLYING TO JOBS! | 2.5h | |

**Phase 3 Checkpoint:** Fine-tuned model with measurable improvement, deployed as API, with RAG comparison.

---

## Phase 4: Agent Systems (Weeks 14-17) ~55h

**Goal:** Build multi-step agents with tool use, error handling, and production-grade architecture.

### Week 14: Agent Fundamentals
- [DeepLearning.AI - AI Agents in LangGraph (1h32m)](https://www.deeplearning.ai/short-courses/ai-agents-in-langgraph/)
- [LangGraph Documentation](https://langchain-ai.github.io/langgraph/)
- [Anthropic MCP Documentation](https://modelcontextprotocol.io)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Study the ReAct pattern. Read about it. Understand plan-act-observe cycle. | 2.5h | |
| 2 | Implement a basic ReAct loop manually in Python (no framework). Get it working with a simple task. | 2.5h | |
| 3 | DLAI LangGraph course (1h32m) - Watch all lessons. Take notes on state machine concepts. | 2.5h | |
| 4 | DLAI LangGraph course - Code along with the exercises. Build your first LangGraph agent. | 2.5h | |
| 5 | Extend your LangGraph agent - add tool use: web search API, calculator. | 2.5h | |
| 6 | Handle tool-call failures and retries. Test edge cases. What happens when tools fail? | 2.5h | |

### Week 15: MCP + Observability
- [Anthropic MCP Documentation](https://modelcontextprotocol.io)
- [Langfuse Documentation](https://langfuse.com)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Study MCP (Model Context Protocol) documentation. Understand the architecture and protocol. | 2.5h | |
| 2 | Study MCP continued - Look at example servers. Understand transport, tool definitions. | 2.5h | |
| 3 | Build a simple MCP server from scratch (e.g., a file reader or database query tool). | 2.5h | |
| 4 | Connect your MCP server to your LangGraph agent. Debug the integration. | 2.5h | |
| 5 | Multi-step planning - Build an agent that breaks complex queries into sub-tasks. | 2.5h | |
| 6 | Add Langfuse observability to your agent. Visualize decision points and trace failures. | 2.5h | |

### Week 16: Advanced Agent Patterns
- [PydanticAI Documentation](https://ai.pydantic.dev)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Study PydanticAI documentation. Understand how it differs from LangGraph. | 2.5h | |
| 2 | Build a simple agent in PydanticAI. Compare the developer experience. | 2.5h | |
| 3 | Implement guardrails: input validation and output filtering. | 2.5h | |
| 4 | Implement prompt injection detection. Test with adversarial inputs. | 2.5h | |
| 5 | Build multi-agent system (part 1): Design the architecture. Research agent that gathers info. | 2.5h | |
| 6 | Build multi-agent system (part 2): Writing agent that uses research agent output. | 2.5h | |

### Week 17: Multi-Agent + Production Deployment

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Multi-agent system (part 3): Handle coordination, error propagation, retries between agents. | 2.5h | |
| 2 | Test multi-agent system end-to-end. Fix edge cases. | 2.5h | |
| 3 | Add persistent memory to your agent using a vector store. Context across conversations. | 2.5h | |
| 4 | Deploy agent as a production service. Add rate limiting and error handling. | 2.5h | |
| 5 | Add cost tracking per conversation. Monitor token usage patterns. | 2.5h | |
| 6 | Write up agent project. Document architecture, failure modes, solutions. Push to GitHub. | 2.5h | |

**Phase 4 Checkpoint:** Deployed multi-tool agent with MCP, observability, and documented failure handling.

---

## Phase 5: LLMOps & Evaluation (Weeks 18-21) ~55h

**Goal:** Master evaluation and monitoring that separate demo builders from production engineers.

### Week 18: Evaluation Deep Dive
- [Langfuse Documentation](https://langfuse.com/guides)
- [RAGAS Documentation](https://docs.ragas.io)
- [DeepLearning.AI - Evaluating LLM Apps (1h55m)](https://www.deeplearning.ai/short-courses/building-evaluating-advanced-rag/)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Set up Langfuse self-hosted with Docker Compose. Follow their guide step by step. | 2.5h | |
| 2 | Langfuse setup continued - Troubleshoot issues. Connect to your RAG project. | 2.5h | |
| 3 | Build golden test set of 100 examples for your RAG system (expand from Phase 2 set). | 2.5h | |
| 4 | Implement automated evaluation pipeline with RAGAS metrics. | 2.5h | |
| 5 | LLM-as-judge: Set up Langfuse evaluators for hallucination, relevance, toxicity. | 2.5h | |
| 6 | Build cost-per-request dashboard. Track token usage, latency p50/p95/p99, error rates. | 2.5h | |

### Week 19: Prompt Testing + CI/CD
- [MLOps Zoomcamp Module 1](https://github.com/DataTalksClub/mlops-zoomcamp)
- [DataCamp Langfuse Tutorial](https://www.datacamp.com/tutorial/langfuse)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | A/B testing for prompts - Set up two prompt variants, measure which performs better. | 2.5h | |
| 2 | DLAI "Building & Evaluating Advanced RAG" eval sections - Systematic debugging: is the failure in retrieval, prompt, or generation? | 2.5h | |
| 3 | MLOps Zoomcamp Module 1 - Watch videos on MLOps lifecycle. Understand how it applies to LLMs. | 2.5h | |
| 4 | MLOps Zoomcamp Module 1 continued - Focus on experiment tracking concepts. | 2.5h | |
| 5 | CI/CD with GitHub Actions - Write a workflow that runs your eval suite on every push. | 2.5h | |
| 6 | CI/CD continued - Add automated RAGAS scoring. Fail the build if metrics drop below threshold. | 2.5h | |

### Week 20: Docker + Containerization
- [freeCodeCamp Docker + K8s Course (4h)](https://www.freecodecamp.org/news/course-on-docker-and-kubernetes/)

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | freeCodeCamp Docker + K8s course - Watch Docker fundamentals section (~2h). | 2.5h | |
| 2 | Docker hands-on - Write a Dockerfile for your RAG/agent app. Get it building. | 2.5h | |
| 3 | Docker Compose - Write docker-compose.yml for your app + its dependencies (DB, Langfuse, etc.). | 2.5h | |
| 4 | freeCodeCamp Docker + K8s course - Watch Kubernetes introduction sections. | 2.5h | |
| 5 | Kubernetes hands-on - Install Minikube. Get it running. Deploy a simple container. | 2.5h | |
| 6 | Kubernetes continued - Deploy YOUR containerized app to Minikube. Troubleshoot. | 2.5h | |

### Week 21: Monitoring + Integration

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Set up Prometheus for your deployed app. Understand metrics, scraping, targets. | 2.5h | |
| 2 | Set up Grafana. Connect to Prometheus. Build your first dashboard. | 2.5h | |
| 3 | Build monitoring dashboards - request latency, error rates, token usage. | 2.5h | |
| 4 | Concept drift detection - Research approaches. How to know when RAG degrades. | 2.5h | |
| 5 | Integration day - Wire everything: your app + Langfuse + Prometheus + Grafana + CI/CD. | 2.5h | |
| 6 | Integration continued - Test the full pipeline end-to-end. Fix issues. Document. | 2.5h | |

**Phase 5 Checkpoint:** Production monitoring, automated evaluation, CI/CD, provable system performance.

---

## Phase 6: Capstone Project (Weeks 22-25) ~55h

**Goal:** Build, deploy, and launch a real AI product demonstrating all skills from Phases 1-5.

### Project Options (Pick One)
- **Option A:** AI-Powered Document Intelligence Platform - Upload docs, get Q&A, summaries, cross-doc analysis
- **Option B:** Domain-Specific AI Assistant - Fine-tuned model + RAG + agents in one domain (legal/medical/finance)
- **Option C:** AI Code Review Agent with MCP - Connect to GitHub, review PRs, identify bugs, suggest improvements

### Week 22: Architecture + Core Build

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Architecture design. System diagram. Define API contracts. Choose your project. | 2.5h | |
| 2 | Set up project structure, Git repo, basic CI/CD from day one. | 2.5h | |
| 3 | Core implementation (part 1) - Set up the base (FastAPI, database, config). | 2.5h | |
| 4 | Core implementation (part 2) - RAG pipeline or agent logic. | 2.5h | |
| 5 | Core implementation (part 3) - Continue building core features. | 2.5h | |
| 6 | Core implementation (part 4) - Integrate components. Get basic end-to-end working. | 2.5h | |

### Week 23: Core Build + Evaluation

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Core implementation (part 5) - Add fine-tuned model integration if applicable. | 2.5h | |
| 2 | Core implementation (part 6) - Polish, error handling, edge cases. | 2.5h | |
| 3 | Build evaluation harness - Golden test set for your capstone. | 2.5h | |
| 4 | Run RAGAS metrics, Langfuse tracing, cost tracking on your capstone. | 2.5h | |
| 5 | Fix issues found during evaluation. Optimize performance. | 2.5h | |
| 6 | More fixes and optimization. Get metrics to an acceptable level. | 2.5h | |

### Week 24: Deployment

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Containerize your app with Docker. Test locally. | 2.5h | |
| 2 | Set up cloud account (GCP/AWS/DigitalOcean). Learn the console/CLI basics. | 2.5h | |
| 3 | Deploy to cloud - Push your container. Get the app running remotely. | 2.5h | |
| 4 | Set up CI/CD pipeline for your cloud deployment. | 2.5h | |
| 5 | Set up monitoring dashboard in production. Verify everything works. | 2.5h | |
| 6 | End-to-end testing in production. Fix remaining bugs. | 2.5h | |

### Week 25: Polish + Launch

| Day | Task | Hours | Done |
|-----|------|-------|------|
| 1 | Write comprehensive README with architecture diagram and eval metrics. | 2.5h | |
| 2 | Record demo video showing the product in action. | 2.5h | |
| 3 | Write blog post about what you built and learned across 25 weeks. | 2.5h | |
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
| 3Blue1Brown: Linear Algebra | Video | 2h 34m |
| 3Blue1Brown: Calculus | Video | 3h |
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
