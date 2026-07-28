# AI/ML Engineer Roadmap — Aug 1, 2026 → Dec 31, 2026

> This plan *does* deliver: real coding ability, a working portfolio of deployed projects, and strong conceptual command of architecture/GenAI/MLOps so you can credibly interview for **AI/ML Engineer, GenAI Engineer, ML Engineer (Junior/Associate), or Applied AI Engineer** roles.

---

## How this roadmap is structured

- **5 months = ~22 weeks**, ~4–5 hrs/day on weekdays, ~6–8 hrs on weekends (adjust to your capacity — consistency matters more than hours).
- Every month ends with a **shippable project** — not just notes.

---

## MONTH 1 (Aug 1 – Aug 31): Foundations — CS, Python, Git, Software Engineering

**Goal:** Write real Python confidently. Understand how software is actually built, not just scripted.

### Week 1 — Computer Science Fundamentals + Dev Environment
- How computers work: CPU, RAM, storage, OS basics (processes, threads, memory management — conceptual, not OS engineering depth)
- Number systems (binary/hex), how data is represented (int, float, char encoding, ASCII/UTF-8)
- Networking basics: client-server model, HTTP/HTTPS, REST, DNS, ports, APIs (you'll need this constantly later)
- Big-O notation: time/space complexity — O(1), O(n), O(log n), O(n²) with real examples
- Set up: VS Code, Python 3.12+, virtual environments (`venv`), pip, Git, GitHub CLI
- Terminal/CLI fluency (navigation, permissions, piping, basic bash scripting)

### Week 2 — Python Core
- Variables, data types, operators, control flow (if/elif/else, loops, comprehensions)
- Data structures: lists, tuples, dicts, sets — when to use which, and their Big-O behavior
- Functions: args/kwargs, default params, scope, closures, decorators, lambda
- String manipulation, regex basics
- File I/O (text, CSV, JSON), exception handling (try/except/finally, custom exceptions)

### Week 3 — Python: OOP + Intermediate
- Classes, objects, inheritance, polymorphism, encapsulation, abstract classes
- Magic/dunder methods (`__init__`, `__str__`, `__repr__`, `__eq__`)
- Iterators, generators, `yield`
- Modules & packages, `__init__.py`, project structuring
- Working with external libraries: `pip`, `requirements.txt`, virtual envs discipline

### Week 4 — Git/GitHub + Software Engineering Practices
- Git: init, add, commit, branch, merge, rebase, stash, `.gitignore`, resolving conflicts
- GitHub: PRs, issues, forking, GitHub Actions (basic CI), commit message conventions
- Clean code principles, SOLID (conceptual level), DRY/KISS/YAGNI
- Basic design patterns you'll actually meet: Singleton, Factory, Strategy
- Unit testing with `pytest` (this is non-negotiable — most non-coders skip it and it shows in interviews)
- Logging (not `print()` — use the `logging` module)

**Project 1 (end of month):** A CLI tool (e.g., expense tracker or file organizer) — properly packaged, tested with pytest, version-controlled with clean commit history, README with usage docs.

---

## MONTH 2 (Sep 1 – Sep 30): Data + Statistics + Classical ML

**Goal:** Be able to take raw data → clean it → analyze it → build and evaluate a model.

### Week 5 — NumPy + Pandas
- NumPy: arrays, vectorization, broadcasting, indexing/slicing, linear algebra ops
- Pandas: Series/DataFrame, indexing (`loc`/`iloc`), filtering, groupby, merge/join, pivot tables
- Data cleaning: missing values, duplicates, outliers, dtype conversion
- Data visualization: Matplotlib, Seaborn (distribution plots, correlation heatmaps, boxplots)

### Week 6 — SQL + Databases
- SQL: SELECT, WHERE, JOINs (inner/left/right/full), GROUP BY, HAVING, subqueries, CTEs, window functions
- Indexing and query performance basics (EXPLAIN plans — conceptual)
- Relational (PostgreSQL) vs NoSQL (MongoDB) — when to use which
- Intro to Redis (caching, key-value store) — you'll need this for GenAI apps later

### Week 7 — Statistics & Probability
- Descriptive statistics: mean/median/mode, variance, std dev, skewness
- Probability: conditional probability, Bayes' theorem, distributions (normal, binomial, Poisson)
- Inferential statistics: sampling, confidence intervals, hypothesis testing, p-values, t-tests, chi-square
- Correlation vs causation, A/B testing fundamentals

### Week 8 — Machine Learning Fundamentals
- Supervised learning: linear/logistic regression, decision trees, random forests, gradient boosting (XGBoost/LightGBM), SVM, KNN
- Unsupervised learning: k-means, hierarchical clustering, PCA, dimensionality reduction
- Feature engineering, feature scaling, encoding categorical variables
- Model evaluation: train/test split, cross-validation, confusion matrix, precision/recall/F1, ROC-AUC, RMSE/MAE
- Overfitting/underfitting, bias-variance tradeoff, regularization (L1/L2)
- Hyperparameter tuning (GridSearch, RandomSearch, Optuna basics)
- scikit-learn end-to-end pipeline

**Project 2 (end of month):** A full ML pipeline on a real (messy) dataset — data cleaning → EDA → feature engineering → model training → evaluation → saved model artifact. Push to GitHub with a proper README and notebook + `.py` scripts (not just a notebook).

---

## MONTH 3 (Oct 1 – Oct 31): Deep Learning + NLP + Start Deployment

**Goal:** Understand neural networks deeply enough to reason about them, and be comfortable with transformer-based models.

### Week 9 — Deep Learning Foundations
- Perceptron, activation functions (ReLU, sigmoid, softmax, tanh)
- Forward/backward propagation, gradient descent, loss functions
- PyTorch basics: tensors, autograd, `nn.Module`, training loops, optimizers (SGD, Adam)
- Regularization for DL: dropout, batch normalization, early stopping

### Week 10 — CNNs and RNNs
- CNNs: convolution, pooling, image classification (build one on MNIST/CIFAR)
- RNNs, LSTMs, GRUs — sequence modeling, vanishing gradient problem
- Transfer learning (fine-tuning pretrained models)

### Week 11 — Transformers + NLP
- Tokenization (BPE, WordPiece), word embeddings (Word2Vec, GloVe conceptually)
- Attention mechanism, self-attention, the Transformer architecture (this is the single most important concept for your GenAI goal — don't rush it)
- BERT vs GPT-style architectures (encoder vs decoder vs encoder-decoder)
- Hugging Face `transformers`: pipelines, tokenizers, fine-tuning a pretrained model for classification/NER

### Week 12 — Deployment Basics Begin (parallel-track from here on)
- FastAPI: routing, Pydantic models, request/response validation, async endpoints, dependency injection
- Wrap your Month 2 ML model as a FastAPI service (`/predict` endpoint)
- Docker: Dockerfile basics, building/running containers, docker-compose
- Deploy the containerized API to a free-tier cloud service (Render/Railway/AWS EC2 free tier)

**Project 3 (end of month):** An image or text classifier (DL) deployed as a Dockerized FastAPI service with a live URL. This is your first "production" project — treat the deployment seriously.

---

## MONTH 4 (Nov 1 – Nov 30): Generative AI — this is your specialization

**Goal:** Be able to design and build production RAG systems and LLM-powered applications, not just call an API.

### Week 13 — LLM Fundamentals + Prompt Engineering
- How LLMs actually work at inference (autoregressive generation, temperature, top-k/top-p, context windows)
- Prompt engineering: zero-shot, few-shot, chain-of-thought, system/user/assistant roles, prompt templates
- Structured outputs (JSON mode, function calling/tool use)
- LLM APIs: Anthropic API and OpenAI API — messages, streaming, tool use, cost/token management

### Week 14 — Embeddings + Vector Databases
- What embeddings are, cosine similarity, semantic search
- Vector databases: Pinecone, Weaviate, Chroma, or pgvector (pick one, understand the concept transfers)
- Chunking strategies for documents (fixed-size, semantic, recursive)

### Week 15 — RAG (Retrieval-Augmented Generation)
- Full RAG architecture: ingestion → chunking → embedding → retrieval → reranking → generation
- Frameworks: LangChain and/or LlamaIndex (learn the concepts, not just the library API — libraries change, architecture doesn't)
- Hybrid search (keyword + semantic), reranking models
- Evaluation of RAG systems: faithfulness, relevance, hallucination detection (RAGAS or similar)

### Week 16 — Agents, Fine-tuning, and LLM Ops
- Agentic patterns: ReAct, tool-calling agents, multi-step planning, MCP (Model Context Protocol) conceptually
- When to fine-tune vs RAG vs prompt engineering (decision framework — this is an architect-level thinking skill, start building it now)
- Fine-tuning basics: LoRA/QLoRA conceptually, when it's worth the cost
- Guardrails: input/output validation, prompt injection risks, PII handling, rate limiting
- LLM observability: logging prompts/responses, tracing (LangSmith or similar), cost monitoring

**Project 4 (end of month):** A production RAG application — e.g., "chat with your documents" — with a FastAPI backend, vector DB, proper chunking/retrieval, a simple frontend (Streamlit or a basic React page), deployed live, with basic evaluation metrics reported in the README.

---

## MONTH 5 (Dec 1 – Dec 31): System Design + Capstone + Interview Readiness

**Goal:** Be able to design ML/GenAI systems on a whiteboard, ship a capstone that proves it, and pass interviews.

### Week 17 — System Design Fundamentals
- Scalability basics: horizontal vs vertical scaling, load balancing, caching (Redis), CDNs
- Databases at scale: sharding, replication, read/write patterns
- Message queues (Kafka/RabbitMQ conceptually), async processing
- API design: REST best practices, rate limiting, versioning, auth (OAuth2/JWT)

### Week 18 — ML/GenAI System Design (the interview differentiator)
- Designing an ML system end-to-end: data pipeline → training → serving → monitoring → retraining (MLOps loop)
- Designing a RAG system for scale: caching embeddings, batching, latency/cost tradeoffs
- Practice framework: clarify requirements → high-level design → deep dive → scale/tradeoffs (practice 5-6 mock prompts: "design a recommendation system," "design a chatbot for customer support," etc.)
- MLflow or Weights & Biases for experiment tracking (mention/use in your capstone)

### Week 19-20 — Capstone Project
Pick ONE that shows the full stack of what you learned (e.g., "Enterprise document Q&A assistant" or "AI-powered support ticket triage system"):
- Data ingestion pipeline
- Model/LLM component with RAG or fine-tuning
- FastAPI backend, Dockerized, deployed
- Database (SQL + vector DB)
- Basic frontend
- Tests, CI/CD (GitHub Actions), logging/monitoring, documented architecture diagram
- This is the project you'll talk about in every interview — build it like it's going into production, because that's exactly what interviewers are checking for.

### Week 21 — Portfolio + Resume + LinkedIn
- GitHub profile README, pin your 4-5 best projects, clean commit history everywhere
- Resume: quantify impact, use the projects as evidence, no fluff
- LinkedIn: headline, summary, project posts (recruiters do check activity)
- Personal portfolio site (optional but strong signal) — deploy the Month 3 FastAPI skills here too

### Week 22 — Interview Preparation
- DSA practice: arrays, strings, hashmaps, two-pointers, sliding window, basic trees/graphs (target: 40-60 easy/medium problems on LeetCode/NeetCode — not competitive programming depth, just fluency)
- ML theory Q&A drills (bias-variance, regularization, evaluation metrics, common algorithm tradeoffs)
- GenAI/LLM interview questions (RAG vs fine-tuning, hallucination mitigation, prompt injection defense, embedding choices)
- System design mock interviews (record yourself, or practice with a peer)
- Behavioral prep (STAR method, "tell me about a project" — rehearse your capstone story)

---

## Updated Repository Structure

Your existing structure is a good skeleton. Here's the fix for gaps and ordering (numbers indicate learning sequence, not necessarily final folder numbers — keep your existing numbering scheme and just add the missing folders):

```
00_ADMIN/
01_COMPUTER_SCIENCE/
02_GIT/
03_PYTHON/
04_SOFTWARE_ENGINEERING/
05_NUMPY/
06_PANDAS/
07_SQL/
08_STATISTICS/
09_MACHINE_LEARNING/
10_DEEP_LEARNING/
11_NLP/
12_GENAI/
    ├── prompt_engineering/
    ├── embeddings_vector_db/
    ├── rag/
    ├── agents/
    ├── fine_tuning/
    └── llm_ops_guardrails/         <-- ADD: was missing
13_FASTAPI/
14_DATABASES/
    ├── sql/
    ├── nosql/
    └── vector_db/                   <-- ADD: was missing
15_FRONTEND/
16_DEVOPS/
    ├── docker/                      <-- ADD explicit subfolder
    ├── ci_cd/
    └── cloud_deployment/            <-- ADD: AWS/GCP/Render/Railway
17_SYSTEM_DESIGN/
    ├── general_system_design/
    └── ml_genai_system_design/       <-- ADD: was missing, and it's the highest-leverage folder for interviews
18_PROJECTS/
19_PORTFOLIO/
20_CAPSTONE/
21_INTERVIEW/
    ├── dsa/                          <-- ADD explicit folder
    ├── ml_theory/
    ├── genai_theory/
    └── system_design_mocks/
22_RESOURCES/
90_DEVELOPMENT/
91_TEMPLATES/
```

## Weekly Discipline (non-negotiable)
- Every week: 1 concept summary note (in your own words, not copy-pasted) + working code, committed to GitHub.
- Every month: 1 shippable, deployed project — no exceptions, even if imperfect.
- Never spend more than 2 days stuck on a single concept without moving forward and circling back — momentum matters more than perfection at this stage.
