# Awesome AI Gateways

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

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

- [LiteLLM](https://github.com/BerriAI/litellm#readme) - Python SDK and proxy server calling 100+ LLMs in OpenAI format.
- [Bifrost](https://github.com/maximhq/bifrost#readme) - High-performance AI gateway in Go.
- [Portkey](https://github.com/Portkey-AI/portkey#readme) - Open-source AI gateway with unified API for 1600+ LLMs.
- [Kong](https://github.com/Kong/kong#readme) - Enterprise API gateway with LLM routing plugin.
- [LocalAI](https://github.com/mudler/LocalAI#readme) - Self-hosted, drop-in replacement for OpenAI API.

### Managed Services

- [Vercel AI Gateway](https://sdk.vercel.ai/docs/ai-gateway#readme) - Single endpoint for hundreds of AI models.
- [Cloudflare AI Gateway](https://developers.cloudflare.com/ai-gateway/#readme) - Unified interface for AI providers at the edge.
- [OpenRouter](https://openrouter.ai/#readme) - Unified API for 500+ models from 60+ providers.
- [SlashLLM](https://slashllm.com/#readme) - Production-grade AI security and operations platform.

---

## Semantic Caching

Reduce costs 60-80% by caching semantically similar responses.

### Libraries & Tools

- [RedisVL SemanticCache](https://redis.io/docs/latest/develop/ai/redisvl/0.7.0/user_guide/llmcache/#readme) - Semantic caching built on Redis vector search.
- [GPT-Cache](https://github.com/ZhouDaoquan/GPT-Cache#readme) - Semantic cache for LLM responses.
- [semantic-prompt-cache](https://github.com/renswickd/semantic-prompt-cache#readme) - RAG plus Semantic Cache system with FAISS.
- [vCache](https://arxiv.org/abs/2502.03771#readme) - Verified semantic prompt caching with adaptive thresholds.
- [VectorQ](https://arxiv.org/abs/2503.05530#readme) - Adaptive similarity thresholds for semantic caching.

### Vector Databases (for Semantic Cache)

- [Qdrant](https://github.com/qdrant/qdrant#readme) - Vector similarity search engine.
- [Pinecone](https://www.pinecone.io/#readme) - Managed vector database.
- [Chroma](https://github.com/chroma-core/chroma#readme) - Vector database for AI apps.
- [pgvector](https://github.com/pgvector/pgvector#readme) - Vector similarity in PostgreSQL.
- [FAISS](https://github.com/facebookresearch/faiss#readme) - Facebook's vector search library.

---

## Cost Tracking & Analytics

Monitor, attribute, and optimize LLM spend.

### Open Source

- [Langfuse](https://github.com/langfuse/langfuse#readme) - Open-source LLM engineering platform.
- [Helicone](https://github.com/Helicone/helicone#readme) - Open-source LLM observability platform.
- [Arize Phoenix](https://github.com/Arize-ai/phoenix#readme) - ML/LLM observability platform.
- [Opik](https://github.com/comet-ml/opik#readme) - LLM development platform by Comet.
- [tokenmeter](https://github.com/jugaad-lab/tokenmeter#readme) - Track AI API usage locally.
- [tokentap](https://github.com/jmuncor/tokentap#readme) - Terminal dashboard for LLM token tracking.
- [tokenator](https://github.com/ujjwalm29/tokenator#readme) - Monitor LLM token usage.
- [LLM Cost Guardian](https://github.com/ogulcanaydogan/LLM-Cost-Guardian#readme) - Multi-provider cost tracking in Go.
- [tokenx](https://github.com/dvlshah/tokenx#readme) - Python decorators for cost and latency monitoring.
- [llm-performance-tracker](https://github.com/tinybirdco/llm-performance-tracker#readme) - Multi-tenant LLM analytics dashboard.

### Managed Services

- [Weave](https://weave.wandb.ai/#readme) - LLM observability from Weights and Biases.
- [Datadog LLM Observability](https://www.datadoghq.com/product/llm-observability/#readme) - Enterprise monitoring with LLM metrics.
- [PostHog](https://posthog.com/#readme) - Product analytics with LLM event tracking.

---

## Load Balancing & Routing

Distribute traffic, implement failovers, and optimize costs.

### Gateways with Routing

- [Bifrost](https://github.com/maximhq/bifrost#readme) - Adaptive load balancing based on real-time metrics.
- [LiteLLM Router](https://docs.litellm.ai/docs/proxy/routing#readme) - Retry/fallback logic and least-busy routing.
- [Portkey](https://portkey.ai/docs/routing-strategies#readme) - Conditional routing and percentage-based distribution.

### Routing Patterns

- **Weighted Routing** - Distribute by weight (for example, 70% OpenAI, 30% Anthropic).
- **Least-Connections** - Route to endpoint with fewest active requests.
- **Latency-Based** - Route to fastest responding provider.
- **Cost-Based** - Route to cheapest model for task complexity.
- **Semantic Routing** - Route based on query type or intent.

### Case Studies

- [Lovable: 1.8B tokens per minute load balancing](https://www.adwaitx.com/llm-provider-load-balancing-agent-workflows/#readme) - PID-controlled dynamic load balancing.

---

## API Management & Rate Limiting

Control access, prevent abuse, and enforce quotas.

### Open Source

- [Kong](https://github.com/Kong/kong#readme) - API gateway with rate limiting and auth.
- [Zuul](https://github.com/Netflix/zuul#readme) - Netflix's edge gateway.
- [RateLimit4j](https://github.com/vladimir-bukhtoyarov/rate-limit#readme) - Java rate limiting library.
- [Guava RateLimiter](https://github.com/google/guava#readme) - Google's token bucket implementation.

### Patterns

- **RPM (Requests Per Minute)** - Standard rate limiting.
- **TPM (Tokens Per Minute)** - LLM-specific provider limits.
- **Virtual Keys** - Per-customer API keys with budgets (LiteLLM, Bifrost).
- **Circuit Breakers** - Prevent cascade failures.

---

## Observability & Logging

Full visibility into LLM behavior, performance, and costs.

### Tracing & Monitoring

- [OpenTelemetry](https://opentelemetry.io/#readme) - Vendor-neutral observability framework.
- [Traceloop OpenLLMetry](https://github.com/traceloop/openllmetry#readme) - OpenTelemetry for LLMs.
- [Arize Phoenix](https://github.com/Arize-ai/phoenix#readme) - Local-first LLM tracing platform.

### Logging Platforms

- [Grafana](https://github.com/grafana/grafana#readme) - Metrics visualization.
- [Loki](https://github.com/grafana/loki#readme) - Log aggregation for LLM logs.
- [LiteLLM Logging](https://docs.litellm.ai/docs/production/logging#readme) - Logging to object storage.

### Dashboards

- [LiteLLM Admin UI](https://docs.litellm.ai/docs/production/litellm_dashboard#readme) - Built-in spend and usage dashboards.
- [LiteLLM Grafana Dashboard](https://github.com/BerriAI/litellm/tree/main/litellm-main#readme) - Prometheus metrics visualization.

---

## SDKs & Libraries

Multi-provider abstractions and LLM client libraries.

### OpenAI-Compatible Clients

- [OpenAI Python SDK](https://github.com/openai/openai-python#readme) - Official OpenAI client.
- [Anthropic Python SDK](https://github.com/anthropics/anthropic-sdk-python#readme) - Official Claude client.
- [Vercel AI SDK](https://github.com/vercel/ai#readme) - AI SDK for Next.js and Svelte.

### Multi-Provider SDKs

- [LiteLLM Python SDK](https://docs.litellm.ai/docs/python-sdk#readme) - Unified interface for 100+ providers.
- [Portkey Python SDK](https://docs.portkey.ai/docs/get-started/python-sdk#readme) - Multi-provider with tracing.
- [Bifrost Go SDK](https://github.com/maximhq/bifrost#readme) - Go client for Bifrost gateway.

### Framework Integrations

- [LangChain](https://github.com/langchain-ai/langchain#readme) - LLM orchestration framework.
- [LlamaIndex](https://github.com/run-llama/llama_index#readme) - RAG framework with gateway integrations.
- [CrewAI](https://github.com/crewAIInc/crewAI#readme) - Multi-agent framework with LLM routing.
- [AutoGen](https://github.com/microsoft/autogen#readme) - Microsoft multi-agent framework.

### Utilities

- [tiktoken](https://github.com/openai/tiktoken#readme) - Fast tokenization by OpenAI.
- [tokenizers](https://github.com/huggingface/tokenizers#readme) - Hugging Face tokenizers.
- [httpx](https://github.com/encode/httpx#readme) - Async HTTP client.

---

## Guardrails & Security

Content filtering, PII redaction, and prompt injection protection.

### Open Source

- [Portkey Guardrails](https://docs.portkey.ai/docs/guardrails#readme) - Input and output filtering.
- [LiteLLM Guardrails](https://docs.litellm.ai/docs/production/guardrails#readme) - Pre and post call hooks.
- [PromptGuard](https://github.com/protectai/promptguard#readme) - Prompt injection detection.
- [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails#readme) - NVIDIA's dialogue guardrails.
- [LLM Guard](https://github.com/burkelaine/llm-guard#readme) - Security toolkit for LLM applications.

### Managed Services

- [SlashLLM Guardrails](https://slashllm.com/#readme) - Enterprise security platform.
- [Azure AI Content Safety](https://azure.microsoft.com/en-us/products/ai-services/content-safety/#readme) - Microsoft's content moderation.
- [AWS AI Services](https://aws.amazon.com/machine-learning/ai-services/#readme) - Amazon's content moderation.

---

## Tutorials & Case Studies

### Getting Started

- [LiteLLM Quick Start](https://docs.litellm.ai/docs/#readme) - Official LiteLLM documentation.
- [Bifrost Documentation](https://getmax.im/bifrostdocs#readme) - Bifrost setup guide.
- [Portkey Quick Start](https://docs.portkey.ai/docs/get-started#readme) - Portkey getting started guide.

### Architecture Patterns

- [Building Multi-Provider LLM Infrastructure](https://medium.com/@ritukampani/future-proof-your-ai-building-a-gateway-for-multiple-llm-providers-b746f80cc169#readme) - Architecture guide.
- [LLM Orchestration with Bifrost](https://dev.to/debmckinney/llm-orchestration-with-bifrost-routing-fallbacks-and-load-balancing-in-one-layer-40p3#readme) - Implementation guide.
- [Failover Routing Strategies](https://portkey.ai/blog/failover-routing-strategies-for-llms-in-production#readme) - Production patterns.

### Cost Optimization

- [Semantic Caching Guide](https://scalemind.ai/blog/semantic-caching-llm-guide#readme) - Implementation best practices.
- [Reducing LLM Costs with Semantic Cache](https://redis.io/docs/latest/develop/ai/redisvl/0.7.0/user_guide/llmcache/#readme) - Redis semantic caching.
- [Cost-Aware Routing Patterns](https://www.mindstudio.ai/blog/best-ai-model-routers-multi-provider-llm-cost/#readme) - Routing strategies.

### Production Deployments

- [Lovable: 1.8B Tokens per Minute Load Balancing](https://www.adwaitx.com/llm-provider-load-balancing-agent-workflows/#readme) - Case study.
- [OpenRouter Multi-Provider Routing](https://dev.to/kirponik/mastering-multi-provider-routing-with-openrouter-1ce3#readme) - OpenRouter guide.
- [Rasa Multi-LLM Routing](https://rasa.com/docs/pro/deploy/llm-routing/#readme) - Rasa routing documentation.

### Research Papers

- [vCache: Verified Semantic Prompt Caching](https://arxiv.org/abs/2502.03771#readme) - Academic paper.
- [VectorQ: Adaptive Semantic Caching](https://arxiv.org/abs/2503.05530#readme) - Academic paper.
- [Cortex: Semantic-Aware Knowledge Caching](https://arxiv.org/html/2509.17360v2#readme) - Academic paper.

---

## Communities

- [/r/LLMOps](https://reddit.com/r/LLMOps#readme) - Reddit community for LLM operations.
- [LangChain Discord](https://discord.gg/langchain#readme) - Framework community.
- [LiteLLM Discord](https://discord.gg/tdNkNArv#readme) - Gateway community.
- [HuggingFace Community](https://discuss.huggingface.co/#readme) - Model and deployment discussions.

---

## Contributing

Contributions welcome! Please read [CONTRIBUTING.md](CONTRIBUTING.md#readme) for guidelines.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the author has waived all copyright and related or neighboring rights to this work.
