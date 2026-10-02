# Vansh Goenka

Applied AI engineer. I build retrieval systems that are fast and accurate, and I measure both.

Open to applied AI engineer roles in India, Germany and the UK. Available immediately.

I build production retrieval, evaluation and LLM cost control. At TinyCheque (an AI-first venture studio) I was the only backend engineer on Saroya AI, a mobile app where creators build an AI avatar that users chat with. It is in tester release on Play Store and TestFlight (Apple's beta-testing service).

## Measured results

| Metric | Before | After | How measured |
|---|---|---|---|
| Retrieval latency | 5 to 8 s, with timed-out streams (graph-database queries) | 0.6 s | Same retrieval step, before and after moving to Postgres with pgvector (vector search for Postgres) |
| Recall | 0.53 | 0.98 (MRR 0.89) | 71-question golden set, scored by an eval harness |
| Cached-input ratio | no baseline | 78% | Instrumented on every LLM call, checked weekly in CI against a 70% threshold |

Recall is the share of questions where the right passage was retrieved. MRR (mean reciprocal rank) rewards ranking it near the top. The new retrieval merges keyword and vector rankings with RRF (reciprocal rank fusion) and adds mem0, an open-source memory layer for LLM apps.

## Selected work

| Repo | Outcome | Stack |
|---|---|---|
| Saroya AI | Private, case study on portfolio. Backend API for auth, payments (Razorpay, an Indian payment provider), creator onboarding and chat. | TypeScript, Node, Express, Postgres, OpenRouter (a gateway to many LLM providers) |
| [meta-ad-creator](https://github.com/unusual9guy/meta-ad-creator) | Five cooperating agents turn a product photo into a 1080 by 1080 Meta ad image. | Python, Gemini, Streamlit, Docker |
| [market-research-agent](https://github.com/unusual9guy/market-research-agent) | Three agents turn a company or sector name into a report with AI use cases and datasets. | Python, LangChain, OpenAI, Tavily, Streamlit |
| [pizzeria-review-agent](https://github.com/unusual9guy/pizzeria-review-agent) | Answers questions about a restaurant from its reviews, fully local. | Python, LangChain, ChromaDB, Ollama |
| [Image-Classification-CNN](https://github.com/unusual9guy/Image-Classification-CNN) | Three CNNs on CIFAR-10. Best single model 89% test accuracy; averaging all three gave 87.9%. | TensorFlow, Keras |
| [Swarm-Robot-Simulation](https://github.com/unusual9guy/Swarm-Robot-Simulation) | BSc dissertation: simulating a connectivity rule for robot swarms in Webots. | Webots, C |
| [AI-Agent-for-research](https://github.com/unusual9guy/AI-Agent-for-research) | Research assistant that writes a report on any topic, with a hosted demo. | Python, LangChain, Streamlit |

## Stack by evidence

- Shipped in production: Python, TypeScript/Node/Express, PostgreSQL, pgvector, hybrid retrieval and RRF, LLM evaluation (recall@k, MRR), prompt and reply caching, SSE streaming, OpenRouter, mem0, Redis, Cloudflare R2, Docker, GCP Cloud Run, GitHub Actions CI/CD.
- Built in projects: LangChain, LangGraph, FastAPI, Streamlit, Ollama, ChromaDB, Gemini, OpenAI, Groq, Tavily, CNNs in TensorFlow/Keras, OpenCV, Hugging Face, GraphRAG on FalkorDB, MCP servers, agent harness design.
- Learning: NeMo Guardrails, Unsloth fine-tuning, n8n.

## Contact

- Email: vanshgoenka007@gmail.com
- LinkedIn: https://www.linkedin.com/in/vanshgoenka
