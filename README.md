<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:2563eb&height=140&section=header" alt="" width="100%" />

<h1 align="center">
<img src="https://readme-typing-svg.demolab.com?weight=700&size=24&duration=4500&pause=10&color=00BFFF&background=44113300&center=true&width=435&lines=Hey+,+I'm+Vansh+a.k.a+unusual9guy+;Nice+to+meet+you!%F0%9F%98%84" alt="Typing SVG" />
</h1>

I'm an AI Engineer specializing in Agentic Workflows architecting autonomous systems that plan and self-correct. Currently, I am engineering a SaaS-grade geospatial lead generation engine alongside a GenAI marketing workflow using Gemini and Nano Banana Pro to automate high-fidelity Meta ad creation.

My focus is on Human-in-the-Loop pipelines that turn probabilistic models into deterministic business value. Leveraging Python, LangGraph, FastAPI, and Docker, I build robust architectures designed to solve production challenges like inference latency and RAG hallucinations.

![Open to work](https://img.shields.io/badge/Open_to_work-India_%C2%B7_Germany_%C2%B7_UK-22c55e?style=for-the-badge)

---

## 🆕 Latest: Saroya AI

From February to September 2026 I was the only backend engineer on Saroya AI, a mobile app from TinyCheque (an AI-first venture studio) where creators build an AI avatar that their audience chats with. I wrote the API from scratch, built the ingestion pipeline, and ran the service from May 2026 until it reached testers on the Play Store and TestFlight. I write the eval set before I trust a change, so the numbers below come from a 71-question golden set that runs in CI.

| Metric | Before | After |
| :--- | :---: | :---: |
| Retrieval latency | 5 to 8 s | 0.6 s |
| Retrieval recall | 0.53 | 0.98 (MRR 0.89) |
| Cached-input ratio on LLM calls | n/a | 78% |

Graph-database queries were slow enough to time out streaming responses, so I moved retrieval to Postgres with pgvector and full-text search, fused with reciprocal rank fusion (RRF), and added mem0 for long-term memory.

```mermaid
flowchart LR
    U[User message] --> V[pgvector search]
    U --> F[Full-text search]
    V --> R[RRF fusion]
    F --> R
    M[mem0 memory] --> P[Prompt and cache]
    R --> P
    P --> L[OpenRouter<br/>5 providers, fallback]
    L --> S[SSE stream to mobile app]
```

<sub>Simplified view of the chat path.</sub>

---

## 🔍 Summary

- 🛠️ **AI Engineer** with production experience in building **Agentic RAG** systems, and **GenAI Marketing Pipelines**.
- 🧠 Hands-on experience training and refining **LLMs**, developing **CNN architectures**, and model deployment.
- 🔧 Proven track record of delivering business impact, including reducing content production costs by **100%** via automated **GenAI workflows** (Gemini/Nano Banana)
- 🚀 Sole backend engineer on a production GenAI mobile app: retrieval recall up from 0.53 to 0.98 and latency down from 5 to 8 s to 0.6 s, verified by an eval harness and gated on SLOs in CI.
- 💸 Built the LLM cost controls for that app, including prompt and reply caching and provider fallback, which reached a 78% cached-input ratio.

---

## 💼 Experience

### **AI Engineer | TinyCheque (Saroya AI)**
_Feb 2026 to Sep 2026_
* **Retrieval:** Cut retrieval latency from 5 to 8 s to 0.6 s and lifted recall from 0.53 to 0.98 (MRR 0.89). I moved retrieval to Postgres pgvector with full-text search, RRF fusion and mem0 memory, then wrote a 71-question golden set and eval harness to check that quality held.
* **Backend:** Built and ran the whole backend alone. I wrote the TypeScript/Node/Express API from scratch (auth, Razorpay payments, creator onboarding, chat) and operated it from May 2026 through the release to testers on Play Store and TestFlight.
* **LLM cost:** Real routing costs overran my cost model, so I instrumented every call, added prompt and reply caching, and pinned OpenRouter to 5 providers with fallback. The cached-input ratio reached 78%, and a weekly CI check alerts below 70%. Tokens stream to mobile over SSE with pacing and keepalive.
* **Ingestion:** Built the pipeline behind every avatar. It pulls creator content from X, Reddit, YouTube and LinkedIn, plus PDF, DOCX, XLSX and PPTX uploads with OCR. I added KYC identity checks and hard-delete workflows across every data store.
* **Pricing:** Originated the creator pricing and credit model the CPO adopted, plus the PRDs, ADRs and cost analyses the team planned against.
* **Tooling:** Set up a Claude Code harness with 14 subagents, 22 slash commands, and MCP tools and hooks that enforce spec-first and test-first work, backed by a 169-test suite.

### **AI Automation Engineer (Contract) | Chitra Goenka Crafts & Creations**
_Remote | Jan 2025 – Feb 2026_
* **GenAI Pipeline:** Architected a marketing workflow using **Nano Banana Pro (Gemini)** and **LangChain** to generate photorealistic product assets, cutting photoshoot costs by **100%**.
* **SaaS-Grade Tooling:** Engineered a **Geospatial Lead Finder** using Google Maps API that extracts global B2B leads with sub-second latency.
* **Deployment:** Built a **Streamlit** dashboard allowing non-technical staff to trigger complex scraping and generation tasks.

### **Software Engineer (Training Data) | G2i**
_Remote | Mar 2025 – Aug 2025_
* **RLHF & Data Quality:** Optimized AI-generated code by correcting logic errors to create high-quality ground truth data for training foundation models.
* **Safety & Compliance:** Enforced strict safety guidelines on code outputs to ensure compliance for production deployment.

### **Computer Vision Intern | CodeSpaze**
_Remote | Nov 2024 – Dec 2024_
* **Custom CNNs:** Architected a multi-class object recognition model (vehicles, biological entities), achieving **90% accuracy** via ensemble techniques.
* **Real-Time Inference:** Deployed a live inference pipeline via Streamlit for instant visual validation.

---

## 🌟 What makes me "Unusual"?

I don't just train models, I break them to see how they fail.
* **Agent First:** I believe the future isn't bigger models, but smarter **agentic loops**. I code for the future where AI plans, not just chats.
* **Rapid Learner:** Learned Swarm Robotics from scratch in 3 weeks for my dissertation because standard robotics felt too "safe."

## 🚀 About Me

* **Current Focus:** Architecting "Human-in-the-Loop" systems for B2B automation.
* **My Philosophy:** An AI model is only as good as the **pipeline** around it. I spend 20% of my time on the model and 80% on the **orchestration** (LangGraph), **data engineering** (RLHF), and **deployment** (FastAPI/Docker).
* **What I'm Building:** A geospatial lead-generation engine that combines Google Maps API with autonomous scraping agents to find B2B leads globally.
* **Language Mix:** Python first, plus TypeScript for the production backend I shipped this year.

---

## 🧪 Selected Projects

My recent production work is in private repos, so these are the public ones.

| Project | What it does | Stack |
| :--- | :--- | :--- |
| [meta-ad-creator](https://github.com/unusual9guy/meta-ad-creator) | Five cooperating Gemini agents turn a product photo into a 1080 x 1080 Meta ad image. | Gemini, Streamlit, Docker |
| [market-research-agent](https://github.com/unusual9guy/market-research-agent) | Three agents take a company or industry name and produce a market research report with AI use cases and matching datasets. | LangChain, OpenAI, Tavily, Exa |
| [pizzeria-review-agent](https://github.com/unusual9guy/pizzeria-review-agent) | Local RAG over restaurant reviews, so inference needs no cloud calls and costs nothing per query. | ChromaDB, Ollama, Llama 3.2 |
| [AI-Agent-for-research](https://github.com/unusual9guy/AI-Agent-for-research) | Research assistant that writes a structured report on any topic, with a hosted demo. | LangChain, Streamlit |
| [Swarm-Robot-Simulation](https://github.com/unusual9guy/Swarm-Robot-Simulation) | BSc dissertation: simulating and optimizing the beta algorithm for swarm connectivity with e-puck robots. | Webots, C |
| [Image-Classification-CNN](https://github.com/unusual9guy/Image-Classification-CNN) | Three CNNs on CIFAR-10 (best single model 89% test accuracy) and an ensemble comparison. | TensorFlow, Keras |

---

## 🎓 Education

BSc (Hons) Artificial Intelligence, 2:1, University of Manchester (2021 to 2024). Dissertation: simulation and optimization of the beta algorithm for autonomous swarm robotics.

---

## 🛠️ Skills

- **Agent Harness:**

<a href="https://www.anthropic.com/claude-code" target="_blank"><img src="https://cdn.simpleicons.org/claude" alt="Claude Code" title="Claude Code" width="40" height="40" /></a>
<a href="https://openai.com/codex/" target="_blank"><img src="https://avatars.githubusercontent.com/u/14957082" alt="Codex" title="Codex" width="40" height="40" /></a>
<a href="https://opencode.ai/" target="_blank"><picture><source media="(prefers-color-scheme: dark)" srcset="https://cdn.simpleicons.org/opencode/ffffff"><img src="https://cdn.simpleicons.org/opencode/000000" alt="OpenCode" title="OpenCode" width="40" height="40" /></picture></a>
<a href="https://pi.dev/" target="_blank"><img src="https://pi.dev/logo-auto.svg" alt="Pi (pi.dev)" title="Pi (pi.dev)" width="40" height="40" /></a>

- **Languages:**

<a href="https://www.java.com/en/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" width="40" height="40" /></a>
<a href="https://www.python.org/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" width="40" height="40" /></a>
<a href="https://en.wikipedia.org/wiki/C_(programming_language)" target="_blank"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/18/C_Programming_Language.svg/500px-C_Programming_Language.svg.png" width="40" height="40" /></a>
<a href="https://en.wikipedia.org/wiki/C%2B%2B" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/cplusplus/cplusplus-original.svg" width="40" height="40" /></a>
<a href="https://learn.microsoft.com/en-us/dotnet/csharp/" target="_blank"><img src="https://upload.wikimedia.org/wikipedia/commons/4/4f/Csharp_Logo.png" width="40" height="40" /></a>
<a href="https://en.wikipedia.org/wiki/JavaScript" target="_blank"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/6/6a/JavaScript-logo.png/500px-JavaScript-logo.png" width="40" height="40" /></a>
<a href="https://www.typescriptlang.org/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" width="40" height="40" /></a>

<!-- <a href="https://en.wikipedia.org/wiki/HTML" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" width="40" height="40" /></a>
<a href="https://en.wikipedia.org/wiki/CSS" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" width="40" height="40" /></a> -->

- **AI/ML:**

<a href="https://www.tensorflow.org/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/tensorflow/tensorflow-original.svg" width="40" height="40" /></a>
<a href="https://keras.io/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/keras/keras-original.svg" width="40" height="40" /></a>
<a href="https://scikit-learn.org/stable/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/scikitlearn/scikitlearn-original.svg" width="40" height="40" /></a>
<a href="https://opencv.org/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/opencv/opencv-original.svg" width="40" height="40" /></a>
<a href="https://streamlit.io/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/streamlit/streamlit-original.svg" width="40" height="40" /></a>
<a href="https://radimrehurek.com/gensim/" target="_blank"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTi0R_1V2XS3ez-Tz9sKSEf_TFKIikLALt6uA&s" width="40" height="40" /></a>

- **Tools:**

<a href="https://ollama.com/" target="_blank"><img src="https://avatars.githubusercontent.com/u/151674099?s=200&v=4" width="40" height="40" /></a>
<a href="https://www.langchain.com/" target="_blank"><img src="https://cdn.brandfetch.io/idzf7Sjo28/w/400/h/400/theme/dark/icon.jpeg?c=1bxid64Mup7aczewSAYMX&t=1743558261168" width="40" height="40" /></a>
<a href="https://git-scm.com/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" width="40" height="40" /></a>
<a href="https://about.gitlab.com/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/gitlab/gitlab-original.svg" width="40" height="40" /></a>
<a href="https://jupyter.org/" target="_blank"><img src="https://upload.wikimedia.org/wikipedia/commons/thumb/3/38/Jupyter_logo.svg/1280px-Jupyter_logo.svg.png" width="40" height="40" /></a>
<a href="https://unsloth.ai/" target="_blank"><img src="https://avatars.githubusercontent.com/u/150920049?s=280&v=4" width="40" height="40" /></a>

- **APIs:**

<a href="https://ai.google.dev/" target="_blank"><img src="https://uxwing.com/wp-content/themes/uxwing/download/brands-and-social-media/google-gemini-icon.png" width="40" height="40" /></a>
<a href="https://openai.com/" target="_blank"><img src="https://yt3.googleusercontent.com/MopgmVAFV9BqlzOJ-UINtmutvEPcNe5IbKMmP_4vZZo3vnJXcZGtybUBsXaEVxkmxKyGqX9R=s160-c-k-c0x00ffffff-no-rj" width="40" height="40" /></a>
<a href="https://www.perplexity.ai/api-platform" target="_blank"><img src="https://framerusercontent.com/images/gcMkPKyj2RX8EOEja8A1GWvCb7E.jpg?width=2000&height=2000" width="40" height="40" /></a>
<a href="https://huggingface.co/" target="_blank"><img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" width="40" height="40" /></a>
<a href="https://tavily.com/" target="_blank"><img src="https://pipedream.com/s.v0/app_qeh7Z6/logo/orig" width="40" height="40" /></a>
<a href="https://groq.com/" target="_blank"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSdtQY9Ofk71m8DVL5yV3d_sDPuqzCexABNLA&s" width="40" height="40" /></a>

- **Backend & DevOps**

<a href="https://fastapi.tiangolo.com/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/fastapi/fastapi-original.svg" width="40" height="40" /></a>
<a href="https://www.docker.com/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/docker/docker-original.svg" width="40" height="40" /></a>
<a href="https://postgresql.org/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/postgresql/postgresql-original.svg" width="40" height="40" /></a>
<a href="https://supabase.com/" target="_blank"><img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQLt5RQx6V1W6XXJcczgwNbzbdGyfHNCYtSCQ&s" width="40" height="40" /></a>
<a href="https://aws.amazon.com/" target="_blank"><img src="https://upload.wikimedia.org/wikipedia/commons/9/93/Amazon_Web_Services_Logo.svg" width="40" height="40" /></a>
<a href="https://nodejs.org/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/nodejs/nodejs-original.svg" width="40" height="40" /></a>
<a href="https://redis.io/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/redis/redis-original.svg" width="40" height="40" /></a>
<a href="https://cloud.google.com/run" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/googlecloud/googlecloud-original.svg" width="40" height="40" /></a>
<a href="https://github.com/features/actions" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/githubactions/githubactions-original.svg" width="40" height="40" /></a>

- **Also in use:** Express, pgvector, FalkorDB, ChromaDB, OpenRouter, mem0, Cloudflare R2, Apify, Railway, OpenTelemetry, SigNoz, Claude Code (custom subagents, skills, hooks), MCP

---

## 📊 GitHub Stats

[![Vansh's GitHub stats](https://github-readme-stats.vercel.app/api?username=unusual9guy&theme=dark)](https://github.com/unusual9guy/github-readme-stats)

[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=unusual9guy&theme=dark)](https://github.com/unusual9guy/github-readme-stats)

---

## 🤝 Let's Connect

I am actively looking for **AI Engineering** roles where I can deploy agentic systems to production. I'm based in Kolkata and available immediately, and I'm open to applied AI, forward-deployed and AI solutions engineering roles in India, Germany and the UK.

<p align="left">
<a href="https://www.linkedin.com/in/vanshgoenka/" target="blank"><img align="center" src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="vanshgoenka" /></a>
<a href="mailto:vanshgoenka007@gmail.com" target="blank"><img align="center" src="https://img.shields.io/badge/Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="email" /></a>
</p>
<!-- <a href="https://www.linkedin.com/in/vansh-goenka-ai/" target="_blank"><img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linkedin/linkedin-original.svg" width="20" height="20" /></a>-->

<h1 align="center">
<img src="https://readme-typing-svg.demolab.com?weight=700&size=24&duration=4000&pause=5&color=00BFFF&background=44113300&center=true&width=435&lines=Thank+you+for+visiting!%F0%9F%A4%97;Feel+free+to+explore+my+work!;See+you+again+soon!%F0%9F%99%83" alt="Typing SVG" />
</h1>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f172a,100:2563eb&height=100&section=footer" alt="" width="100%" />
