<!-- ═════════════════════════  HEADER  ═════════════════════════ -->
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=240&color=0:0f0c29,50:302b63,100:24c6dc&text=Bartu%20%C3%96nder&fontColor=ffffff&fontSize=64&fontAlignY=36&desc=AI%20Researcher%20in%20the%20making%20%C2%B7%20AI%2FML%20Engineer%20by%20craft&descSize=20&descAlignY=58&animation=fadeIn" alt="Bartu Önder banner" width="100%"/>

<a href="https://github.com/bartuonder">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3200&pause=900&color=24C6DC&center=true&vCenter=true&width=760&lines=%F0%9F%A7%A0+Deep+Learning+%C2%B7+PyTorch+%C2%B7+Transformers;%F0%9F%93%84+Implementing+papers+from+scratch;%F0%9F%A4%96+RAG+%C2%B7+Agentic+AI+%C2%B7+LangGraph;%F0%9F%94%AC+Agents+that+test+ML+claims+with+statistics;%E2%9A%99%EF%B8%8F+Training+%E2%86%92+Serving+%E2%86%92+Monitoring+(MLOps);%F0%9F%8E%93+Aiming+for+a+PhD+in+AI+in+the+USA" alt="Typing animation"/>
</a>

<br/>

<a href="https://www.linkedin.com/in/bartuonder/"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/></a>
<a href="https://huggingface.co/Bartu0nder"><img src="https://img.shields.io/badge/Hugging%20Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face"/></a>
<a href="https://www.kaggle.com/bartuonder"><img src="https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=kaggle&logoColor=white" alt="Kaggle"/></a>
<a href="mailto:onderbartu8@gmail.com"><img src="https://img.shields.io/badge/Email-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Email"/></a>

<br/><br/>

<img src="https://img.shields.io/badge/📍_Istanbul,_Türkiye-302b63?style=flat-square" alt="Location"/>
<img src="https://img.shields.io/badge/🎓_Altınbaş_University-SWE_%C2%B7_3rd_year-24c6dc?style=flat-square" alt="University"/>
<img src="https://img.shields.io/badge/GPA-3.78_/_4.00-success?style=flat-square" alt="GPA"/>
<img src="https://img.shields.io/badge/🏅_Full_Scholarship-gold?style=flat-square" alt="Scholarship"/>

</div>

---

## 👋 About me

I'm a **3rd-year Software Engineering student** (full scholarship, GPA 3.78/4.00) who is fascinated by **every corner of AI**. My long-term goal is to become an **AI researcher / scientist**: to do a **PhD in AI in the USA** and help shape where the field goes next.

I care about both halves of the job:

- 🔬 **The science:** ML/DL theory, the math underneath, reading papers and re-implementing them until I really understand them.
- 🛠️ **The engineering:** training models, serving them, tracking and deploying them, and turning them into real products.

> *"If I can't build it from scratch, I don't understand it yet."* 🧩

```python
class BartuOnder:
    role      = "AI/ML Engineer  →  AI Researcher"
    focus     = ["Deep Learning (PyTorch)", "LLMs & Transformers", "RAG & Agentic AI", "MLOps"]
    building  = "end-to-end, scalable, AI-powered SaaS products"
    next_step = "PhD in AI 🇺🇸"

    def philosophy(self):
        return "Read the paper. Implement it. Break it. Ship it."
```

---

## ⭐ Flagship Project: [AxiomForge](https://github.com/bartuonder/AxiomForge)

> **Replicate machine-learning claims with statistics, not with a language model.** 🔬

An autonomous **AI research agent** that reads a claim (or an arXiv link), tests it on many real datasets inside a sandbox, and lets **Python, not the LLM, decide the verdict**. The research agent then proposes its own follow-up hypotheses and tests them on datasets it has never seen.

<div align="center">
  <a href="https://github.com/bartuonder/AxiomForge">
    <img src="https://raw.githubusercontent.com/bartuonder/AxiomForge/main/docs/media/axiomforge-demo.gif" alt="AxiomForge demo: summary, evidence ledger, research agent session and live progress" width="760"/>
  </a>
  <br/>
  <sub>70-second walkthrough recorded from the real console.</sub>
</div>

<br/>

**💡 The idea:** LLM agents write fluent conclusions but are unreliable judges of evidence. AxiomForge splits the work: the model plans experiments and writes prose, while a deterministic statistics layer computes every verdict and ties every number to an **evidence ledger**.

| 🧪 Question | 📊 Measured result |
|---|---|
| Does it get known claims right? | **10 / 10** established comparisons judged as expected, on 9 real datasets |
| Does it invent differences? | Decisive verdict in only **2.1 %** of simulated worlds with no true effect; **0 / 45** real-model comparisons significant when the only difference was the random seed |
| Does the research agent inflate discoveries? | Family-wise error **3 %**, versus **24 %** for an agent that selects and tests on the same data and 89 % for uncorrected testing |
| A real research session | 6 models × 16 datasets: **16 hypotheses registered → 15 confirmed, 0 reversed, 1 not confirmed**. The "winner's curse" overestimated the lead of tree ensembles ~3× on the exploration data, so only confirmation datasets are reported |

**🔑 What makes it interesting**

- 🔒 **Sealed confirmation data:** the hypothesis generator never sees the confirmation datasets. Hypotheses are frozen with a **SHA-256 digest** *before* testing, and `python -m app.research verify` detects tampering.
- 📐 **Real statistics:** Wilcoxon signed-rank, Friedman, Holm and Benjamini-Hochberg corrections, with the dataset (not the split) as the unit of replication.
- 🚧 **LLM output is policed:** the paper text is composed from ledger values and checked by **17 deterministic rules** that reject overclaims.
- 📏 **Honest limits:** conservative, low power under 1 ROC-AUC point, and the real session *reproduces* a known finding (Grinsztajn et al., NeurIPS 2022) rather than claiming a new one.

<p>
  <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square"/>
  <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/>
  <img src="https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white"/>
  <img src="https://img.shields.io/badge/PostgreSQL-pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
  <img src="https://img.shields.io/badge/E2B_Sandbox-FF8800?style=flat-square"/>
  <img src="https://img.shields.io/badge/SciPy-8CAAE6?style=flat-square&logo=scipy&logoColor=white"/>
  <img src="https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white"/>
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white"/>
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
  <img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=white"/>
</p>

<p>
  <a href="https://github.com/bartuonder/AxiomForge"><img src="https://img.shields.io/badge/⭐_Repository-24c6dc?style=for-the-badge" alt="Repository"/></a>
  <a href="https://github.com/bartuonder/AxiomForge/blob/main/TECHNICAL_REPORT.md"><img src="https://img.shields.io/badge/📄_Technical_Report-302b63?style=for-the-badge" alt="Technical report"/></a>
  <a href="https://github.com/bartuonder/AxiomForge/blob/main/demo/README.md"><img src="https://img.shields.io/badge/▶️_Try_the_demo_(no_API_key)-0f0c29?style=for-the-badge" alt="Demo"/></a>
</p>

---

## 🧭 What I work on

> Click a section to expand 👇

<details open>
<summary><b>🔬 &nbsp;Research &amp; Theory</b></summary>
<br/>

Reading papers, deriving things by hand, and re-implementing architectures from scratch to see how they really work.

<p>
  <img src="https://img.shields.io/badge/Transformers-8A2BE2?style=flat-square"/>
  <img src="https://img.shields.io/badge/Attention-6A5ACD?style=flat-square"/>
  <img src="https://img.shields.io/badge/Backpropagation-FF6F61?style=flat-square"/>
  <img src="https://img.shields.io/badge/Optimization-E67E22?style=flat-square"/>
  <img src="https://img.shields.io/badge/Linear_Algebra_%26_Calculus-2E86C1?style=flat-square"/>
  <img src="https://img.shields.io/badge/Probability_%26_Statistics-17A589?style=flat-square"/>
  <img src="https://img.shields.io/badge/Paper_Implementation-F1C40F?style=flat-square&labelColor=555"/>
  <img src="https://img.shields.io/badge/Language_Modeling-C0392B?style=flat-square"/>
  <img src="https://img.shields.io/badge/Hypothesis_Testing-1ABC9C?style=flat-square"/>
  <img src="https://img.shields.io/badge/Multiple_Testing_Correction-8E44AD?style=flat-square"/>
  <img src="https://img.shields.io/badge/Reproducibility-34495E?style=flat-square"/>
</p>

See [🧪 Research &amp; From-Scratch Implementations](#-research--from-scratch-implementations) below.

</details>

<details open>
<summary><b>🧠 &nbsp;AI / ML / GenAI</b></summary>
<br/>

| Area | Topics & tools |
|---|---|
| **Deep Learning** | PyTorch, CNNs, Vision Transformers (ViT), MobileNet, DeBERTa, transfer learning, mixed-precision training |
| **NLP & LLMs** | Hugging Face Transformers, fine-tuning, semantic search & embeddings, structured outputs |
| **Computer Vision** | OpenCV, image classification, object detection (YOLO), face recognition & emotion analysis |
| **GenAI / RAG** | RAG pipelines, vector databases (Chroma, Qdrant), chunking & retrieval evaluation (Hit@k, MRR) |
| **Agentic AI** | Tool calling, ReAct loops, planning, memory, reflection, **LangChain / LangGraph** (human-in-the-loop interrupts, checkpoints), autonomous research agents, LLM output guardrails |
| **Evaluation & statistics** | Wilcoxon, Friedman, Holm / Benjamini-Hochberg corrections, false-positive calibration, power simulations, experiment reproducibility |
| **Data science** | NumPy, SciPy, Pandas, Matplotlib, Seaborn, scikit-learn, XGBoost / LightGBM / CatBoost |

<p>
  <img src="https://skillicons.dev/icons?i=python,pytorch,opencv,numpy,pandas,sklearn&perline=6" alt="AI stack"/>
</p>

</details>

<details>
<summary><b>🚀 &nbsp;MLOps &amp; Deployment</b></summary>
<br/>

Models that only live in notebooks don't count. I train → track → containerize → serve → monitor.

- 📈 **Experiment tracking:** MLflow
- 🐳 **Containers:** Docker, Docker Compose
- ☁️ **Cloud:** AWS
- ⚡ **Inference:** async inference queues (Celery + RabbitMQ), ONNX Runtime, Redis caching
- 🧰 **Sandboxed execution:** running agent-generated experiment code in isolated sandboxes (E2B)
- ✅ **CI & quality:** GitHub Actions, Pytest, mutation checks, Playwright browser tests
- 🗄️ **Model & artifact hosting:** Hugging Face Hub

<p>
  <img src="https://skillicons.dev/icons?i=docker,aws,linux,git,github&perline=6" alt="MLOps stack"/>
  <img src="https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white" alt="MLflow"/>
</p>

</details>

<details>
<summary><b>🏗️ &nbsp;Backend &amp; SaaS Development</b></summary>
<br/>

Production-minded backends that wrap AI models in clean, tested, scalable services.

| Layer | Stack |
|---|---|
| **API** | FastAPI, Starlette, Pydantic |
| **Async & queues** | Celery, RabbitMQ, Redis |
| **Data** | PostgreSQL (+ pgvector), SQLite, SQLAlchemy, Alembic, Redis, Vector DBs |
| **Frontend** | Next.js, Tailwind CSS (dashboards for my SaaS products) |
| **Quality** | Pytest, Clean Architecture, Dependency Injection |

<p>
  <img src="https://skillicons.dev/icons?i=fastapi,postgres,redis,rabbitmq,sqlite,nextjs,tailwind&perline=7" alt="Backend stack"/>
</p>

</details>

<details>
<summary><b>🛡️ &nbsp;Security</b></summary>
<br/>

I build AI products, so I also care about securing them.

- 🔐 **Web & API security:** OWASP Top 10, **OWASP Top 10 for LLM Applications**, API security
- 🔑 **AuthN / AuthZ:** OAuth, JWT, API keys
- 🚦 **Hardening:** rate limiting, reverse proxy, basic pentesting
- 🧱 **AI security:** prompt-injection defense, PII redaction ([Sentinel-Shield](https://github.com/bartuonder/Sentinel-Shield))

</details>

<details>
<summary><b>💻 &nbsp;Languages &amp; Tools</b></summary>
<br/>

<p>
  <img src="https://skillicons.dev/icons?i=python,c,java,sql,git,github,pycharm,vscode,linux&perline=9" alt="Languages and tools"/>
</p>

</details>

---

## 🧪 Research &amp; From-Scratch Implementations

Learning by building: no black boxes, paper-faithful code, and tests where it matters.

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>📄 <a href="https://github.com/bartuonder/attention-is-all-you-need">Attention Is All You Need</a></h3>
      <p>Paper-to-code implementation of the original 2017 Transformer, written to match the paper (<b>Post-LN, sinusoidal PE, tied embeddings, label smoothing, Adam warmup, beam search with length penalty</b>) rather than wrapping <code>nn.Transformer</code>. Includes tests and a paper→code architecture map.</p>
      <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/> <img src="https://img.shields.io/badge/Paper-arXiv_1706.03762-b31b1b?style=flat-square"/>
    </td>
    <td width="50%" valign="top">
      <h3>🤖 <a href="https://github.com/bartuonder/GPT-2">GPT-2 (124M)</a></h3>
      <p>Clean from-scratch GPT-2 small: masked multi-head self-attention, FlashAttention via SDPA, loading of official pretrained weights, bf16 mixed-precision fine-tuning with cosine LR, grad accumulation and clipping, and temperature / top-k sampling.</p>
      <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/> <img src="https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white"/>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>🕵️ <a href="https://github.com/bartuonder/ai-agents-from-scratch">AI Agents From Scratch</a></h3>
      <p>Agents in <b>pure Python, with no frameworks</b>: LLM call → tool calling → ReAct agent loop → memory → plan-and-execute → reflection, plus evals and tests. The goal: show there's no magic in an agent, just a loop.</p>
      <img src="https://img.shields.io/badge/Agentic_AI-6A5ACD?style=flat-square"/> <img src="https://img.shields.io/badge/Pure_Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
    </td>
    <td width="50%" valign="top">
      <h3>🧮 <a href="https://github.com/bartuonder/machine-learning">Machine Learning From Scratch</a></h3>
      <p>Classic estimators in <b>NumPy only</b>: linear/logistic/softmax regression, decision trees, random forests, second-order gradient boosting, dual SVM (SMO), GMM, GDA, naive Bayes, k-means, PCA and a one-hidden-layer MLP. Every model is derived from an explicit objective.</p>
      <img src="https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white"/> <img src="https://img.shields.io/badge/Math-first-2E86C1?style=flat-square"/>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>🕸️ <a href="https://github.com/bartuonder/neural-networks-from-scratch">Neural Networks From Scratch</a></h3>
      <p>A small neural-network library with layers, activations, losses and manual backprop, validated with gradient checking and demos on XOR, regression and classification.</p>
      <img src="https://img.shields.io/badge/Backprop-FF6F61?style=flat-square"/> <img src="https://img.shields.io/badge/Gradient_Checking-17A589?style=flat-square"/>
    </td>
    <td width="50%" valign="top">
      <h3>🎭 <a href="https://github.com/bartuonder/ShakespeareGPT">ShakespeareGPT</a></h3>
      <p>A decoder-only GPT trained on Shakespeare's poetry to emulate the Bard's linguistic style and meter: dataset, model, training and generation scripts.</p>
      <img src="https://img.shields.io/badge/Language_Modeling-C0392B?style=flat-square"/> <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/>
    </td>
  </tr>
</table>

**Also:** 📚 [Paper-to-Code](https://github.com/bartuonder/Paper-to-Code) (a growing home for AI/ML/DL paper implementations) · 🔥 [PyTorch-General-Codes](https://github.com/bartuonder/PyTorch-General-Codes) (CNNs, ViT, transfer learning, TensorBoard, YOLO) · 📊 [Kaggle notebooks](https://www.kaggle.com/bartuonder)

---

## 🚀 Featured Projects

End-to-end AI products, from model to deployment.

| Project | What it does | Stack |
|---|---|---|
| 📑 **[Veridex](https://github.com/bartuonder/Veridex)** | Extractive **contract risk QA** SaaS. Fine-tuned **DeBERTa-v3 on CUAD → 87.96 F1**, tracked with MLflow. Inference isolated from the API via Celery/RabbitMQ, Redis caching, JWT/API-key auth, Next.js risk-card dashboard. [🤗 Model](https://huggingface.co/Bartu0nder/Veridex-QA-cuad-deberta-v3) | `PyTorch` `DeBERTa-v3` `FastAPI` `Celery` `Redis` `PostgreSQL` `Next.js` `MLflow` `Docker` |
| 🛡️ **[Sentinel-Shield](https://github.com/bartuonder/Sentinel-Shield)** | **AI security firewall** for LLM apps: PII redaction and prompt-injection blocking. **Deployed on AWS**, with JWT auth, Redis rate-limiting and a user dashboard with API keys and stats. | `FastAPI` `Starlette` `SQLAlchemy` `AWS` `Redis` `Next.js` |
| 🥗 **[MacroFit AI](https://github.com/bartuonder/MacroFitAI)** | Estimates **calories and macros from food photos** with a Vision Transformer, then builds nutrition tracking and workout plans. AI layer isolated via dependency injection. | `PyTorch` `ViT` `FastAPI` `Next.js` `PostgreSQL` `Docker` |
| 🖼️ **[Vision Classifier API](https://github.com/bartuonder/VisionClassifierAPI)** | ViT image-classification platform with an **async task queue** so heavy inference never blocks the server. JWT-secured and horizontally scalable via Docker. | `PyTorch` `Hugging Face` `Celery` `RabbitMQ` `JWT` `Docker` |
| 🌿 **[LeafLens](https://github.com/bartuonder/LeafLens)** | **MobileNetV3** detecting **38 plant diseases at ~97% accuracy**, served as a REST API with request logging. | `PyTorch` `FastAPI` `SQLAlchemy` `Tailwind` |
| 👁️ **[DeepGuard](https://github.com/bartuonder/DeepGuard)** | AI access-control / mini-**SOC**: face recognition, age estimation and emotion-based anomaly detection (anger/fear) with real-time event logging. | `PyTorch` `Transformers` `FastAPI` |
| 🎮 **[NextQuest](https://github.com/bartuonder/NextQuest)** | **LLM taste-based recommender** for games, movies, books, series and anime, with Pydantic **structured outputs**, top-up rounds for incomplete answers and per-query taste snapshots. | `LangChain` `OpenAI` `Pydantic` `PostgreSQL` `Docker` |
| 🧠 **[DocuMind API](https://github.com/bartuonder/DocuMind-API)** | Production-grade **RAG platform** to chat with your documents: async ingestion, vector search, ONNX inference and MLOps tooling. | `FastAPI` `PyTorch` `ONNX` `Qdrant` `Celery` `MLflow` |
| ☣️ **[ToxGate](https://github.com/bartuonder/ToxGate)** | Async **Turkish toxicity detection** PoC: DistilBERT on ONNX Runtime behind FastAPI, Celery workers and a Redis result cache. | `DistilBERT` `ONNX` `FastAPI` `RabbitMQ` `Redis` |

---

## 💼 Experience

**🏢 Software Engineering Intern, GullsEye Logistics Technologies Inc.** *(20 days)*

Designed and built, end to end, a fully **offline AI-powered semantic search engine** over enterprise documents.

- ⚡ Cut search latency to **~5 ms** by optimizing vector matrices with NumPy
- 🎯 Reached **Hit@3 = 90.6 %** and **MRR = 0.735** using custom chunking and an automated evaluation harness
- 🤗 Used Hugging Face **MiniLM-L12** embeddings, with a CLI on top of the core engine
- ✅ Secured the whole project with **164 unit and integration tests** (Pytest)

---

## 📊 GitHub Stats

<div align="center">

<a href="https://github.com/bartuonder">
  <img height="170" src="https://streak-stats.demolab.com?user=bartuonder&theme=tokyonight&hide_border=true&background=0f0c29&ring=24c6dc&fire=24c6dc&currStreakLabel=24c6dc" alt="Contribution streak"/>
  <img height="170" src="https://github-readme-stats.vercel.app/api/top-langs/?username=bartuonder&layout=compact&theme=tokyonight&hide_border=true&bg_color=0f0c29&title_color=24c6dc&langs_count=7" alt="Top languages"/>
</a>

<br/><br/>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/bartuonder/bartuonder/output/github-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/bartuonder/bartuonder/output/github-snake.svg"/>
  <img alt="GitHub contribution snake" src="https://raw.githubusercontent.com/bartuonder/bartuonder/output/github-snake-dark.svg"/>
</picture>

</div>

---

## 🎯 Currently

- 🔭 Re-implementing more landmark papers in [Paper-to-Code](https://github.com/bartuonder/Paper-to-Code)
- 🌱 Going deeper into LLM fine-tuning, RAG evaluation and agentic systems (LangGraph)
- 🎓 Preparing for **graduate studies / PhD in AI** in the USA
- 🤝 Open to **research collaborations, internships and interesting AI projects**

<div align="center">

<br/>

**📫 Let's connect!**
&nbsp;
[LinkedIn](https://www.linkedin.com/in/bartuonder/) · [Hugging Face](https://huggingface.co/Bartu0nder) · [Kaggle](https://www.kaggle.com/bartuonder) · [Email](mailto:onderbartu8@gmail.com)

<img src="https://capsule-render.vercel.app/api?type=waving&height=120&color=0:24c6dc,50:302b63,100:0f0c29&section=footer" alt="footer" width="100%"/>

</div>
