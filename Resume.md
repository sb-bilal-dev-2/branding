# Bilol Saidumarov

**AI Architect · Software Engineer**

· 00bilal@gmail.com
· +998909366692
· Tashkent, Uzbekistan
· [Official Website](https://bilol-saidumarov.vercel.app)
· [LinkedIn](https://www.linkedin.com/in/bilol-saidumarov-30b795356/)
· [Hugging Face](https://huggingface.co/bilalsaidumarov)
· [GitHub](https://github.com/sb-bilal-dev-2)

---

## Summary

Software engineer with 7+ years shipping production systems across web, mobile, and AI. Currently founding Vocoplay — an Uzbek-language AI tutor built on self-hosted open-source models — and previously built in-car STT/TTS voice assistants and Python speech pipelines at Xanavi. Native Uzbek speaker focused on low-resource-language NLP and speech, where off-the-shelf models fall short.

---

## Experience

### Co-founder / CTO — ARA (AI Resource Assistant)
*January 2026 – Present · Python, FastAPI, PyTorch, Hugging Face, PostgreSQL, Qdrant, RabbitMQ, vLLM, Docker*

- Self-hosted document-intelligence platform for ministry-scale archives — OCR, hybrid search, structured extraction, and citation-grounded RAG. Closed-perimeter deployment, no paid-API dependency.
- Fine-tuned Qwen 2.5 with LoRA and QLoRA on a trilingual (Uzbek / Russian / English) corpus across 15 task families — published as [bilalsaidumarov/ara-extract-v1](https://huggingface.co/bilalsaidumarov/ara-extract-v1) and [bilalsaidumarov/ara-extract-7b-qlora](https://huggingface.co/bilalsaidumarov/ara-extract-7b-qlora). 7B QLoRA on held-out eval: JSON validity 0% → 100%, exact-match 0% → 26.3%, char-similarity 0.166 → 0.610 (~3.7×).
- QLoRA on the 7B fits in ~7.6 GB peak VRAM on a single RTX 4060 — ~5 min wall time, ~40 MB adapter; 0.5B LoRA trains in ~20 sec.
- Async pipeline end-to-end: FastAPI gateway (<200 ms p95), RabbitMQ workers for OCR / embedding / LLM, PostgreSQL as source of truth (3NF, Alembic), Qdrant + BGE-m3 hybrid BM25 / semantic retrieval, append-only audit log.
- Owns the full surface: model selection, training & eval pipelines, backend, dashboard UI, landing page, docs, brand.

### Founder — Vocoplay
*Sep 2025 – Present · Python, PyTorch, Hugging Face Transformers, FastAPI, Docker*

- Building an Uzbek language-learning platform (mobile app + chat bot) on self-hosted open-source LLMs instead of paid APIs.
- Fine-tuning 7B-parameter open-source LLMs with SFT and LoRA/QLoRA on a ~20k-pair Uzbek corpus, lifting downstream eval accuracy ~18% over the base model.
- Generating lesson audio with FunAudioLLM (FunMusic) — ~60 hours of material across 12 cloned voices — giving learners native-quality Uzbek speech and music.
- Cost-engineered audio generation: self-hosting FunAudioLLM offsets ~$1k+ in one-shot paid-TTS catalog generation and ~$150/month in ongoing fresh-lesson audio vs an ElevenLabs cloned-voice tier (~$0.30 / 1k chars), with zero marginal cost per added minute beyond electricity.
- Scaled the audio-gen GPU from ~1 sequential request to ~25 concurrent (~25× throughput) via microbatched inference and a warm voice-clone pool, keeping per-request p95 under ~2s. Pre-rendered the top 200 lessons (~80% of traffic) to a disk cache served at <100ms median — freeing GPU capacity for the long tail.
- Designing the NLP pipeline behind lessons, feedback, and conversation — a RAG layer over ~5k lesson chunks with embedding-based retrieval returning context in <120ms p95.
- Deploying FastAPI inference services on Docker/Linux, running on a single GPU at ~800ms p95; owning dataset preparation, preprocessing, and evaluation workflows.
- Owning the product end-to-end alongside engineering: model selection, backend, mobile UI/UX, brand, and pitch deck.

### Software Engineer — Xanavi
*Dec 2023 – Sep 2025 · Python, PyTorch, Hugging Face, STT/TTS, Android, Docker*

- Designed custom STT/TTS voice-assistant solutions embedded in the Android system shipped across 3 production vehicle model lines.
- Built Python speech-analysis pipelines processing ~200 hours of in-car audio per training cycle, owning dataset preparation, preprocessing, and evaluation end-to-end.
- Trained and adapted open-source speech models for in-car audio conditions — cut WER on Uzbek/Russian speakers from ~22% to ~9%.
- Built internal tooling that cut localization and customization turnaround for the in-car Android system by ~50%.

### Software Engineer — PressReader
*May 2022 – Dec 2023 · Vancouver, BC, Canada · Full-time · JavaScript, TypeScript, React, Node.js*

- Shipped the company-wide redesign across the reader app (millions of monthly readers globally), replacing legacy UI with modernized full-stack flows.
- Built 8+ internal tools and integrations supporting the reader app and surrounding editorial workflows.

### Frontend Developer — TENNISI
*Jan 2021 – Nov 2021 · Moscow, Russia · Next.js, React, SSR*

- Migrated ~40 SSR pages onto a new design system across the full product, cutting first-paint by ~35%.

### JavaScript Developer — OX Group
*Apr 2019 – Jun 2020 · React, Node.js, Electron*

- Built a cross-platform POS system from scratch — Electron desktop client, Node.js backend, React UI — deployed across 50+ retail locations.

---

## Skills

**AI / ML:** PyTorch, Hugging Face Transformers, LLM fine-tuning (SFT, LoRA/QLoRA, PEFT), RAG, embedding models, vector databases (pgvector, Qdrant), STT/TTS, audio generation (FunAudioLLM / FunMusic), NLP/NLU, low-resource languages (Uzbek), OCR / Document Understanding, dataset preparation & evaluation, model optimization (quantization, vLLM, TensorRT-LLM)
**Languages:** Python, JavaScript, TypeScript, SQL
**Backend:** FastAPI, Node.js, PostgreSQL (indexing & query optimization), MongoDB, Redis, pgvector, RabbitMQ
**Frontend:** React, Next.js, Electron, TailwindCSS
**Mobile / Embedded:** Android (automotive), Flutter, React Native
**Infra & DevOps:** Docker, Linux, Git, CI/CD, GitHub Actions
**Engineering practice:** System design, distributed systems, async programming, TDD, code review & mentoring
**Product:** UI/UX, pitch decks, brand & logo, video editing
**Other:** Jira, Agile

---

## Languages

Uzbek — native · Russian — native · English — fluent

---

## Education

[Self Study]

---

## Selected Projects

**ARA (AI Resource Assistant)** — Self-hosted document-intelligence platform for government archives; OCR + hybrid search + structured extraction with custom Qwen 2.5 LoRA/QLoRA adapters published on Hugging Face (100% JSON validity on held-out eval, 7.6 GB peak VRAM training on an RTX 4060). Co-founder / CTO. 2026–present. [ara-production-baa8.up.railway.app](https://ara-production-baa8.up.railway.app/) (beta) · [huggingface.co/bilalsaidumarov/ara-extract-7b-qlora](https://huggingface.co/bilalsaidumarov/ara-extract-7b-qlora)

**Vocoplay** — Uzbek-language AI tutor (app + bot) on self-hosted open-source LLMs. Founder. 2025–present. [vocoplay.com](https://vocoplay.com)

**Xanavi Voice Assistant & Voice Analytics** — In-car STT/TTS built on custom models. 2023–2025. [xanavi-ai.uz](https://xanavi-ai.uz)

**OX Retail POS** — Cross-platform retail point-of-sale built with React + Electron. 2019–2020. [oxapp.io/en/products/oxretail/pos](https://oxapp.io/en/products/oxretail/pos)
