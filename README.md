<h1 align="center">Hi, I'm Hamsika 👋</h1>

<p align="center">
  <b>AI/ML Engineer</b> — Building RAG systems, LLM agents, and production-ready AI tools
</p>

<p align="center">
  <a href="https://linkedin.com/in/hamsikarg"><img src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn"></a>
  <a href="mailto:hamsikaraog@gmail.com"><img src="https://img.shields.io/badge/Email-hamsikaraog@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white" alt="Email"></a>
  <img src="https://img.shields.io/badge/New%20York-📍-333333?style=flat-square" alt="New York">
</p>

---

### About

I'm an AI/ML engineer finishing my M.S. in Artificial Intelligence at the University at Buffalo. Most of my work sits at the point where language models meet real systems — taking a promising demo and turning it into something with access control, cost budgets, and evaluation you can actually trust.

I like the unglamorous parts: figuring out *why* one model is 18× slower than another, catching a retrieval pipeline that hallucinates on out-of-scope questions, or proving an agent's output is correct before it ships. Before focusing on AI, I built backend microservices and data pipelines, so I tend to think about models and the infrastructure around them together.

Right now I'm a Data Engineer at Saayam for All, working on multi-provider LLM routing and evaluation.

---

### What I work on

- **RAG systems** — retrieval pipelines with access control, multi-backend vector search, and evaluation harnesses that measure faithfulness and catch hallucinations instead of eyeballing outputs.
- **LLM agents** — multi-agent orchestration with LangGraph, self-correcting review loops, and per-task model routing to keep cost and latency in check.
- **Applied ML** — reinforcement learning, computer vision, and classical modeling, usually taken all the way to a deployed, measurable result.
- **Production engineering** — FastAPI backends, Docker, cloud (GCP / AWS / Azure), and the profiling and monitoring that keep the above honest.

---

### Tech I use

**Languages** — Python · SQL · TypeScript · JavaScript

**GenAI & LLMs** — RAG · Hybrid Search · Embeddings · LangChain · LangGraph · Multi-Agent Orchestration · LLM Agents & Tool Calling · ReAct · MCP · Prompt Engineering · Fine-Tuning (PEFT / LoRA / QLoRA)

**LLM APIs & Evaluation** — Anthropic · OpenAI · Gemini · Groq · Hugging Face · RAGAS · LLM-as-Judge · Hallucination Detection

**ML & Deep Learning** — PyTorch · TensorFlow · Transformers · scikit-learn · XGBoost · CNNs / LSTM · DQN / DDQN · Reward Design

**Retrieval & Vector DBs** — FAISS · Qdrant · ChromaDB · Weaviate · Sentence Transformers

**Cloud & MLOps** — AWS (SageMaker, Lambda, S3, EC2) · GCP (Vertex AI, BigQuery) · Azure (Databricks, Data Factory) · Weights & Biases · Docker · Kubernetes

**Data Engineering** — Apache Airflow · PySpark · Databricks · Snowflake · Kafka · BigQuery

**Backend & Web** — FastAPI · Spring Boot · React · Node.js · Streamlit · REST · SSE · JWT

**Databases** — PostgreSQL · MongoDB · MySQL · Redis · SQLite

---

### Featured Projects

**🤖 [Multi-Agent Coding Assistant](https://github.com/HamsikaRaj/multi-agent-coding-assistant)** &nbsp;·&nbsp; `LangGraph` `FastAPI` `React` `Claude`
A 5-agent pipeline (Planner → Architect → Coder → two Reviewers) that turns a single prompt into a multi-file codebase — it shipped a 25-file React/TypeScript app in one run, with a self-correcting review loop that retries up to 3× to repair broken output before it ships. I routed models per task (Opus for generation, Sonnet for planning/review, a Haiku intent classifier out front) so a full dual-reviewer cycle costs ~$0.0007, and streamed per-agent tokens/latency/cost over SSE to find the real bottleneck.

**📊 [RAG Evaluation Harness](https://github.com/HamsikaRaj/rag-eval-harness)** &nbsp;·&nbsp; `FastAPI` `FAISS` `Claude` `Pytest`
An automated harness that uses Claude as an LLM-judge to replace manual RAG scoring, cutting evaluation effort ~90%. On a 75-question benchmark it measured faithfulness 0.996, hallucination rate 0.017, and Recall@5 0.87 / Recall@10 0.92. The retrieval layer is pluggable across FAISS, ChromaDB, Qdrant, and Weaviate, so benchmarking a new backend is a one-config change.

**🔐 [FinSolve — RAG with Role-Based Access Control](https://github.com/HamsikaRaj/FinSolve-RBAC-RAG)** &nbsp;·&nbsp; `FastAPI` `Qdrant` `Claude` `JWT`
A RAG chatbot where access is enforced at the vector-search layer: dual-layer RBAC across 6 role tiers and 5 department knowledge bases, reaching 100% access-control accuracy and 0 hallucinations across 16 adversarial test cases. Roles are derived dynamically from a 100-person HR dataset via JWT, and I replaced a local Llama 3.2 model that hallucinated on every out-of-scope query with Claude Sonnet, taking fabricated responses to zero.

**📈 [RL for Derivatives Markets](https://github.com/HamsikaRaj/rl-options-trading)** &nbsp;·&nbsp; `PyTorch` `OpenAI Gym` `DDQN`
A custom Gym environment with a 5-dimensional state space and a reward function I designed and debugged (an early version reward-hacked before I diagnosed and fixed it). A DDQN agent with prioritized experience replay took reward from near-zero to a 600+ moving average over 900 episodes, reaching 15% ROI with zero major drawdowns on NVDA call-option data.

**⚽ [VARLite — Real-Time Offside Detection](https://github.com/HamsikaRaj/VARLite)** &nbsp;·&nbsp; `YOLOv8n` `OpenCV` `NumPy`
Offside detection from single-camera football footage at >20 FPS and 95% detection accuracy on consumer GPUs, using YOLOv8n with SVD-based vanishing-point perspective correction. Multi-threaded video pipelines with geometric reconstruction and HSV team classification improved offside-call precision by 32%.

**🌊 [Ripple — AI Policy Simulator](https://github.com/HamsikaRaj/Ripple)** &nbsp;·&nbsp; `React` `Gemini` `Monte Carlo`
A deployed web app that pairs Monte Carlo simulation with Gemini to explore the downstream effects of policy changes — minimum wage, taxes, housing subsidies — across a synthetic population, before any of it happens in the real world.

---

### How I think about engineering

- **Measure before you optimize.** Most of my wins came from profiling first — finding the 18× latency gap or the ~8.7s coder step — then fixing the thing that actually mattered.
- **Evaluation is the feature.** For anything LLM-shaped, I build the way to score it before I trust it. A number I can defend beats a demo that looks good once.
- **Correctness and access come first.** RBAC, grounding checks, and adversarial tests aren't polish — they're what makes an AI system safe to put in front of real users.
- **Ship the whole thing.** A model isn't done until it's behind an API, in a container, and telling me how it's doing in production.

---

### Contact

📍 New York &nbsp;·&nbsp; 📧 [hamsikaraog@gmail.com](mailto:hamsikaraog@gmail.com) &nbsp;·&nbsp; 💼 [LinkedIn](https://linkedin.com/in/hamsikarg)

<p align="center"><i>Open to AI/ML Engineer, Applied AI, and Software Engineer (AI) roles.</i></p>
