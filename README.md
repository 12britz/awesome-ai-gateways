# Awesome AI Gateways

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
[![License: CC0](https://img.shields.io/badge/License-CC0-1.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
[![Stars](https://img.shields.io/github/stars/your-username/awesome-ai-gateways?style=social)](https://github.com/your-username/awesome-ai-gateways)

> A curated list of tools, libraries, and resources for LLM routing, orchestration, and gateway infrastructure.

Managing 100+ LLM APIs, handling rate limits, implementing fallbacks, and tracking token costs is a massive operational headache. This list curates the best open-source tools, managed services, and resources to help you build production-grade AI infrastructure.

## Table of Contents

- [AI Gateways](#ai-gateways)
- [Semantic Caching](#semantic-caching)
- [Cost Tracking & Analytics](#cost-tracking--analytics)
- [Load Balancing & Routing](#load-balancing--routing)
- [API Management & Rate Limiting](#api-management--rate-limiting)
- [Observability & Logging](#observability--logging)
- [SDKs & Libraries](#sdks--libraries)
- [Guardrails & Security](#guardrails--security)
- [Tutorials & Case Studies](#tutorials--case-studies)
- [Communities](#communities)

---

## AI Gateways

Unified API gateways that route requests across multiple LLM providers.

### Open Source

- [LiteLLM](https://github.com/BerriAI/litellm) - Python SDK & proxy server calling 100+ LLMs in OpenAI format. Supports OpenAI, Anthropic, Azure, Bedrock, Vertex, Ollama, and more. [[40K stars]](https://github.com/BerriAI/litellm)
  - Cost tracking, budgets, rate limits, virtual keys
  - Retry/fallback logic, load balancing
  - Admin UI, streaming support
  - Integrations: Langfuse, LangSmith, Helicone, Prometheus

- [Bifrost](https://github.com/maximhq/bifrost) - High-performance AI gateway in Go. ~11µs overhead at 5K RPS. OpenAI-compatible API for 1000+ models. [[Apache 2.0]](https://github.com/maximhq/bifrost)
  - Adaptive load balancing, automatic failover
  - Semantic caching built-in
  - <3ms latency overhead
  - Enterprise governance & compliance

- [Portkey](https://github.com/Portkey-AI/portkey) - Open-source AI gateway with unified API for 1600+ LLMs. Observability, guardrails, prompt management. [[MIT]](https://github.com/Portkey-AI/portkey)
  - Tracing, metrics, cost tracking
  - Fallback routing, retries
  - MCP (Model Context Protocol) support
  - 600+ models, 50+ providers

- [Kong AI Gateway](https://github.com/Kong/kong) - Enterprise API gateway with LLM routing plugin. [[Apache 2.0]](https://github.com/Kong/kong)
  - Plugin ecosystem for auth, rate limiting
  - Load balancing algorithms
  - Enterprise security (mTLS, API key rotation)
  - 6 load balancing strategies

- [LocalAI](https://github.com/mudler/LocalAI) - Self-hosted, drop-in replacement for OpenAI API. Run LLMs locally. [[MIT]](https://github.com/mudler/LocalAI)
  - GGUF models, audio transcription, embeddings
  - OpenAI-compatible API
  - CPU and GPU support
  - Docker/k8s deployment

### Managed Services

- [Vercel AI Gateway](https://sdk.vercel.ai/docs/ai-gateway) - Single endpoint for hundreds of AI models. Built-in caching, rate limits. <20ms overhead.
  - Next.js/React integration
  - Edge deployment
  - Streaming support

- [Cloudflare AI Gateway](https://developers.cloudflare.com/ai-gateway/) - Unified interface for AI providers at the edge.
  - Caching, rate limiting
  - Analytics dashboard
  - Workers AI integration

- [OpenRouter](https://openrouter.ai/) - Unified API for 500+ models from 60+ providers.
  - Automatic provider fallbacks
  - Routing by latency, cost, or popularity
  - Simple pricing

- [SlashLLM](https://slashllm.com/) - Production-grade AI security and operations platform.
  - Guardrails, content filtering
  - Audit trails, compliance
  - Sub-300ms latency

---

## Semantic Caching

Reduce costs 60-80% by caching semantically similar responses.

### Libraries & Tools

- [RedisVL SemanticCache](https://redis.io/docs/latest/develop/ai/redisvl/0.7.0/user_guide/llmcache/) - Semantic caching built on Redis vector search. 96%+ time savings demonstrated.
  - Distance threshold configuration
  - TTL support
  - Redis Stack integration

- [GPT-Cache](https://github.com/ZhouDaoquan/GPT-Cache) - Semantic cache for LLM responses. [[MIT]](https://github.com/ZhouDaoquan/GPT-Cache)
  - Multiple embedding models
  - Redis, FAISS, Chroma backends
  - Similarity search

- [semantic-prompt-cache](https://github.com/renswickd/semantic-prompt-cache) - RAG + Semantic Cache system with FAISS. [[MIT]](https://github.com/renswickd/semantic-prompt-cache)
  - BGE embeddings
  - Configurable similarity threshold
  - Mistral/Groq integration

- [vCache](https://arxiv.org/abs/2502.03771) - Verified semantic prompt caching with adaptive thresholds.
  - User-defined error rate guarantees
  - Adaptive threshold per cached prompt
  - Academic research, production-ready

- [VectorQ](https://arxiv.org/abs/2503.05530) - Adaptive similarity thresholds for semantic caching.
  - 12x throughput improvements
  - Production benchmarks

### Vector Databases (for Semantic Cache)

- [Qdrant](https://github.com/qdrant/qdrant) - Vector similarity search engine. High performance, Rust-based. [[Apache 2.0]](https://github.com/qdrant/qdrant)
- [Pinecone](https://www.pinecone.io/) - Managed vector database. Production-ready.
- [Chroma](https://github.com/chroma-core/chroma) - Vector database for AI apps. [[MIT]](https://github.com/chroma-core/chroma)
- [pgvector](https://github.com/pgvector/pgvector) - Vector similarity in PostgreSQL. [[PostgreSQL License]](https://github.com/pgvector/pgvector)
- [FAISS](https://github.com/facebookresearch/faiss) - Facebook's vector search library. [[MIT]](https://github.com/facebookresearch/faiss)

---

## Cost Tracking & Analytics

Monitor, attribute, and optimize LLM spend.

### Open Source

- [Langfuse](https://github.com/langfuse/langfuse) - Open-source LLM engineering platform. Tracing, metrics, cost tracking. [[MIT]](https://github.com/langfuse/langfuse)
  - Self-hosted option
  - Trace-level cost breakdown
  - Prompt versioning
  - Team collaboration

- [Helicone](https://github.com/Helicone/helicone) - Open-source LLM observability platform. [[MIT]](https://github.com/Helicone/helicone)
  - Request logging, analytics
  - Prompt versioning
  - Cache analytics
  - Self-host or cloud

- [Arize Phoenix](https://github.com/Arize-ai/phoenix) - ML/LLM observability. Local-first tracing. [[Apache 2.0]](https://github.com/Arize-ai/phoenix)
  - RAG evaluation
  - LLM tracing
  - Notebook-friendly

- [Opik](https://github.com/comet-ml/opik) - LLM development platform by Comet. Tracing, evaluation, cost tracking. [[Apache 2.0]](https://github.com/comet-ml/opik)
  - Multi-provider cost tracking
  - Span-level costs
  - Evaluation framework

- [tokenmeter](https://github.com/jugaad-lab/tokenmeter) - Track AI API usage locally. Multi-provider support. [[MIT]](https://github.com/jugaad-lab/tokenmeter)
  - OpenAI, Anthropic, Azure, Google
  - Real-time cost estimates
  - 100% local, privacy-focused

- [tokentap](https://github.com/jmuncor/tokentap) - Terminal dashboard for LLM token tracking. [[MIT]](https://github.com/jmuncor/tokentap)
  - Real-time visualization
  - Claude Code integration
  - Context usage tracking

- [tokenator](https://github.com/ujjwalm29/tokenator) - Monitor LLM token usage. Drop-in SDK replacement. [[MIT]](https://github.com/ujjwalm29/tokenator)
  - SQLite storage
  - Cost analysis by period
  - Provider comparison

- [LLM Cost Guardian](https://github.com/ogulcanaydogan/LLM-Cost-Guardian) - Multi-provider cost tracking in Go. [[Apache 2.0]](https://github.com/ogulcanaydogan/LLM-Cost-Guardian)
  - Per-tenant spend limits
  - Anomaly alerts
  - Prometheus metrics

- [tokenx](https://github.com/dvlshah/tokenx) - Python decorators for cost & latency monitoring. [[MIT]](https://github.com/dvlshah/tokenx)
  - OpenAI, Anthropic, Gemini
  - Accurate cost calculation
  - Prometheus export

- [llm-performance-tracker](https://github.com/tinybirdco/llm-performance-tracker) - Multi-tenant LLM analytics dashboard. [[MIT]](https://github.com/tinybirdco/llm-performance-tracker)
  - Tinybird integration
  - Vector search
  - User-facing dashboard

### Managed Services

- [Weave (W&B)](https://weave.wandb.ai/) - LLM observability from Weights & Biases.
  - Experiment tracking
  - Cost-aware evaluation
- [Datadog LLM Observability](https://www.datadoghq.com/product/llm-observability/) - Enterprise monitoring with LLM metrics.
- [PostHog](https://posthog.com/) - Product analytics + LLM event tracking. [[MIT]](https://github.com/PostHog/posthog)

---

## Load Balancing & Routing

Distribute traffic, implement failovers, optimize costs.

### Gateways with Routing

- **Bifrost** - Adaptive load balancing based on real-time metrics. Health-aware routing with circuit breakers.
- **LiteLLM Router** - Retry/fallback logic, least-busy routing, multiple deployments.
- **Portkey** - Conditional routing, percentage-based distribution, multi-provider failover.

### Routing Patterns

- **Weighted Routing** - Distribute by weight (e.g., 70% OpenAI, 30% Anthropic)
- **Least-Connections** - Route to endpoint with fewest active requests
- **Latency-Based** - Route to fastest responding provider
- **Cost-Based** - Route to cheapest model for task complexity
- **Semantic Routing** - Route based on query type/intent

### Libraries

- [OpenRouter SDK](https://openrouter.ai/docs) - Multi-provider routing with fallbacks
- [RasA LLM Router](https://rasa.com/docs/pro/deploy/llm-routing/) - Multi-LLM routing for Rasa Pro

### Case Studies

- [Lovable: 1.8B tokens/minute load balancing](https://www.adwaitx.com/llm-provider-load-balancing-agent-workflows/) - PID-controlled dynamic load balancing

---

## API Management & Rate Limiting

Control access, prevent abuse, enforce quotas.

### Open Source

- [Kong](https://github.com/Kong/kong) - API gateway with rate limiting, auth, load balancing.
- [Zuul](https://github.com/Netflix/zuul) - Netflix's edge gateway, rate limiting, routing.
- [RateLimit4j](https://github.com/vladimir-bukhtoyarov/rate-limit) - Java rate limiting library.
- [Guava RateLimiter](https://github.com/google/guava) - Google's token bucket implementation.

### Patterns

- **RPM (Requests Per Minute)** - Standard rate limiting
- **TPM (Tokens Per Minute)** - LLM-specific, provider limits
- **Virtual Keys** - Per-customer API keys with budgets (LiteLLM, Bifrost)
- **Circuit Breakers** - Prevent cascade failures

---

## Observability & Logging

Full visibility into LLM behavior, performance, and costs.

### Tracing & Monitoring

- [OpenTelemetry](https://opentelemetry.io/) - Vendor-neutral observability. LLM instrumentations available.
- [Traceloop/OpenLLMetry](https://github.com/traceloop/openllmetry) - OpenTelemetry for LLMs. [[Apache 2.0]](https://github.com/traceloop/openllmetry)
  - LangChain, LlamaIndex, LiteLLM integration
  - Prometheus export
  - Datadog, Honeycomb backends

- [Phoenix (Arize)](https://github.com/Arize-ai/phoenix) - Local-first LLM tracing. Spans, traces, evals.

### Logging Platforms

- [Grafana](https://github.com/grafana/grafana) - Metrics visualization. Prometheus integration.
- [Loki](https://github.com/grafana/loki) - Log aggregation for LLM logs.
- [S3/GCS Logging](https://docs.litellm.ai/docs/production/logging) - LiteLLM supports logging to object storage.

### Dashboards

- [LiteLLM Admin UI](https://docs.litellm.ai/docs/production/litellm_dashboard) - Built-in spend, usage dashboards
- [Grafana Dashboard for LiteLLM](https://github.com/BerriAI/litellm/tree/main/litellm-main) - Prometheus metrics visualization

---

## SDKs & Libraries

Multi-provider abstractions and LLM client libraries.

### OpenAI-Compatible Clients

- [OpenAI Python SDK](https://github.com/openai/openai-python) - Official OpenAI client, works with any OpenAI-compatible API.
- [Anthropic Python SDK](https://github.com/anthropics/anthropic-sdk-python) - Official Claude client.
- [Vercel AI SDK](https://github.com/vercel/ai) - AI SDK for Next.js, Svelte, etc. [[MIT]](https://github.com/vercel/ai)

### Multi-Provider SDKs

- [LiteLLM Python SDK](https://docs.litellm.ai/docs/python-sdk) - Unified interface for 100+ providers.
- [Portkey Python SDK](https://docs.portkey.ai/docs/get-started/python-sdk) - Multi-provider with tracing.
- [Bifrost Go SDK](https://github.com/maximhq/bifrost) - Go client for Bifrost gateway.

### Framework Integrations

- [LangChain](https://github.com/langchain-ai/langchain) - LLM orchestration framework. 100+ integrations.
- [LlamaIndex](https://github.com/run-llama/llama_index) - RAG framework with gateway integrations.
- [CrewAI](https://github.com/crewAIInc/crewAI) - Multi-agent framework with LLM routing.
- [AutoGen](https://github.com/microsoft/autogen) - Microsoft multi-agent framework.

### Utilities

- [tiktoken](https://github.com/openai/tiktoken) - Fast tokenization. Used for token counting.
- [tokenizers](https://github.com/huggingface/tokenizers) - Hugging Face tokenizers.
- [httpx](https://github.com/encode/httpx) - Async HTTP client. Used by many LLM libraries.

---

## Guardrails & Security

Content filtering, PII redaction, prompt injection protection.

### Open Source

- [Portkey Guardrails](https://docs.portkey.ai/docs/guardrails) - Input/output filtering, PII redaction.
- [LiteLLM Guardrails](https://docs.litellm.ai/docs/production/guardrails) - Pre/post call hooks for validation.
- [PromptGuard](https://github.com/protectai/promptguard) - Prompt injection detection. [[MIT]](https://github.com/protectai/promptguard)
- [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) - NVIDIA's dialogue guardrails. [[Apache 2.0]](https://github.com/NVIDIA/NeMo-Guardrails)
- [LLM Guard](https://github.com/burkelaine/llm-guard) - Security toolkit for LLM applications. [[MIT]](https://github.com/burkelaine/llm-guard)
  - Prompt injection detection
  - Sensitive data scanning
  - Toxicity detection

### Managed Services

- [SlashLLM Guardrails](https://slashllm.com/) - Enterprise security platform.
- [Azure AI Content Safety](https://azure.microsoft.com/en-us/products/ai-services/content-safety) - Microsoft's content moderation.
- [AWS AI Services](https://aws.amazon.com/machine-learning/ai-services/) - Amazon's content moderation.

---

## Tutorials & Case Studies

### Getting Started

- [LiteLLM Quick Start](https://docs.litellm.ai/docs/)
- [Bifrost Documentation](https://getmax.im/bifrostdocs)
- [Portkey Quick Start](https://docs.portkey.ai/docs/get-started)

### Architecture Patterns

- [Building Multi-Provider LLM Infrastructure](https://medium.com/@ritukampani/future-proof-your-ai-building-a-gateway-for-multiple-llm-providers-b746f80cc169)
- [LLM Orchestration with Bifrost](https://dev.to/debmckinney/llm-orchestration-with-bifrost-routing-fallbacks-and-load-balancing-in-one-layer-40p3)
- [Failover Routing Strategies](https://portkey.ai/blog/failover-routing-strategies-for-llms-in-production)

### Cost Optimization

- [Semantic Caching Guide](https://scalemind.ai/blog/semantic-caching-llm-guide)
- [Reducing LLM Costs with Semantic Cache](https://redis.io/docs/latest/develop/ai/redisvl/0.7.0/user_guide/llmcache/)
- [Cost-Aware Routing Patterns](https://www.mindstudio.ai/blog/best-ai-model-routers-multi-provider-llm-cost/)

### Production Deployments

- [Lovable: 1.8B Tokens/Minute Load Balancing](https://www.adwaitx.com/llm-provider-load-balancing-agent-workflows/)
- [OpenRouter Multi-Provider Routing](https://dev.to/kirponik/mastering-multi-provider-routing-with-openrouter-1ce3)
- [Rasa Multi-LLM Routing](https://rasa.com/docs/pro/deploy/llm-routing/)

### Research Papers

- [vCache: Verified Semantic Prompt Caching](https://arxiv.org/abs/2502.03771)
- [VectorQ: Adaptive Semantic Caching](https://arxiv.org/abs/2503.05530)
- [Cortex: Semantic-Aware Knowledge Caching](https://arxiv.org/html/2509.17360v2)

---

## Communities

- [/r/LLMOps](https://reddit.com/r/LLMOps) - Reddit community for LLM operations
- [LangChain Discord](https://discord.gg/langchain) - Framework community
- [LiteLLM Discord](https://discord.gg/tdNkNArv) - Gateway community
- [HuggingFace Community](https://discuss.huggingface.co/) - Model & deployment discussions

---

## Contributing

Contributions welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the author has waived all copyright and related or neighboring rights to this work.
