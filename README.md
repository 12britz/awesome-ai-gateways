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
• [Kong AI Gateway Plugin](https://docs.konghq.com/gateway/latest/hub/kong-inc/ai-gateway/) - Kong plugin for LLM provider integration with request/response transformation.
• [Traefik Forward Auth for AI](https://doc.traefik.io/traefik/middlewares/forward-auth/) - Use forward auth middleware for AI-based authentication and authorization.
• [Traefik AI Plugin](https://doc.traefik.io/traefik/v2.0/plugins/ai-overview/) - Traefik plugin for AI-based request routing and middleware.
• [Traefik Pilot AI](https://pilot.traefik.io/) - AI-driven configuration and optimization for Traefik proxies.
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
- [lm-proxy](https://github.com/Nayjest/lm-proxy#readme) - Lightweight OpenAI-compatible proxy for multi-provider inference.
- [LLM API Proxy](https://github.com/rxliuli/llm-api-proxy#readme) - Edge runtime proxy supporting OpenAI, Anthropic, Gemini, and more.
- [LLMProxy](https://github.com/aiyuekuang/LLMProxy#readme) - High-performance reverse proxy for LLM inference with SSE streaming.
- [Zuul](https://github.com/Netflix/zuul#readme) - Netflix edge gateway.
- [RouteLLM](https://github.com/lm-sys/RouteLLM#readme) - Open-source framework from LMSYS for training and deploying lightweight LLM routers that balance cost and quality.

### Managed Services
• [OCI AI Services API Gateway](https://docs.oracle.com/en-us/iaas/Content/AI/Services/Concepts/aioverview.htm) - Oracle Cloud Infrastructure AI services exposed via API Gateway.
• [Alibaba Cloud API Gateway for AI](https://www.alibabacloud.com/help/doc-detail/301136.htm) - Alibaba Cloud's API gateway with AI capabilities for model serving.
• [Azure API Management with Cognitive Services](https://learn.microsoft.com/en-us/azure/api-management/api-management-howto-add-product) - Integrate Azure Cognitive Services with API Management for AI-enhanced APIs.
• [IBM API Connect AI](https://www.ibm.com/docs/en/api-connect/10.0.0.x?topic=services-ai) - Use AI for API lifecycle management and security in IBM API Connect.
• [AWS API Gateway with Bedrock Integration](https://docs.aws.amazon.com/apigateway/latest/developerguide/apigateway-websocket-bedrock.html) - Expose Bedrock models via REST/WebSocket APIs with throttling and auth.
• [GCP Apigee AI Gateway](https://cloud.google.com/apigee/docs/api-platform/get-started) - Manage and secure LLM APIs with Apigee's traffic management and analytics.

- [Vercel AI Gateway](https://sdk.vercel.ai/docs/ai-gateway#readme) - Single endpoint for hundreds of AI models.
- [Cloudflare AI Gateway](https://developers.cloudflare.com/ai-gateway/#readme) - Unified interface for AI providers at the edge.
- [OpenRouter](https://openrouter.ai/#readme) - Unified API for 500+ models from 60+ providers.
- [Portkey Hosted](https://portkey.ai/#readme) - Managed AI gateway with 1600+ LLMs and enterprise features.
- [Braintrust](https://www.braintrust.dev/#readme) - Unified API with encrypted caching and integrated evaluation.
- [Inworld Router](https://www.inworlds.ai/#readme) - LLM plus TTS pipelining for high-interactivity use cases.
- [Maxim AI](https://www.getmaxim.ai/#readme) - End-to-end platform for simulation, evaluation, and monitoring.
- [Together AI](https://www.together.ai/#readme) - Cloud platform for 200+ open-source models with optimized inference.
- [Fireworks AI](https://fireworks.ai/#readme) - Fast inference platform optimized for latency and throughput.
- [DeepInfra](https://deepinfra.com/#readme) - Serverless GPU inference for open-source LLMs.
- [Replicate](https://replicate.com/#readme) - Cloud platform for running and fine-tuning open-source models.
- [Anyscale](https://www.anyscale.com/#readme) - AI platform built on Ray for scaling LLM applications.

## Semantic Caching
• [RedisAI](https://redis.io/docs/stack/ai/) - Redis module for serving AI models and caching embeddings.
• [Vald](https://vald.vdaas.org/) - Highly scalable distributed fast approximate nearest neighbor search engine.
• [Elasticsearch Semantic Cache](https://www.elastic.co/guide/en/elasticsearch/reference/current/semantic-search.html) - Use Elasticsearch for semantic caching with dense vector search.
• [Weaviate](https://weaviate.io/) - Open-source vector database for storing and querying AI embeddings with hybrid search capabilities.
• [Weaviate Semantic Cache](https://weaviate.io/developers/weaviate/use-guides/generative-ai/semantic-caching) - Vector-based semantic caching using Weaviate hybrid search.
• [Milvus AI Cache](https://milvus.io/blog/semantic-caching.md) - Use Milvus vector store for prompt similarity caching.

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
• [Kubecost](https://kubecost.com/) - Cost monitoring for Kubernetes workloads, adaptable for LLM costs.
• [AWS Cost Explorer with AI Insights](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/) - AI-driven cost anomaly detection and forecasting.
• [OpenCost](https://opencost.io/) - Open-source cost monitoring for cloud-native workloads, can be adapted for LLM costs.
• [Cloudability](https://www.cloudability.com/) - Cloud cost management platform with AI-driven insights.
• [Prometheus LLM Exporter](https://github.com/berriai/litellm/tree/main/litellm-main#prometheus) - Export LLM metrics (tokens, latency, cost) to Prometheus via LiteLLM.
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

## Load Balancing and Routing
• [F5 NGINX Plus AI Security](https://www.f5.com/products/nginx-plus/ai-security) - AI-powered web application and API protection.
• [Citrix ADC with AI](https://www.citrix.com/products/citrix-adc.html) - Application delivery controller with AI-based traffic management.
• [Envoy AI Extension](https://www.envoyproxy.io/docs/envoy/latest/faq/overview/about) - Use Envoy extensions for AI-driven load balancing.
• [Istio AI Traffic Management](https://istio.io/latest/docs/tasks/traffic-management/) - AI-based traffic routing in Istio service mesh.
• [NGINX Plus AI Module](https://docs.nginx.com/nginx/admin-guide/dynamic-modules/ai-module/) - Dynamic module for request routing, fallback, and token limiting.
• [HAProxy LLM Runtime](https://www.haproxy.com/blog/haproxy-for-llm-load-balancing/) - Use HAProxy ACLs and stick tables for provider failover and latency-based routing.

Distribute traffic, implement failovers, and optimize costs.

- [LiteLLM Router](https://docs.litellm.ai/docs/proxy/routing#readme) - Retry/fallback logic and least-busy routing.
- [Portkey](https://portkey.ai/docs/routing-strategies#readme) - Conditional routing and percentage-based distribution.
- [Bifrost Load Balancing](https://www.getmaxim.ai/bifrostdocs#readme) - Adaptive load balancer with cluster mode.
- [Ferro Labs Router](https://github.com/ferro-labs/ai-gateway#readme) - Multi-provider routing with 29 providers.
- [Routerly Policies](https://www.routerly.ai/#readme) - 9 configurable policies including LLM-native routing.
- [Lovable: 1.8B tokens per minute load balancing](https://www.adwaitx.com/llm-provider-load-balancing-agent-workflows/#readme) - PID-controlled dynamic load balancing.
- [RouteLLM](https://github.com/lm-sys/RouteLLM#readme) - Cost-quality routing with trainable lightweight routers.

## API Management and Rate Limiting
• [MuleSoft AI Governance](https://www.mulesoft.com/lp/ai/anypoint-platform-for-ai) - AI-powered API governance and security.
• [Apigee API Hub with AI Recommendations](https://cloud.google.com/apigee/docs/api-hub/what-is-api-hub) - Discover and recommend APIs using AI-powered insights.
• [Apigee AI-powered API Management](https://cloud.google.com/apigee/docs/api-platform/get-started) - Google Cloud's Apigee with AI for intelligent API lifecycle management.
• [3Scale AI API Management](https://www.redhat.com/en/products/red-hat-3scale-api-management) - AI-enhanced API management for performance and security insights.
• [Tyk AI Gateway](https://tyk.io/blog/ai-gateway/) - Open-source API gateway with AI-specific rate limiting, token quotas, and prompt guardrails.
• [Kong AI Rate Limiting Advanced](https://docs.konghq.com/gateway/latest/hub/kong-inc/ai-rate-limiting-advanced/) - Plugin for token-based rate limiting and semantic caching.

Control access, prevent abuse, and enforce quotas.

- [RateLimit4j](https://github.com/vladimir-bukhtoyarov/rate-limit#readme) - Java rate limiting library.
- [Guava RateLimiter](https://github.com/google/guava#readme) - Google token bucket implementation.
- [Resilience4j RateLimiter](https://github.com/resilience4j/resilience4j#readme) - Java rate limiting and circuit breaker library.
- [express-rate-limit](https://github.com/express-rate-limit/express-rate-limit#readme) - Rate limiting middleware for Express.js and Node.js.
- [bottleneck](https://github.com/SGrondin/bottleneck#readme) - Promise-based rate limiter for Node.js with clustering support.

## Observability and Logging
• [Splunk AI for IT](https://www.splunk.com/en_us/products/splunk-ai-for-it.html) - AI-powered IT observability and security.
• [Dynatrace AI](https://www.dynatrace.com/solutions/artificial-intelligence/) - AI-powered observability and automation.
• [Datadog AI Monitoring](https://www.datadoghq.com/product/ai-monitoring/) - AI-powered monitoring for applications and infrastructure.
• [New Relic AI](https://newrelic.com/product/ai-monitoring) - AI-driven observability and incident response.
• [LangSmith](https://smith.langchain.com/) - Unified platform for tracing, evaluation, and prompt management from LangChain.
• [Helicone AI](https://www.helicone.ai/) - Open-source LLM observability with prompt tracing and cost monitoring.

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
• [LangFlow](https://www.langflow.org/) - Visual framework for building agents and agent-based applications.
• [Promptflow](https://github.com/microsoft/promptflow) - Development tool for streamlining LLM application development.
• [LlamaIndex Agents](https://docs.llamaindex.ai/en/stable/module_agents/index.html) - Build agents with LlamaIndex for data-aware applications.
• [LangChain Agents](https://python.langchain.com/docs/modules/agents/) - Framework for building agents with LangChain.
• [Microsoft Semantic Kernel](https://github.com/microsoft/semantic-kernel) - SDK for orchestrating AI agents with planners, memory, and connectors.
• [AutoGen Studio](https://microsoft.github.io/autogen/studio.html) - Low-code UI for building and debugging multi-agent workflows.

Build and manage autonomous agents, long-running tasks, and multi-agent coordination.

- [LangGraph](https://github.com/langchain-ai/langgraph#readme) - Low-level orchestration framework for building stateful, multi-agent applications.
- [Agency Swarm](https://github.com/vrsen/agency-swarm#readme) - Multi-agent framework building collaborative networks of AI agents.
- [CrewAI](https://github.com/crewAIInc/crewAI#readme) - Multi-agent framework with LLM routing.
- [AutoGen](https://github.com/microsoft/autogen#readme) - Microsoft multi-agent framework.
- [UiPath Maestro](https://www.uipath.com/#readme) - Enterprise orchestrator blending LLM agents with RPA and human-in-the-loop.

## SDKs and Libraries
• [Together AI SDK](https://docs.together.ai/reference/python-sdk) - Python SDK for Together AI's inference API.
• [Replicate SDK](https://replicate.com/docs) - SDK for running and fine-tuning open-source models.
• [Cohere Python SDK](https://docs.cohere.com/reference/python-sdk) - Official Python client for Cohere's NLP models.
• [AI21 Labs SDK](https://github.com/AI21Labs/ai21-studio-python-sdk) - Python SDK for AI21 Labs' Jurassic models.
• [Mistral AI SDK](https://github.com/mistralai/mistral-python) - Official Python client for Mistral AI endpoints.
• [Google AI Python SDK](https://github.com/google-generativeai/python-genai) - Generative AI SDK for Gemini models.

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
• [Lakera Guard](https://lakera.ai/guard) - Real-time AI application security for prompt injection, data loss, and more.
• [HiddenLayer](https://hiddenlayer.com/) - ML model security platform for protecting AI systems.
• [Microsoft Presidio](https://microsoft.github.io/presidio/) - Open-source service for PII detection and redaction.
• [Amazon Comprehend](https://aws.amazon.com/comprehend/) - NLP service for insights and content moderation.
• [Guardrails AI](https://www.guardrailsai.com/) - Open-source framework for adding validation and correction to LLM outputs.
• [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails) - Programmable guardrails for LLM applications (NVIDIA).

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

### Agent Identity & Payment Verification

- [TWZRD Agent Intel](https://intel.twzrd.xyz) - On-chain trust scoring for AI agents on Solana. Provides `score_agent(wallet)` and `preflight_check(wallet)` for verifying agent wallet identity before routing requests or authorizing x402 micropayments. Free streamable-HTTP MCP: `{"mcpServers":{"twzrd-agent-intel":{"url":"https://intel.twzrd.xyz/mcp"}}}`

## Tutorials and Case Studies
• [Microsoft Azure AI Gateway Documentation](https://learn.microsoft.com/en-us/azure/architecture/example-scenario/ai/ai-gateway) - Guide to building AI gateways on Azure.
• [HashiCorp Consul for AI Service Mesh](https://developer.hashicorp.com/tutorials/cloud-mesh-consul) - Using Consul for AI service discovery and security.
• [AWS AI/ML Gateway Patterns](https://aws.amazon.com/blogs/apigateway/building-ai-ml-gateways-with-amazon-api-gateway/) - AWS blog on building AI/ML gateways.
• [Google Cloud AI Gateway Best Practices](https://cloud.google.com/blog/topics/developers-practitioners/best-practices-for-building-ai-powered-applications-on-google-cloud) - Google Cloud blog.
• [Building AI Gateways with Kong](https://konghq.com/blog/how-to-build-an-ai-gateway-with-kong) - Step‑by‑step guide to adding LLM routing, caching, and guardrails.
• [Multi‑Provider LLM Routing with AWS API Gateway](https://aws.amazon.com/blogs/apigateway/integrating-amazon-bedrock-with-amazon-api-gateway/) - AWS tutorial on Bedrock integration.

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
• [MLOps World Community](https://mldotworld.com/community/) - Community for MLOps practitioners and enthusiasts.
• [Dataiku Community](https://www.dataiku.com/community/) - Community for collaborative data science and ML.
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
