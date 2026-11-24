<!-- ═════════════════════════  HEADER  ═════════════════════════ -->
<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=240&color=0:0f0c29,50:302b63,100:24c6dc&text=Bartu%20%C3%96nder&fontColor=ffffff&fontSize=64&fontAlignY=36&desc=AI%20Researcher%20in%20the%20making%20%C2%B7%20AI%2FML%20Engineer%20by%20craft&descSize=20&descAlignY=58&animation=fadeIn" alt="Bartu Önder banner" width="100%"/>

<a href="https://github.com/bartuonder">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3200&pause=900&color=24C6DC&center=true&vCenter=true&width=760&lines=%F0%9F%A7%A0+Deep+Learning+%C2%B7+PyTorch+%C2%B7+Transformers;%F0%9F%93%84+Reproducing+papers%3A+paper+%E2%86%92+code+%E2%86%92+verified+numbers;%F0%9F%94%AC+Agents+that+test+ML+claims+with+statistics;%F0%9F%A4%96+RAG+%C2%B7+Agentic+AI+%C2%B7+LangGraph+%C2%B7+Evals;%E2%9A%99%EF%B8%8F+Training+%E2%86%92+Serving+%E2%86%92+Monitoring+%28MLOps%29;%F0%9F%8E%93+Aiming+for+a+PhD+in+AI+in+the+USA" alt="Typing animation"/>
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

<br/><br/>

<sub>
<a href="#-flagship-project-axiomforge">⭐ Flagship</a> ·
<a href="#-paper-reproductions">📄 Paper reproductions</a> ·
<a href="#-agentic-ai-and-rag-systems">🤖 Agentic AI &amp; RAG</a> ·
<a href="#-from-scratch-implementations">🧮 From scratch</a> ·
<a href="#-ml-and-deep-learning-applications">🧠 ML &amp; DL</a> ·
<a href="#-saas-products-and-ai-security">🏢 SaaS &amp; Security</a> ·
<a href="#-toolbox">🧰 Toolbox</a>
</sub>

</div>

---

## 👋 About me

I'm a **3rd-year Software Engineering student** (full scholarship, GPA 3.78/4.00) who wants to become an **AI researcher**: do a **PhD in AI in the USA** and help shape where the field goes next. I work on both halves of the job, and I try to keep them honest with each other:

| 🔬 Research | 🛠️ Engineering |
|---|---|
| Re-implement landmark papers from scratch and **compare my numbers with the paper's**, including where I fall short and why. | Turn models into tested, containerized, observable services with CI. |
| Multiple seeds, ablations, confidence intervals, multiple-testing corrections. | Async inference, RAG, agents with human approval, multi-tenant isolation. |
| Write down scope: what was reproduced, what was only implemented, what was not run. | Evaluation harnesses and regression gates that decide whether a change ships. |

> *"If I can't build it from scratch, I don't understand it yet."* 🧩

```python
class BartuOnder:
    role      = "AI/ML Engineer  →  AI Researcher"
    research  = ["Paper reproduction", "Evaluation & statistics", "LLMs & Transformers"]
    building  = ["Evaluated agentic systems", "RAG", "End-to-end ML products"]
    next_step = "PhD in AI 🇺🇸"

    def philosophy(self):
        return "Read the paper. Implement it. Measure it. Report it honestly. Ship it."
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

## 📄 Paper Reproductions

> **Paper → code → verified numbers.** [**Paper-to-Code**](https://github.com/bartuonder/Paper-to-Code) is the index of every paper I re-implement from scratch: one repo per paper, a paper → code map, tests that check the quantities the paper states, and a results table that says what matched and what did not.

| Paper | What I built | Result vs. the paper | Status |
|---|---|---|---|
| 🔧 **[LoRA: Low-Rank Adaptation of LLMs](https://github.com/bartuonder/LoRA-Low-Rank-Adaptation-of-Large-Language-Models)** <br/><sub>Hu et al., ICLR 2022</sub> | Hand-written `LoRALinear` (merge / unmerge, zero-init), a full fine-tuning baseline, **rank and projection ablations**, **5 seeds**, 170 training runs on RoBERTa-base / GLUE, plus latency and memory benchmarks. Logits match Hugging Face PEFT in tests. | **4 of 5 tasks within 0.5 pt** of the published numbers (SST-2 −0.3, MRPC −0.5, CoLA −0.3, STS-B −0.5). RTE is −7.9: the paper starts from an MNLI checkpoint and I did not. **0.24 %** trainable parameters. | ✅ Reproduced · [🤗 weights](https://huggingface.co/Bartu0nder/lora-roberta-base-glue) |
| 🏗️ **[Deep Residual Learning (ResNet)](https://github.com/bartuonder/deep-residual-learning-for-image-recognition)** <br/><sub>He et al., CVPR 2016</sub> | Plain and residual networks (CIFAR-10 `6n+2`, ImageNet ResNet-18 to 152) with shortcut options A/B/C, trained with the paper's protocol. Tests check ImageNet FLOPs (Table 1) and parameter counts. | **ResNet-110: 6.42 % error (paper 6.43 %).** The degradation of plain nets with depth (Fig. 6) is reproduced: it is an optimization problem, not overfitting. | ✅ Reproduced (CIFAR-10) |
| 🧬 **[Attention Is All You Need](https://github.com/bartuonder/attention-is-all-you-need)** <br/><sub>Vaswani et al., NeurIPS 2017</sub> | The original Transformer without `nn.Transformer`: Post-LN, sinusoidal PE, tied embeddings, label smoothing, Adam warmup, beam search with length penalty. | Base model **63.0 M params** (paper 65 M). Paper-scale WMT BLEU was not run, and the repo says so. | 🧪 Implemented & tested |

<div align="center">
  <img src="https://raw.githubusercontent.com/bartuonder/deep-residual-learning-for-image-recognition/HEAD/docs/cifar10_plain_vs_resnet.png" alt="Plain vs residual networks on CIFAR-10" width="48%"/>
  <img src="https://raw.githubusercontent.com/bartuonder/LoRA-Low-Rank-Adaptation-of-Large-Language-Models/HEAD/figures/rank_ablation.png" alt="LoRA rank ablation on GLUE" width="48%"/>
  <br/>
  <sub>Left: ResNet plain vs. residual on CIFAR-10 (Fig. 6 reproduced). Right: LoRA rank ablation on GLUE.</sub>
</div>

<br/>

**How I reproduce a paper**

- 🧱 **From scratch:** the method is written by hand and follows the paper's equations and section numbers. No `nn.Transformer`, no `torchvision.models`, no PEFT in the training path.
- ✅ **Verified:** tests assert what the paper states (parameter counts, FLOPs, masking, schedules, equivalence to a reference implementation).
- 📊 **Measured properly:** several seeds, mean ± std next to the paper's statistic, ablations, and a stated hypothesis for every gap.
- 🪞 **Honest about scope:** each entry says what was reproduced, what was only implemented, and what was not run.

<p>
  <a href="https://github.com/bartuonder/Paper-to-Code"><img src="https://img.shields.io/badge/📄_Paper--to--Code_index-24c6dc?style=for-the-badge" alt="Paper-to-Code"/></a>
  <a href="https://github.com/bartuonder/Paper-to-Code/tree/main/papers"><img src="https://img.shields.io/badge/📝_Per--paper_write--ups-302b63?style=for-the-badge" alt="Write-ups"/></a>
</p>


---

## 🤖 Agentic AI and RAG Systems

Agents and retrieval systems that are **measured, not just demoed**: each one ships with an evaluation harness, a red-team set and numbers that link back to the run that produced them. My flagship, [**AxiomForge**](#-flagship-project-axiomforge), belongs here too.

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>🤝 <a href="https://github.com/bartuonder/Parley">Parley</a></h3>
      <p>Eval-driven <b>multi-agent customer operations</b> platform. LangGraph specialists resolve refund, shipping and subscription tickets with policy RAG, MCP tool use, a <b>policy critic</b> and human approval. <b>98.8 % task success</b> on 55 core scenarios (140 in total), <b>pass^4 96.4 %</b>, <b>0 of 108</b> attacks landed with guards on, ~$0.003 per ticket. 1500+ tests, OpenTelemetry traces, Next.js console.</p>
      <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square"/> <img src="https://img.shields.io/badge/MCP-6A5ACD?style=flat-square"/> <img src="https://img.shields.io/badge/pgvector-4169E1?style=flat-square&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/OpenTelemetry-425CC7?style=flat-square&logo=opentelemetry&logoColor=white"/> <img src="https://img.shields.io/badge/Evals-17A589?style=flat-square"/>
    </td>
    <td width="50%" valign="top">
      <h3>🏢 <a href="https://github.com/bartuonder/Mabeyn">Mabeyn</a></h3>
      <p>Multi-tenant support agent you embed with <b>one script tag</b>: cited answers from your documents (hybrid retrieval, reranker, faithfulness check), tool use with <b>human approval</b>, customer memory and a four-layer <b>LLM firewall</b>. <b>Accuracy 0.95</b> on 80 dev questions and 0.97 on 30 held-out ones; <b>0 of 80</b> attacks worked with the firewall on. PostgreSQL <b>Row-Level Security</b>, 700+ tests, CI evaluation gate.</p>
      <img src="https://img.shields.io/badge/LangGraph-1C3C3C?style=flat-square"/> <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/> <img src="https://img.shields.io/badge/PostgreSQL_RLS-4169E1?style=flat-square&logo=postgresql&logoColor=white"/> <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white"/> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>🧠 <a href="https://github.com/bartuonder/DocuMind-API">DocuMind API</a></h3>
      <p>Production-grade <b>RAG platform</b> to chat with your documents: async ingestion, vector search, ONNX inference and MLOps tooling.</p>
      <img src="https://img.shields.io/badge/Qdrant-DC244C?style=flat-square"/> <img src="https://img.shields.io/badge/ONNX-005CED?style=flat-square&logo=onnx&logoColor=white"/> <img src="https://img.shields.io/badge/Celery-37814A?style=flat-square&logo=celery&logoColor=white"/> <img src="https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=mlflow&logoColor=white"/>
    </td>
    <td width="50%" valign="top">
      <h3>🎮 <a href="https://github.com/bartuonder/NextQuest">NextQuest</a></h3>
      <p><b>LLM taste-based recommender</b> for games, movies, books, series and anime, with Pydantic <b>structured outputs</b>, top-up rounds for incomplete answers and per-query taste snapshots.</p>
      <img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square"/> <img src="https://img.shields.io/badge/Pydantic-E92063?style=flat-square&logo=pydantic&logoColor=white"/> <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white"/>
    </td>
  </tr>
</table>

**Also:** 🕵️ [AI Agents From Scratch](https://github.com/bartuonder/ai-agents-from-scratch), the same ideas in pure Python with no framework (see below).


---

## 🧮 From-Scratch Implementations

Learning by building: no black boxes, from the math to the training loop. The paper-faithful ones are in [Paper Reproductions](#-paper-reproductions).

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>🤖 <a href="https://github.com/bartuonder/GPT-2">GPT-2 (124M)</a></h3>
      <p>Clean from-scratch GPT-2 small: masked multi-head self-attention, FlashAttention via SDPA, loading of official pretrained weights, bf16 mixed-precision fine-tuning with cosine LR, grad accumulation and clipping, and temperature / top-k sampling.</p>
      <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/> <img src="https://img.shields.io/badge/CUDA-76B900?style=flat-square&logo=nvidia&logoColor=white"/>
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
      <h3>🕵️ <a href="https://github.com/bartuonder/ai-agents-from-scratch">AI Agents From Scratch</a></h3>
      <p>Agents in <b>pure Python, with no frameworks</b>: LLM call → tool calling → ReAct loop → memory → plan-and-execute → reflection, plus evals and tests. The goal: show there is no magic in an agent, just a loop.</p>
      <img src="https://img.shields.io/badge/Agentic_AI-6A5ACD?style=flat-square"/> <img src="https://img.shields.io/badge/Pure_Python-3776AB?style=flat-square&logo=python&logoColor=white"/>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>🎭 <a href="https://github.com/bartuonder/ShakespeareGPT">ShakespeareGPT</a></h3>
      <p>A decoder-only GPT trained on Shakespeare's poetry to emulate the Bard's linguistic style and meter: dataset, model, training and generation scripts.</p>
      <img src="https://img.shields.io/badge/Language_Modeling-C0392B?style=flat-square"/> <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/>
    </td>
    <td width="50%" valign="top">
      <h3>🔥 <a href="https://github.com/bartuonder/PyTorch-General-Codes">PyTorch General Codes</a></h3>
      <p>My PyTorch notebook collection: CNNs, Vision Transformers, transfer learning, TensorBoard and YOLO.</p>
      <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/> <img src="https://img.shields.io/badge/Notebooks-F37626?style=flat-square&logo=jupyter&logoColor=white"/>
    </td>
  </tr>
</table>

**Also:** 📊 [Kaggle notebooks](https://www.kaggle.com/bartuonder) · 🧩 [Python-DSA](https://github.com/bartuonder/Python-DSA) and [NeetCode-150](https://github.com/bartuonder/NeetCode-150) (algorithms practice)


---

## 🧠 ML and Deep Learning Applications

Models trained, evaluated and served: tabular, NLP and vision.

<table>
  <tr>
    <td width="50%" valign="top">
      <h3>🏦 <a href="https://github.com/bartuonder/credit-default-risk">Credit Default Risk</a></h3>
      <p><b>Calibrated</b> credit-card default prediction on 30,000 clients. Repeated-CV model comparison with significance tests, <b>cost-based decision threshold</b>, SHAP explanations, fairness diagnostics and a FastAPI service. LightGBM <b>ROC-AUC 0.784</b>, <b>PR-AUC 0.565</b>, test ECE 0.010. A hold-out set used once and every README number generated from <code>results/</code>.</p>
      <img src="https://img.shields.io/badge/LightGBM-2980B9?style=flat-square"/> <img src="https://img.shields.io/badge/scikit-learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white"/> <img src="https://img.shields.io/badge/SHAP-8E44AD?style=flat-square"/> <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/> <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white"/>
    </td>
    <td width="50%" valign="top">
      <h3>☣️ <a href="https://github.com/bartuonder/ToxGate">ToxGate</a></h3>
      <p>Async <b>Turkish toxicity detection</b> PoC: DistilBERT on ONNX Runtime behind FastAPI, Celery workers and a Redis result cache.</p>
      <img src="https://img.shields.io/badge/DistilBERT-FFD21E?style=flat-square&logo=huggingface&logoColor=black"/> <img src="https://img.shields.io/badge/ONNX-005CED?style=flat-square&logo=onnx&logoColor=white"/> <img src="https://img.shields.io/badge/RabbitMQ-FF6600?style=flat-square&logo=rabbitmq&logoColor=white"/> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white"/>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>🌿 <a href="https://github.com/bartuonder/LeafLens">LeafLens</a></h3>
      <p><b>MobileNetV3</b> detecting <b>38 plant diseases at ~97 % accuracy</b>, served as a REST API with request logging.</p>
      <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/> <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/> <img src="https://img.shields.io/badge/SQLAlchemy-D71F00?style=flat-square"/>
    </td>
    <td width="50%" valign="top">
      <h3>👁️ <a href="https://github.com/bartuonder/DeepGuard">DeepGuard</a></h3>
      <p>AI access-control / mini-<b>SOC</b>: face recognition, age estimation and emotion-based anomaly detection (anger/fear) with real-time event logging.</p>
      <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white"/> <img src="https://img.shields.io/badge/Transformers-FFD21E?style=flat-square&logo=huggingface&logoColor=black"/> <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>🎯 <a href="https://github.com/bartuonder/YoloDetectionWebApp">YOLO + CLIP Detection</a></h3>
      <p>Real-time object detection web app. <b>CLIP re-ranking</b> fixes the small handheld objects (mouse, phone, wallet) that YOLO confuses.</p>
      <img src="https://img.shields.io/badge/YOLO-00FFFF?style=flat-square"/> <img src="https://img.shields.io/badge/CLIP-412991?style=flat-square&logo=openai&logoColor=white"/> <img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white"/>
    </td>
    <td width="50%"></td>
  </tr>
</table>


---

## 🏢 SaaS Products and AI Security

Models wrapped in real products: auth, queues, dashboards and deployment. Multi-tenant SaaS with isolation is also in [Mabeyn](https://github.com/bartuonder/Mabeyn), and the red-team work is in [Parley](https://github.com/bartuonder/Parley).

| Project | What it does | Stack |
|---|---|---|
| 📑 **[Veridex](https://github.com/bartuonder/Veridex)** | Extractive **contract risk QA** SaaS. Fine-tuned **DeBERTa-v3 on CUAD → 87.96 F1**, tracked with MLflow. Inference isolated from the API via Celery/RabbitMQ, Redis caching, JWT/API-key auth, Next.js risk-card dashboard. [🤗 Model](https://huggingface.co/Bartu0nder/Veridex-QA-cuad-deberta-v3) | `PyTorch` `DeBERTa-v3` `FastAPI` `Celery` `Redis` `PostgreSQL` `Next.js` `MLflow` `Docker` |
| 🛡️ **[Sentinel-Shield](https://github.com/bartuonder/Sentinel-Shield)** | **AI security firewall** for LLM apps: PII redaction and prompt-injection blocking. **Deployed on AWS**, with JWT auth, Redis rate-limiting and a user dashboard with API keys and stats. | `FastAPI` `Starlette` `SQLAlchemy` `AWS` `Redis` `Next.js` |
| 🥗 **[MacroFit AI](https://github.com/bartuonder/MacroFitAI)** | Estimates **calories and macros from food photos** with a Vision Transformer, then builds nutrition tracking and workout plans. AI layer isolated via dependency injection. | `PyTorch` `ViT` `FastAPI` `Next.js` `PostgreSQL` `Docker` |
| 🖼️ **[Vision Classifier API](https://github.com/bartuonder/VisionClassifierAPI)** | ViT image-classification platform with an **async task queue** so heavy inference never blocks the server. JWT-secured and horizontally scalable via Docker. | `PyTorch` `Hugging Face` `Celery` `RabbitMQ` `JWT` `Docker` |


---

## 🧰 Toolbox

> Click a section to expand 👇

<details open>
<summary><b>🔬 &nbsp;Research &amp; Evaluation</b></summary>
<br/>

Reading papers, re-implementing them, and deciding with statistics whether a claim holds.

<p>
  <img src="https://img.shields.io/badge/Paper_Reproduction-F1C40F?style=flat-square&labelColor=555"/>
  <img src="https://img.shields.io/badge/Ablation_Studies-E67E22?style=flat-square"/>
  <img src="https://img.shields.io/badge/Hypothesis_Testing-1ABC9C?style=flat-square"/>
  <img src="https://img.shields.io/badge/Multiple_Testing_Correction-8E44AD?style=flat-square"/>
  <img src="https://img.shields.io/badge/Confidence_Intervals-2E86C1?style=flat-square"/>
  <img src="https://img.shields.io/badge/Calibration-17A589?style=flat-square"/>
  <img src="https://img.shields.io/badge/Reproducibility-34495E?style=flat-square"/>
  <img src="https://img.shields.io/badge/Linear_Algebra_%26_Calculus-6A5ACD?style=flat-square"/>
  <img src="https://img.shields.io/badge/Probability_%26_Statistics-C0392B?style=flat-square"/>
</p>

See [📄 Paper Reproductions](#-paper-reproductions) and the [⭐ flagship](#-flagship-project-axiomforge).

</details>

<details open>
<summary><b>🧠 &nbsp;AI / ML / GenAI</b></summary>
<br/>

| Area | Topics & tools |
|---|---|
| **Deep Learning** | PyTorch, Transformers, CNNs / ResNets, Vision Transformers (ViT), MobileNet, DeBERTa, transfer learning, mixed-precision (bf16) training |
| **LLMs & fine-tuning** | Hugging Face Transformers, **LoRA / PEFT**, GLUE-style evaluation, embeddings and semantic search, structured outputs |
| **GenAI / RAG** | Hybrid retrieval (vectors + full text), reranking, chunking, faithfulness checks, retrieval evaluation (Hit@k, MRR, document recall), vector stores (pgvector, Qdrant, Chroma) |
| **Agentic AI** | Tool calling, ReAct, planning, memory, reflection, **LangGraph** (human-in-the-loop interrupts, checkpoints), **MCP**, multi-agent routing, policy critics, LLM guardrails |
| **Agent evaluation** | Scenario suites with expected end states, pass^k reliability, LLM-judge calibration, red-teaming, regression gates in CI |
| **Computer Vision** | OpenCV, image classification, object detection (YOLO, CLIP), face recognition & emotion analysis |
| **Classical ML & data** | scikit-learn, XGBoost / LightGBM / CatBoost, SHAP, probability calibration, cost-based thresholds, NumPy, SciPy, Pandas |

<p>
  <img src="https://skillicons.dev/icons?i=python,pytorch,opencv,sklearn&perline=6" alt="AI stack"/>
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy"/>
  <img src="https://img.shields.io/badge/pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" alt="pandas"/>
  <img src="https://img.shields.io/badge/Hugging_Face-FFD21E?style=for-the-badge&logo=huggingface&logoColor=black" alt="Hugging Face"/>
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
- 🔭 **Observability:** OpenTelemetry traces, LangSmith, cost and latency tracking
- 🧰 **Sandboxed execution:** running agent-generated experiment code in isolated sandboxes (E2B)
- ✅ **CI & quality:** GitHub Actions, Pytest, Ruff, mypy, Playwright browser tests, Locust load tests, evaluation gates
- 🗄️ **Model & artifact hosting:** Hugging Face Hub

<p>
  <img src="https://skillicons.dev/icons?i=docker,aws,linux,githubactions&perline=6" alt="MLOps stack"/>
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
| **Data** | PostgreSQL (+ pgvector, Row-Level Security), SQLite, SQLAlchemy, Alembic, Redis, vector databases |
| **Frontend** | Next.js, TypeScript, Tailwind CSS (dashboards and consoles for my products) |
| **Quality** | Pytest, Clean Architecture, Dependency Injection |

<p>
  <img src="https://skillicons.dev/icons?i=fastapi,postgres,redis,rabbitmq,sqlite,nextjs,ts,tailwind&perline=8" alt="Backend stack"/>
</p>

</details>

<details>
<summary><b>🛡️ &nbsp;Security</b></summary>
<br/>

I build AI products, so I also care about securing them.

- 🔐 **Web & API security:** OWASP Top 10, **OWASP Top 10 for LLM Applications**, API security
- 🔑 **AuthN / AuthZ:** OAuth, JWT, API keys
- 🚦 **Hardening:** rate limiting, reverse proxy, basic pentesting
- 🧱 **AI security:** prompt-injection defense, PII redaction, canary tokens, tool allowlists, red-team evaluation ([Sentinel-Shield](https://github.com/bartuonder/Sentinel-Shield), [Mabeyn](https://github.com/bartuonder/Mabeyn), [Parley](https://github.com/bartuonder/Parley))

</details>

<details>
<summary><b>💻 &nbsp;Languages &amp; Tools</b></summary>
<br/>

<p>
  <img src="https://skillicons.dev/icons?i=python,ts,bash,git,github,linux&perline=6" alt="Languages and tools"/>
  <img src="https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white" alt="SQL"/>
</p>

</details>


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

- 📄 Reproducing more landmark papers for [Paper-to-Code](https://github.com/bartuonder/Paper-to-Code), with the same standard: tests against the paper, several seeds, honest scope
- 🔬 Taking [AxiomForge](https://github.com/bartuonder/AxiomForge) further as a research tool for evaluating ML claims
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
