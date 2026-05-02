# Awesome AI Gateways [![Awesome](https://awesome.re/badge-flat.svg)](https://awesome.re)

> A curated list of tools, libraries, and resources for LLM routing, orchestration, and gateway infrastructure.

Managing 100+ LLM APIs, handling rate limits, implementing fallbacks, and tracking token costs is a massive operational headache. This list curates the best open-source tools, managed services, and resources to help you build production-grade AI infrastructure.

## Contents

- [AI Gateways](#ai-gateways)
- [Semantic Caching](#semantic-caching)
- [Cost Tracking and Analytics](#cost-tracking-and-analytics)
- [Load Balancing and Routing](#load-balancing-and-routing)
- [API Management and Rate Limiting](#api-management-and-rate-limiting)
- [Observability and Logging](#observability-and-logging)
- [Agentic Orchestration](#agentic-orchestration)
- [SDKs and Libraries](#sdks-and-libraries)
- [Guardrails and Security](#guardrails-and-security)
- [Tutorials and Case Studies](#tutorials-and-case-studies)
- [Communities](#communities)
- [KubeStellar Console](https://github.com/kubestellar/console) - Multi-cluster Kubernetes dashboard with AI gateway observability, LLM request monitoring, real-time metrics, and CNCF integrations. CNCF Sandbox project.

## AI Gateways

Unified API gateways that route requests across multiple LLM providers.

### Open Source

- [LiteLLM](https://github.com/BerriAI/litellm#readme) - Python SDK and proxy server calling 100+ LLMs in OpenAI format.
- [Portkey Gateway](https://github.com/Portkey-AI/gateway#readme) - Blazing fast AI gateway with 250+ LLMs, 50+ guardrails.
- [Bifrost](https://github.com/maximhq/bifrost#readme) - High-performance AI gateway in Go with adaptive load balancing.
- [Ferro Labs AI Gateway](https://github.com/ferro-labs/ai-gateway#readme) - Go-native gateway for 29 providers with caching & guardrails.
- [Envoy AI Gateway](https://github.com/envoyproxy/ai-gateway#readme) - Unified access to GenAI services built on Envoy Gateway.
- [LLM Gateway](https://github.com/theopenco/llmgateway#readme) - Unified interface for running and managing LLMs with analytics.
- [Inference Gateway](https://github.com/inference-gateway/inference-gateway#readme) - Cloud-native gateway unifying multiple LLM providers.
- [OpenGateLLM](https://github.com/etalab-ia/OpenGateLLM#readme) - Open-source API gateway focused on self-hosted LLMs.
- [Routerly](https://github.com/Inebrio/Routerly#readme) - Self-hosted LLM gateway with intelligent multi-policy routing.
- [Plexus](https://github.com/mcowger/plexus#readme) - Unified API gateway with OAuth auth, quota tracking, and 15+ providers.
- [OpenZiti LLM Gateway](https://github.com/openziti/llm-gateway#readme) - Zero-trust LLM gateway with semantic routing and E2E encryption.
- [Kong](https://github.com/Kong/kong#readme) - Enterprise API gateway with LLM routing plugin.
- [LocalAI](https://github.com/mudler/LocalAI#readme) - Self-hosted, drop-in replacement for OpenAI API.
- [lm-proxy](https://github.com/Nayjest/lm-proxy#readme) - Lightweight OpenAI-compatible proxy for multi-provider inference.
- [LLM API Proxy](https://github.com/rxliuli/llm-api-proxy#readme) - Edge runtime proxy supporting OpenAI, Anthropic, Gemini, and more.
- [LLMProxy](https://github.com/aiyuekuang/LLMProxy#readme) - High-performance reverse proxy for LLM inference with SSE streaming.
- [Zuul](https://github.com/Netflix/zuul#readme) - Netflix edge gateway.

### Managed Services

- [Vercel AI Gateway](https://sdk.vercel.ai/docs/ai-gateway#readme) - Single endpoint for hundreds of AI models.
- [Cloudflare AI Gateway](https://developers.cloudflare.com/ai-gateway/#readme) - Unified interface for AI providers at the edge.
- [OpenRouter](https://openrouter.ai/#readme) - Unified API for 500+ models from 60+ providers.
- [Portkey Hosted](https://portkey.ai/#readme) - Managed AI gateway with 1600+ LLMs and enterprise features.
- [Braintrust](https://www.braintrust.dev/#readme) - Unified API with encrypted caching and integrated evaluation.
- [Inworld Router](https://www.inworlds.ai/#readme) - LLM plus TTS pipelining for high-interactivity use cases.
- [Maxim AI](https://www.getmaxim.ai/#readme) - End-to-end platform for simulation, evaluation, and monitoring.

## Semantic Caching

Reduce costs 60-80% by caching semantically similar responses.

- [RedisVL SemanticCache](https://redis.io/docs/latest/develop/ai/redisvl/0.7.0/user_guide/llmcache/#readme) - Semantic caching built on Redis vector search.
- [GPT-Cache](https://github.com/ZhouDaoquan/GPT-Cache#readme) - Semantic cache for LLM responses.
- [semantic-prompt-cache](https://github.com/renswickd/semantic-prompt-cache#readme) - RAG plus Semantic Cache system with FAISS.
- [vCache](https://arxiv.org/abs/2502.03771#readme) - Verified semantic prompt caching with adaptive thresholds.
- [VectorQ](https://arxiv.org/abs/2503.05530#readme) - Adaptive similarity thresholds for semantic caching.
- [Qdrant](https://github.com/qdrant/qdrant#readme) - Vector similarity search engine.
- [Pinecone](https://www.pinecone.io/#readme) - Managed vector database.
- [Chroma](https://github.com/chroma-core/chroma#readme) - Vector database for AI apps.
- [pgvector](https://github.com/pgvector/pgvector#readme) - Vector similarity in PostgreSQL.
- [FAISS](https://github.com/facebookresearch/faiss#readme) - Facebook vector search library.

## Cost Tracking and Analytics

Monitor, attribute, and optimize LLM spend.

- [Langfuse](https://github.com/langfuse/langfuse#readme) - Open-source LLM engineering platform.
- [Helicone](https://github.com/Helicone/helicone#readme) - Open-source LLM observability platform.
- [Arize Phoenix](https://github.com/Arize-ai/phoenix#readme) - ML and LLM observability platform.
- [Opik](https://github.com/comet-ml/opik#readme) - LLM development platform by Comet.
- [tokenmeter](https://github.com/jugaad-lab/tokenmeter#readme) - Track AI API usage locally.
- [tokentap](https://github.com/jmuncor/tokentap#readme) - Terminal dashboard for LLM token tracking.
- [tokenator](https://github.com/ujjwalm29/tokenator#readme) - Monitor LLM token usage.
- [LLM Cost Guardian](https://github.com/ogulcanaydogan/LLM-Cost-Guardian#readme) - Multi-provider cost tracking in Go.
- [tokenx](https://github.com/dvlshah/tokenx#readme) - Python decorators for cost and latency monitoring.
- [llm-performance-tracker](https://github.com/tinybirdco/llm-performance-tracker#readme) - Multi-tenant LLM analytics dashboard.
- [Weave](https://weave.wandb.ai/#readme) - LLM observability from Weights and Biases.
- [Datadog LLM Observability](https://www.datadoghq.com/product/llm-observability/#readme) - Enterprise monitoring with LLM metrics.
- [PostHog](https://posthog.com/#readme) - Product analytics with LLM event tracking.
- [Confident AI](https://www.confident-ai.com/#readme) - Evaluation-first observability platform.
- [Maxim AI](https://www.getmaxim.ai/#readme) - End-to-end platform for simulation, evaluation, and monitoring.

## Load Balancing and Routing

Distribute traffic, implement failovers, and optimize costs.

- [LiteLLM Router](https://docs.litellm.ai/docs/proxy/routing#readme) - Retry/fallback logic and least-busy routing.
- [Portkey](https://portkey.ai/docs/routing-strategies#readme) - Conditional routing and percentage-based distribution.
- [Bifrost Load Balancing](https://www.getmaxim.ai/bifrostdocs#readme) - Adaptive load balancer with cluster mode.
- [Ferro Labs Router](https://github.com/ferro-labs/ai-gateway#readme) - Multi-provider routing with 29 providers.
- [Routerly Policies](https://www.routerly.ai/#readme) - 9 configurable policies including LLM-native routing.
- [Lovable: 1.8B tokens per minute load balancing](https://www.adwaitx.com/llm-provider-load-balancing-agent-workflows/#readme) - PID-controlled dynamic load balancing.

## API Management and Rate Limiting

Control access, prevent abuse, and enforce quotas.

- [RateLimit4j](https://github.com/vladimir-bukhtoyarov/rate-limit#readme) - Java rate limiting library.
- [Guava RateLimiter](https://github.com/google/guava#readme) - Google token bucket implementation.

## Observability and Logging

Full visibility into LLM behavior, performance, and costs.

- [OpenTelemetry](https://opentelemetry.io/#readme) - Vendor-neutral observability framework.
- [Traceloop OpenLLMetry](https://github.com/traceloop/openllmetry#readme) - OpenTelemetry for LLMs.
- [Grafana](https://github.com/grafana/grafana#readme) - Metrics visualization.
- [Loki](https://github.com/grafana/loki#readme) - Log aggregation for LLM logs.
- [LiteLLM Logging](https://docs.litellm.ai/docs/production/logging#readme) - Logging to object storage.
- [LiteLLM Admin UI](https://docs.litellm.ai/docs/production/litellm_dashboard#readme) - Built-in spend and usage dashboards.
- [LiteLLM Grafana Dashboard](https://github.com/BerriAI/litellm/tree/main/litellm-main#readme) - Prometheus metrics visualization.
- [AgentOps](https://www.agentops.ai/#readme) - Observability for agentic loops with tool usage tracking.

## Agentic Orchestration

Build and manage autonomous agents, long-running tasks, and multi-agent coordination.

- [LangGraph](https://github.com/langchain-ai/langgraph#readme) - Low-level orchestration framework for building stateful, multi-agent applications.
- [Agency Swarm](https://github.com/vrsen/agency-swarm#readme) - Multi-agent framework building collaborative networks of AI agents.
- [CrewAI](https://github.com/crewAIInc/crewAI#readme) - Multi-agent framework with LLM routing.
- [AutoGen](https://github.com/microsoft/autogen#readme) - Microsoft multi-agent framework.
- [UiPath Maestro](https://www.uipath.com/#readme) - Enterprise orchestrator blending LLM agents with RPA and human-in-the-loop.

## SDKs and Libraries

Multi-provider abstractions and LLM client libraries.

- [OpenAI Python SDK](https://github.com/openai/openai-python#readme) - Official OpenAI client.
- [Anthropic Python SDK](https://github.com/anthropics/anthropic-sdk-python#readme) - Official Claude client.
- [Vercel AI SDK](https://github.com/vercel/ai#readme) - AI SDK for Next.js and Svelte.
- [LiteLLM Python SDK](https://docs.litellm.ai/docs/python-sdk#readme) - Unified interface for 100+ providers.
- [Portkey Python SDK](https://docs.portkey.ai/docs/get-started/python-sdk#readme) - Multi-provider with tracing.
- [LangChain](https://github.com/langchain-ai/langchain#readme) - LLM orchestration framework.
- [LlamaIndex](https://github.com/run-llama/llama_index#readme) - RAG framework with gateway integrations.
- [tiktoken](https://github.com/openai/tiktoken#readme) - Fast tokenization by OpenAI.
- [tokenizers](https://github.com/huggingface/tokenizers#readme) - Hugging Face tokenizers.
- [httpx](https://github.com/encode/httpx#readme) - Async HTTP client.
- [Ferro Labs Go SDK](https://github.com/ferro-labs/ai-gateway#readme) - Go SDK for Ferro Labs gateway.

## Guardrails and Security

Content filtering, PII redaction, and prompt injection protection.

- [Portkey Guardrails](https://docs.portkey.ai/docs/guardrails#readme) - Input and output filtering.
- [LiteLLM Guardrails](https://docs.litellm.ai/docs/production/guardrails#readme) - Pre and post call hooks.
- [Ferro Labs Guardrails](https://github.com/ferro-labs/ai-gateway#readme) - Word/phrase filtering and token limits.
- [PromptGuard](https://github.com/protectai/promptguard#readme) - Prompt injection detection.
- [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails#readme) - NVIDIA dialogue guardrails.
- [LLM Guard](https://github.com/burkelaine/llm-guard#readme) - Security toolkit for LLM applications.
- [SlashLLM](https://slashllm.com/#readme) - Enterprise security platform.
- [Azure AI Content Safety](https://azure.microsoft.com/en-us/products/ai-services/content-safety/#readme) - Microsoft content moderation.
- [AWS AI Services](https://aws.amazon.com/machine-learning/ai-services/#readme) - Amazon content moderation.
- [DeepEval](https://github.com/confident-ai/deepeval#readme) - Open-source testing framework for LLM outputs.
- [OpenZiti Security](https://github.com/openziti/llm-gateway#readme) - Zero-trust access with E2E encryption.

## Tutorials and Case Studies

- [LiteLLM Quick Start](https://docs.litellm.ai/docs/#readme) - Official LiteLLM documentation.
- [Bifrost Documentation](https://getmaxim.ai/bifrostdocs#readme) - Bifrost setup guide.
- [Portkey Quick Start](https://docs.portkey.ai/docs/get-started#readme) - Portkey getting started guide.
- [Building Multi-Provider LLM Infrastructure](https://medium.com/@ritukampani/future-proof-your-ai-building-a-gateway-for-multiple-llm-providers-b746f80cc169#readme) - Architecture guide.
- [LLM Orchestration with Bifrost](https://dev.to/debmckinney/llm-orchestration-with-bifrost-routing-fallbacks-and-load-balancing-in-one-layer-40p3#readme) - Implementation guide.
- [Failover Routing Strategies](https://portkey.ai/blog/failover-routing-strategies-for-llms-in-production#readme) - Production patterns.
- [Semantic Caching Guide](https://scalemind.ai/blog/semantic-caching-llm-guide#readme) - Implementation best practices.
- [Cost-Aware Routing Patterns](https://www.mindstudio.ai/blog/best-ai-model-routers-multi-provider-llm-cost/#readme) - Routing strategies.
- [OpenRouter Multi-Provider Routing](https://dev.to/kirponik/mastering-multi-provider-routing-with-openrouter-1ce3#readme) - OpenRouter guide.
- [Rasa Multi-LLM Routing](https://rasa.com/docs/production/llm-routing/#readme) - Rasa routing documentation.
- [Cortex](https://arxiv.org/html/2509.17360v2#readme) - Semantic-aware knowledge caching for LLM agents.
- [Ferro Labs Getting Started](https://github.com/ferro-labs/ai-gateway#readme) - Go-native gateway setup.
- [Routerly Documentation](https://www.routerly.ai/#readme) - Intelligent routing guide.

## Communities

- [/r/LLMOps](https://reddit.com/r/LLMOps#readme) - Reddit community for LLM operations.
- [LangChain Discord](https://discord.gg/langchain#readme) - Framework community.
- [LiteLLM Discord](https://discord.gg/tdNkNArv#readme) - Gateway community.
- [Hugging Face Community](https://discuss.huggingface.co/#readme) - Model and deployment discussions.

## Related Awesome Lists

- [rothgar/awesome-tuis](https://github.com/rothgar/awesome-tuis) - 18K+ stars, comprehensive TUI list.
- [msmps/awesome-opentui](https://github.com/msmps/awesome-opentui) - Curated open TUI resources.
