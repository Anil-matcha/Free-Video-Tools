# Awesome AI Image Models [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> The most complete, up-to-date comparison of AI image generation models — **which model, via which API, at what price, and what it's best at.**

Unlike other lists that just dump links, this one answers the question developers actually have: *"I need to generate images — which model do I pick, and where do I call it?"* Every model is mapped to the APIs that serve it, with real per-image pricing and what it's genuinely good for.

> 💡 Prices are per **standard image** (retail API rates verified July 2026) and move fast — always confirm against the provider. 4K/high-res and batch modes change the math (batch often ~50% off).

## Related Projects

- [awesome-uncensored-ai-image-models](https://github.com/Anil-matcha/awesome-uncensored-ai-image-models) — Filtering-, access-, and licensing-focused companion catalog for local and hosted image model variants
- [MuAPI image playground](https://muapi.ai/playground) — Run the image models compared in this list through one API.
- [MuAPI model docs](https://muapi.ai/docs/models) — Browse model IDs and supported capabilities.
- [awesome-ai-video-models](https://github.com/Anil-matcha/awesome-ai-video-models) — sister list: compare AI **video** models by API, price & speed
- [Open-Generative-AI](https://github.com/Anil-matcha/Open-Generative-AI) — curated hub of open generative-media tools and pipelines
- [Awesome-GPT-Image-2-API-Prompts](https://github.com/Anil-matcha/Awesome-GPT-Image-2-API-Prompts) — prompt library for GPT Image
- [nano-banana-generator](https://github.com/SamurAIGPT/nano-banana-generator) — generate with Google Nano Banana
- [ai-headshot-generator](https://github.com/SamurAIGPT/ai-headshot-generator) — AI headshots pipeline
- [Generative-Media-Skills](https://github.com/SamurAIGPT/Generative-Media-Skills) — runtime for generative-media prompts
- [ai-creator-academy](https://github.com/Anil-matcha/ai-creator-academy) — free curriculum teaching creators how to monetize the models compared in this list
- [Flux-3-Dev-API](https://github.com/Anil-matcha/Flux-3-Dev-API) — Python wrapper for Black Forest Labs' FLUX 3 (Dev variant) — text-to-image, image-to-image, text-to-video, image-to-video
- [Grok-Imagine-Image-2-API](https://github.com/Anil-matcha/Grok-Imagine-Image-2-API) — Python SDK and MCP server for Grok Imagine Image 2.0 text-to-image and multi-reference editing through MuAPI
- [awesome-flux-3-api-prompts](https://github.com/Anil-matcha/awesome-flux-3-api-prompts) — FLUX 3 API guide, prompts, and parameters

## Contents

- [Commercial models (closed, API-only)](#commercial-models-closed-api-only)
- [Open-source models (self-host or API)](#open-source-models-self-host-or-api)
- [Image editing & control](#image-editing--control)
- [Frameworks & UIs](#frameworks--uis)
- [Upscaling & restoration](#upscaling--restoration)
- [Benchmarks & leaderboards](#benchmarks--leaderboards)
- [How to choose](#how-to-choose)
- [Where to run them (API providers)](#where-to-run-them-api-providers)
- [Contributing](#contributing)

## Commercial models (closed, API-only)

| Model | Maker | Best for | APIs | Price / image | Notes |
|-------|-------|----------|------|---------------|-------|
| **Nano Banana Pro** | Google | 4K, editing, realism | Gemini API, Fal, Replicate, MuAPI | ~$0.20 (4K ~$0.24; batch 2K ~$0.067) | Best true 4K; strong image editing |
| **GPT Image 1.5** | OpenAI | Instruction following, text | OpenAI API, Fal | ~$0.04 | Excellent prompt adherence |
| **FLUX.2 [pro]** | Black Forest Labs | Cheapest premium, 4MP | Fal, Replicate, BFL API, MuAPI | ~$0.015–0.02 | Best price/quality |
| **Seedream 4.5** | ByteDance | Value + quality | Fal, Replicate, MuAPI | ~$0.04 | Strong all-rounder |
| **Imagen 4** | Google | Photorealism | Gemini / Vertex AI | ~$0.04 | Google's flagship photoreal |
| **Ideogram v3** | Ideogram | In-image text, typography | Ideogram API, Fal, Replicate | ~$0.07 (Balanced) | Best text-in-image |
| **Recraft V3** | Recraft | Design, vector, brand | Fal, Replicate | ~$0.04 | SVG/vector + style control |
| **Midjourney v7** | Midjourney | Aesthetic / artistic | ⚠️ No official API | Subscription only | Access via web/Discord only |

## Open-source models (self-host or API)

| Model | Maker | License | Best for | APIs | Self-host VRAM |
|-------|-------|---------|----------|------|----------------|
| **FLUX.2 [dev]** | Black Forest Labs | Non-commercial (paid license for commercial) | Top OSS quality, 4MP | Fal, Replicate | ~24GB+ |
| **FLUX.1 [schnell]** | Black Forest Labs | Apache-2.0 | Fast + free commercial use | Fal, Replicate | ~12GB+ |
| **Qwen-Image** | Alibaba | Apache-2.0 | Best in-image text (EN/CN) | Fal, Replicate | ~24GB+ (20B) |
| **HunyuanImage 3.0** | Tencent | Open (check terms) | Largest OSS model (80B MoE) | self-host | ~40GB+ |
| **Stable Diffusion 3.5 Large** | Stability AI | Community License (free <$1M rev) | Ecosystem, LoRAs, ControlNet | Fal, Replicate, self-host | ~18GB+ |
| **SANA** | NVIDIA | Permissive research | Fast, efficient, low-VRAM | self-host | ~12GB |

## Image editing & control

Modify existing images rather than generate from scratch:

- **Nano Banana Pro / FLUX.2** — natural-language image editing (img2img, inpainting, relighting)
- **FLUX.1 Kontext** — instruction-based editing, character consistency
- **ControlNet** — structural conditioning (pose, depth, edges, scribble)
- **IP-Adapter** — image prompting / style + subject transfer
- **Inpainting/outpainting** — supported natively by FLUX, SD 3.5, and most APIs above

## Frameworks & UIs

For local generation, training, and workflows:

- **[ComfyUI](https://github.com/comfyanonymous/ComfyUI)** — node-based, most powerful for custom pipelines
- **[AUTOMATIC1111 WebUI](https://github.com/AUTOMATIC1111/stable-diffusion-webui)** — the classic all-in-one UI
- **[InvokeAI](https://github.com/invoke-ai/InvokeAI)** — polished pro/creative UI
- **[Fooocus](https://github.com/lllyasviel/Fooocus)** — simplest "just works" UI
- **Training:** kohya_ss, OneTrainer, SimpleTuner (LoRA / fine-tuning)

## Upscaling & restoration

- **Real-ESRGAN** — general-purpose upscaling (open source)
- **GFPGAN / CodeFormer** — face restoration
- **chaiNNer** — node-based batch processing
- **Topaz Photo AI** — highest-quality commercial upscale/denoise

## Benchmarks & leaderboards

Check independent evals before trusting a maker's demo gallery:

- **Artificial Analysis Image Arena** — Elo-style human-preference leaderboard
- **HEIM** (Holistic Evaluation of Image Models) — multi-dimension benchmark
- **FID / CLIP Score / ImageReward** — automated quality & alignment metrics

## How to choose

- **Best 4K / editing** → Nano Banana Pro
- **Best value premium** → FLUX.2 [pro] (~$0.015–0.02/image)
- **Best text in image** → Ideogram v3 or Qwen-Image (open)
- **Best instruction following** → GPT Image 1.5
- **Design / vector / brand** → Recraft V3
- **Fully open, commercial-safe** → FLUX.1 [schnell] or Qwen-Image (both permissive)
- **Ecosystem & LoRAs** → Stable Diffusion 3.5

## Where to run them (API providers)

Aggregators that expose many of the above behind one API/key:

- **[MuAPI](https://muapi.ai)** — unified API across image + video models (Nano Banana, FLUX, Seedream, and more), one key, one billing
- **[Fal](https://fal.ai)** — fast inference, broad model catalog
- **[Replicate](https://replicate.com)** — pay-per-run, large community model catalog
- **[Eimu](https://eimu.art)** — GPT Image 2 & Nano Banana Pro generation API (OpenAI-compatible) with MCP integration — sign in and use, no relay setup or API key required

Native APIs (single-vendor): Google Gemini/Vertex (Nano Banana, Imagen), OpenAI (GPT Image), Black Forest Labs (FLUX), Ideogram, Recraft.

## Contributing

PRs welcome. When adding a model, keep the table columns filled — **a row without provider + price isn't useful.** New models go in the correct table (commercial vs open-source) and stay sorted by relevance.

---

*Maintained alongside [awesome-ai-video-models](https://github.com/Anil-matcha/awesome-ai-video-models) and [Open-Generative-AI](https://github.com/Anil-matcha/Open-Generative-AI). Found it useful? ⭐ the repo.*
