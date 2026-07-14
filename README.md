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

## AI Gateways

Unified API gateways that route requests across multiple LLM providers.

### Open Source
• [APISIX AI Plugin](https://apisix.apache.org/docs/apisix/plugins/ai-proxy/) - Apache APISIX plugin for LLM provider integration with load balancing and observability.
• [Ambassador AI Gateway](https://www.getambassador.io/docs/edge-stack/latest/topics/using/ai/) - Kubernetes-native AI gateway built on Envoy with rate limiting and fallback.

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
- [LocalGateway](https://github.com/Correctover/local-gateway#readme) - Desktop LLM gateway with zero-dependency multi-provider failover and automatic model name mapping. Works with Cursor, Claude Desktop, Windsurf.
- [lm-proxy](https://github.com/Nayjest/lm-proxy#readme) - Lightweight OpenAI-compatible proxy for multi-provider inference.
- [LLM API Proxy](https://github.com/rxliuli/llm-api-proxy#readme) - Edge runtime proxy supporting OpenAI, Anthropic, Gemini, and more.
- [LLMProxy](https://github.com/aiyuekuang/LLMProxy#readme) - High-performance reverse proxy for LLM inference with SSE streaming.
- [Zuul](https://github.com/Netflix/zuul#readme) - Netflix edge gateway.
- [RouteLLM](https://github.com/lm-sys/RouteLLM#readme) - Open-source framework from LMSYS for training and deploying lightweight LLM routers that balance cost and quality.
- [ClawRouter](https://github.com/BlockRunAI/ClawRouter#readme) - Agent-native LLM router with 41+ models, sub-millisecond routing, and USDC payments.
- [NadirClaw](https://github.com/NadirRouter/NadirClaw#readme) - Self-hosted LLM router that routes simple prompts to cheap models and complex to premium, saving 40-70% on costs.
- [Olla](https://github.com/thushan/olla#readme) - High-performance lightweight Go proxy and load balancer for LLM infrastructure with intelligent routing.
- [BitRouter](https://github.com/bitrouter/bitrouter#readme) - Rust-based agentic LLM gateway and router for cost-optimizing agentic workflows.
- [Nyro](https://github.com/nyroway/nyro#readme) - Self-hosted Rust AI gateway with protocol translation for Claude Code, Codex, and Gemini CLI.
- [1Flowbase](https://github.com/taichuy/1flowbase#readme) - Rust AI gateway for fusion-style multi-model workflows published as OpenAI-compatible virtual models.
- [SmarterRouter](https://github.com/peva3/SmarterRouter#readme) - VRAM-aware router for Ollama and llama.cpp with semantic caching, model profiling, and automatic failover.
- [Llamactl](https://github.com/lordmathis/llamactl#readme) - Unified management and routing for llama.cpp, MLX, and vLLM models with web dashboard.
- [Nexus Gateway](https://github.com/AlphaBitCore/nexus-gateway#readme) - Enterprise AI traffic gateway with compliance, routing across 20+ providers, semantic cache, quotas, and audit.
- [AI Firewall](https://github.com/vcal-project/ai-firewall#readme) - Rust OpenAI-compatible gateway using Redis exact cache and Qdrant semantic cache.
- [Hecate](https://github.com/hecatehq/hecate#readme) - Local AI operations console for supervised agent work with MCP and OpenTelemetry.
- [Alvus](https://github.com/filariasistrichoglossusmoluccanus49/Alvus#readme) - Lightweight Go proxy for handling AI API rate limits.

### Managed Services
• [AWS API Gateway with Bedrock Integration](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-bedrock.html) - Expose Bedrock models via REST/WebSocket APIs with throttling and auth.
• [GCP Apigee AI Gateway](https://cloud.google.com/apigee/docs/api-platform/get-started) - Manage and secure LLM APIs with Apigee's traffic management and analytics.

- [Cloudflare AI Gateway](https://developers.cloudflare.com/ai-gateway/#readme) - Unified interface for AI providers at the edge.
- [OpenRouter](https://openrouter.ai/#readme) - Unified API for 500+ models from 60+ providers.
- [Portkey Hosted](https://portkey.ai/#readme) - Managed AI gateway with 1600+ LLMs and enterprise features.
- [Braintrust](https://www.braintrust.dev/#readme) - Unified API with encrypted caching and integrated evaluation.
- [Maxim AI](https://www.getmaxim.ai/#readme) - End-to-end platform for simulation, evaluation, and monitoring.
- [Together AI](https://www.together.ai/#readme) - Cloud platform for 200+ open-source models with optimized inference.
- [Fireworks AI](https://fireworks.ai/#readme) - Fast inference platform optimized for latency and throughput.
- [DeepInfra](https://deepinfra.com/#readme) - Serverless GPU inference for open-source LLMs.
- [Replicate](https://replicate.com/#readme) - Cloud platform for running and fine-tuning open-source models.
- [Anyscale](https://www.anyscale.com/#readme) - AI platform built on Ray for scaling LLM applications.

## Semantic Caching
• [Elasticsearch Semantic Cache](https://www.elastic.co/guide/en/elasticsearch/reference/current/semantic-search.html) - Use Elasticsearch for semantic caching with dense vector search.
• [Weaviate](https://weaviate.io/) - Open-source vector database for storing and querying AI embeddings with hybrid search capabilities.

Reduce costs 60-80% by caching semantically similar responses.

- [RedisVL SemanticCache](https://redis.io/docs/latest/develop/ai/redisvl/0.7.0/user_guide/llmcache/#readme) - Semantic caching built on Redis vector search.
- [semantic-prompt-cache](https://github.com/renswickd/semantic-prompt-cache#readme) - RAG plus Semantic Cache system with FAISS.
- [vCache](https://arxiv.org/abs/2502.03771#readme) - Verified semantic prompt caching with adaptive thresholds.
- [VectorQ](https://arxiv.org/abs/2503.05530#readme) - Adaptive similarity thresholds for semantic caching.
- [Qdrant](https://github.com/qdrant/qdrant#readme) - Vector similarity search engine.
- [Pinecone](https://www.pinecone.io/#readme) - Managed vector database.
- [Chroma](https://github.com/chroma-core/chroma#readme) - Vector database for AI apps.
- [pgvector](https://github.com/pgvector/pgvector#readme) - Vector similarity in PostgreSQL.
- [FAISS](https://github.com/facebookresearch/faiss#readme) - Facebook vector search library.
- [ModelCache](https://github.com/codefuse-ai/ModelCache#readme) - LLM semantic caching system for reducing response time via cached query-result pairs.
- [Mimir](https://github.com/aqstack/mimir#readme) - Go drop-in proxy that caches LLM API responses using semantic similarity.
- [Semcache](https://github.com/sensoris/semcache#readme) - Rust semantic caching layer for LLM applications.
- [OmniCache](https://github.com/ashishpatel26/omnicache-ai#readme) - Unified multi-layer caching library for AI and agent pipelines.
- [Graft](https://github.com/AEndrix03/Graft#readme) - Local-first semantic cache for AI agents with cross-session memory via MCP.

## Cost Tracking and Analytics
• [Kubecost](https://kubecost.com/) - Cost monitoring for Kubernetes workloads, adaptable for LLM costs.
• [AWS Cost Explorer with AI Insights](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/) - AI-driven cost anomaly detection and forecasting.
• [OpenCost](https://opencost.io/) - Open-source cost monitoring for cloud-native workloads, can be adapted for LLM costs.
• [Cloudability](https://www.cloudability.com/) - Cloud cost management platform with AI-driven insights.
• [OpenLLMetry](https://github.com/traceloop/openllmetry) - OpenTelemetry instrumentation for LLM applications.

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
- [Coze Loop](https://github.com/coze-dev/coze-loop#readme) - Next-gen AI agent optimization platform with full-lifecycle management.
- [Pydantic Logfire](https://github.com/pydantic/logfire#readme) - AI observability platform for production LLM and agent systems.
- [Agenta](https://github.com/Agenta-AI/agenta#readme) - Open-source LLMOps platform with prompt playground, management, evaluation, and observability.
- [Latitude](https://github.com/latitude-dev/latitude-llm#readme) - Open-source AI monitoring platform.
- [Acontext](https://github.com/memodb-io/Acontext#readme) - Agent skills as a memory layer for context engineering.
- [Laminar](https://github.com/lmnr-ai/lmnr#readme) - Open-source observability platform purpose-built for AI agents.
- [Judgeval](https://github.com/JudgmentLabs/judgeval#readme) - Continuous-improvement stack for agents with environment data and evals.
- [TraceRoot](https://github.com/traceroot-ai/traceroot#readme) - Open-source observability and self-healing layer for AI agents.
- [Agent Prism](https://github.com/evilmartians/agent-prism#readme) - React components for visualizing traces from AI agents.
- [Aegis](https://github.com/Justin0504/Aegis#readme) - Runtime policy enforcement for AI agents with cryptographic audit trail and kill switch.
- [AgentWatch](https://github.com/cyberark/agentwatch#readme) - AI observability framework for comprehensive agent interaction insights.
- [VoltAgent](https://github.com/VoltAgent/voltagent#readme) - AI Agent Engineering Platform built on open-source TypeScript framework.

## Load Balancing and Routing
• [Istio AI Traffic Management](https://istio.io/latest/docs/tasks/traffic-management/) - AI-based traffic routing in Istio service mesh.

Distribute traffic, implement failovers, and optimize costs.

- [LiteLLM Router](https://docs.litellm.ai/docs/proxy/load_balancing#readme) - Retry/fallback logic and least-busy routing.
- [Portkey](https://portkey.ai/docs#readme) - Conditional routing and percentage-based distribution.
- [Bifrost Load Balancing](https://github.com/maximhq/bifrost#readme) - Adaptive load balancer with cluster mode.
- [Ferro Labs Router](https://github.com/ferro-labs/ai-gateway#readme) - Multi-provider routing with 29 providers.
- [Routerly Policies](https://www.routerly.ai/#readme) - 9 configurable policies including LLM-native routing.
- [RouteLLM](https://github.com/lm-sys/RouteLLM#readme) - Cost-quality routing with trainable lightweight routers.
- [vLLM Semantic Router](https://github.com/vllm-project/semantic-router#readme) - System-level intelligent router for Mixture-of-Models at cloud, data center, and edge.
- [NVIDIA LLM Router](https://github.com/NVIDIA-AI-Blueprints/llm-router#readme) - Route LLM requests to the best model for the task at hand.
- [Dario](https://github.com/askalf/dario#readme) - Claude Pro/Max subscription proxy for any tool at subscription pricing.
- [RouterArena](https://github.com/RouteWorks/RouterArena#readme) - Open framework for evaluating LLM routers with standardized datasets, metrics, and live leaderboard.
- [Infermux](https://github.com/greynewell/infermux#readme) - Go-based inference routing across providers with load balancing and cost tracking.
- [FreeRouter](https://github.com/openfreerouter/freerouter#readme) - Self-hosted AI model router with 14-dimension classifier. OpenRouter alternative using your own API keys.
- [Claude Model Router Hook](https://github.com/tzachbon/claude-model-router-hook#readme) - Claude Code hooks that auto-switch model tier based on task complexity.
- [a3m Router](https://github.com/Das-rebel/a3m-router#readme) - Top-ranked router on RouterArena with 96.77% accuracy at $0.0768/1K tokens.

## API Management and Rate Limiting
• [Apigee API Hub with AI Recommendations](https://cloud.google.com/apigee/docs/api-hub/what-is-api-hub) - Discover and recommend APIs using AI-powered insights.
• [Apigee AI-powered API Management](https://cloud.google.com/apigee/docs/api-platform/get-started) - Google Cloud's Apigee with AI for intelligent API lifecycle management.
• [Tyk AI Gateway](https://tyk.io/blog/ai-gateway/) - Open-source API gateway with AI-specific rate limiting, token quotas, and prompt guardrails.

Control access, prevent abuse, and enforce quotas.

- [Guava RateLimiter](https://github.com/google/guava#readme) - Google token bucket implementation.
- [Resilience4j RateLimiter](https://github.com/resilience4j/resilience4j#readme) - Java rate limiting and circuit breaker library.
- [express-rate-limit](https://github.com/express-rate-limit/express-rate-limit#readme) - Rate limiting middleware for Express.js and Node.js.

## Observability and Logging
• [LangSmith](https://smith.langchain.com/) - Unified platform for tracing, evaluation, and prompt management from LangChain.
• [Helicone AI](https://www.helicone.ai/) - Open-source LLM observability with prompt tracing and cost monitoring.

Full visibility into LLM behavior, performance, and costs.

- [OpenTelemetry](https://opentelemetry.io/#readme) - Vendor-neutral observability framework.
- [Traceloop OpenLLMetry](https://github.com/traceloop/openllmetry#readme) - OpenTelemetry for LLMs.
- [Grafana](https://github.com/grafana/grafana#readme) - Metrics visualization.
- [Loki](https://github.com/grafana/loki#readme) - Log aggregation for LLM logs.
- [AgentOps](https://www.agentops.ai/#readme) - Observability for agentic loops with tool usage tracking.

## Agentic Orchestration
• [LangFlow](https://www.langflow.org/) - Visual framework for building agents and agent-based applications.
• [Promptflow](https://github.com/microsoft/promptflow) - Development tool for streamlining LLM application development.
• [LangChain Agents](https://python.langchain.com/docs/modules/agents/) - Framework for building agents with LangChain.
• [Microsoft Semantic Kernel](https://github.com/microsoft/semantic-kernel) - SDK for orchestrating AI agents with planners, memory, and connectors.

Build and manage autonomous agents, long-running tasks, and multi-agent coordination.

- [LangGraph](https://github.com/langchain-ai/langgraph#readme) - Low-level orchestration framework for building stateful, multi-agent applications.
- [Agency Swarm](https://github.com/vrsen/agency-swarm#readme) - Multi-agent framework building collaborative networks of AI agents.
- [CrewAI](https://github.com/crewAIInc/crewAI#readme) - Multi-agent framework with LLM routing.
- [AutoGen](https://github.com/microsoft/autogen#readme) - Microsoft multi-agent framework.
- [UiPath Maestro](https://www.uipath.com/#readme) - Enterprise orchestrator blending LLM agents with RPA and human-in-the-loop.

## SDKs and Libraries
• [Replicate SDK](https://replicate.com/docs) - SDK for running and fine-tuning open-source models.

Multi-provider abstractions and LLM client libraries.

- [OpenAI Python SDK](https://github.com/openai/openai-python#readme) - Official OpenAI client.
- [Anthropic Python SDK](https://github.com/anthropics/anthropic-sdk-python#readme) - Official Claude client.
- [Vercel AI SDK](https://github.com/vercel/ai#readme) - AI SDK for Next.js and Svelte.
- [LiteLLM Python SDK](https://docs.litellm.ai/docs/python-sdk#readme) - Unified interface for 100+ providers.
- [Correctover SDK](https://github.com/Correctover/Correctover-#readme) - Enterprise AI reliability SDK with self-healing rules engine and 6-dimension contract validation.
- [Portkey Python SDK](https://docs.portkey.ai/docs/get-started/python-sdk#readme) - Multi-provider with tracing.
- [NeuralBridge](https://github.com/Correctover/neuralbridge-sdk#readme) - Self-healing engine for LLM APIs with 87 fault-recovery rules and MAPE-K decision loop.
- [LangChain](https://github.com/langchain-ai/langchain#readme) - LLM orchestration framework.
- [LlamaIndex](https://github.com/run-llama/llama_index#readme) - RAG framework with gateway integrations.
- [tiktoken](https://github.com/openai/tiktoken#readme) - Fast tokenization by OpenAI.
- [tokenizers](https://github.com/huggingface/tokenizers#readme) - Hugging Face tokenizers.
- [httpx](https://github.com/encode/httpx#readme) - Async HTTP client.
- [Ferro Labs Go SDK](https://github.com/ferro-labs/ai-gateway#readme) - Go SDK for Ferro Labs gateway.

## Guardrails and Security
• [HiddenLayer](https://hiddenlayer.com/) - ML model security platform for protecting AI systems.
• [Microsoft Presidio](https://microsoft.github.io/presidio/) - Open-source service for PII detection and redaction.
• [Amazon Comprehend](https://aws.amazon.com/comprehend/) - NLP service for insights and content moderation.
• [Guardrails AI](https://www.guardrailsai.com/) - Open-source framework for adding validation and correction to LLM outputs.
• [NeMo Guardrails](https://github.com/NVIDIA-NeMo/Guardrails) - Programmable guardrails for LLM applications (NVIDIA).

Content filtering, PII redaction, and prompt injection protection.

- [Ferro Labs Guardrails](https://github.com/ferro-labs/ai-gateway#readme) - Word/phrase filtering and token limits.
- [NeMo Guardrails](https://github.com/NVIDIA-NeMo/Guardrails#readme) - NVIDIA dialogue guardrails.
- [SlashLLM](https://slashllm.com/#readme) - Enterprise security platform.
- [AWS AI Services](https://aws.amazon.com/machine-learning/ai-services/#readme) - Amazon content moderation.
- [DeepEval](https://github.com/confident-ai/deepeval#readme) - Open-source testing framework for LLM outputs.
- [OpenZiti Security](https://github.com/openziti/llm-gateway#readme) - Zero-trust access with E2E encryption.
- [Agentic Security](https://github.com/msoedov/agentic_security#readme) - Agentic LLM vulnerability scanner and AI red teaming kit.
- [DeepTeam](https://github.com/confident-ai/deepteam#readme) - Framework to red team LLMs and AI agents.
- [Fast LLM Security Guardrails](https://github.com/ZenGuard-AI/fast-llm-security-guardrails#readme) - The fastest trust layer for AI agents.
- [Last Layer](https://github.com/arekusandr/last_layer#readme) - Ultra-fast, low latency LLM prompt injection and jailbreak detection.
- [Open Bias](https://github.com/open-bias/open-bias#readme) - Open-source reliability harness for enforcing, tracing, and improving agent rule compliance.
- [Trylon Gateway](https://github.com/trylonai/gateway#readme) - Self-hosted firewall for LLMs with powerful guardrails.
- [PROMPTPurify](https://github.com/securelayer7/PROMPTPurify#readme) - Prompt-injection guardrail using compact model that outperforms larger open-source guards.
- [Control Layer](https://github.com/Emmimal/control-layer#readme) - Production-grade control layer with input validation, schema enforcement, and circuit breaking.
- [HAI Guardrails](https://github.com/presidio-oss/hai-guardrails#readme) - TypeScript library providing guards for LLM applications.
- [VeilArmor](https://github.com/0x-Professor/VeilArmor#readme) - Enterprise-grade security framework for LLMs with multi-layered protection.
- [Agent Guardrails](https://github.com/logi-cmd/agent-guardrails#readme) - Merge gates and safety checks for AI coding agents via MCP.

## Tutorials and Case Studies
• [Google Cloud AI Gateway Best Practices](https://cloud.google.com/blog/topics/developers-practitioners/best-practices-for-building-ai-powered-applications-on-google-cloud) - Google Cloud blog.

- [LiteLLM Quick Start](https://docs.litellm.ai/docs/#readme) - Official LiteLLM documentation.
- [Bifrost Documentation](https://github.com/maximhq/bifrost#readme) - Bifrost setup guide.
- [Portkey Quick Start](https://portkey.ai/docs#readme) - Portkey getting started guide.
- [Failover Routing Strategies](https://portkey.ai/blog/failover-routing-strategies-for-llms-in-production#readme) - Production patterns.
- [Semantic Caching Guide](https://scalemind.ai/blog/semantic-caching-llm-guide#readme) - Implementation best practices.
- [Cost-Aware Routing Patterns](https://www.mindstudio.ai/blog/best-ai-model-routers-multi-provider-llm-cost/#readme) - Routing strategies.
- [OpenRouter Multi-Provider Routing](https://dev.to/kirponik/mastering-multi-provider-routing-with-openrouter-1ce3#readme) - OpenRouter guide.
- [Cortex](https://arxiv.org/html/2509.17360v2#readme) - Semantic-aware knowledge caching for LLM agents.
- [Ferro Labs Getting Started](https://github.com/ferro-labs/ai-gateway#readme) - Go-native gateway setup.
- [OSS LLMOps Stack](https://github.com/langfuse/oss-llmops-stack#readme) - Modular open-source LLMOps stack combining LiteLLM and Langfuse.
- [awesome-mllm-guardrails](https://github.com/ant-research/awesome-mllm-guardrails#readme) - Curated list of LLM guardrails, safety benchmarks, guard models, and jailbreak attacks.

## Communities
• [LLMops Subreddit](https://www.reddit.com/r/LLMOps/) - Reddit community for LLM operations.
• [MLops.community](https://mlops.community/) - Community for MLOps practitioners.
• [Discord: AI Gateway Developers](https://discord.gg/aigateway) - Community for discussing gateway patterns, tools, and best practices.

- [/r/LLMOps](https://reddit.com/r/LLMOps#readme) - Reddit community for LLM operations.
- [LangChain Discord](https://discord.gg/langchain#readme) - Framework community.
- [LiteLLM Discord](https://discord.gg/tdNkNArv#readme) - Gateway community.
- [Hugging Face Community](https://discuss.huggingface.co/#readme) - Model and deployment discussions.

## Related Awesome Lists

- [rothgar/awesome-tuis](https://github.com/rothgar/awesome-tuis) - 18K+ stars, comprehensive TUI list.
- [msmps/awesome-opentui](https://github.com/msmps/awesome-opentui) - Curated open TUI resources.
