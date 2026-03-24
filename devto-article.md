---
title: "I Built a Curated List of 50+ Tools for LLM Infrastructure (So You Don't Have To)"
published: true
tags: [ai, llm, llmops, opensource, programming]
canonical_url: https://github.com/12britz/awesome-ai-gateways
cover_image: 
description: "Managing LLM infrastructure is a mess. Here's a curated list of the best tools for routing, caching, cost tracking, and orchestration."
---

# The LLM Infrastructure Headache is Real

Last month, I was debugging a production issue at 2 AM. Our OpenAI calls were failing, latency was spiking, and our token costs had tripled in a week.

We weren't alone. Every team I've talked to building with LLMs hits the same walls:

- **"Which model should I use?"** - OpenAI? Anthropic? Local? 
- **"We're getting rate limited"** - How do we fail over gracefully?
- **"Wait, we spent $50K this month?"** - Where did all the tokens go?
- **"The agent is looping forever"** - How do we even debug this?

After weeks of research, I compiled everything I learned into one list: **[awesome-ai-gateways](https://github.com/12britz/awesome-ai-gateways)**

## What's Actually in It

### 1. AI Gateways (The Traffic Cops)
Instead of hardcoding API calls everywhere, route everything through a gateway.

- **[LiteLLM](https://github.com/BerriAI/litellm)** - The most popular. One line of code = 100+ LLMs
- **[Bifrost](https://github.com/maximhq/bifrost)** - Go-based, blazing fast, built-in semantic caching
- **[Portkey](https://github.com/Portkey-AI/portkey)** - 1600+ models, solid observability built in

### 2. Semantic Caching (The Cost Killer)
This is where the magic happens. Instead of hitting the API for every request, cache semantically similar responses.

> We reduced API costs by **67%** just by caching similar queries.

- **[RedisVL SemanticCache](https://redis.io/docs/latest/develop/ai/redisvl/0.7.0/user_guide/llmcache/)** - Drop-in semantic cache on Redis
- **[vCache](https://arxiv.org/abs/2502.03771)** - Academic but production-ready, verified caching
- **[GPT-Cache](https://github.com/ZhouDaoquan/GPT-Cache)** - Open source, multiple backends

### 3. Cost Tracking (The Budget Saver)
You can't optimize what you can't see.

- **[Langfuse](https://github.com/langfuse/langfuse)** - Open source, self-hostable, great UI
- **[Helicone](https://github.com/Helicone/helicone)** - Simple, works with any OpenAI-compatible API
- **[Confident AI](https://www.confident-ai.com/)** - Evaluation-first approach to observability

### 4. Agentic Orchestration (The New Frontier)
This is 2026's big thing - building agents that can reason, use tools, and collaborate.

- **[LangGraph](https://github.com/langchain-ai/langgraph)** - Build stateful, multi-step agents with cycles
- **[Agency Swarm](https://github.com/vrsen/agency-swarm)** - Multi-agent collaboration framework
- **[CrewAI](https://github.com/crewAIInc/crewAI)** - Role-based agent orchestration

### 5. Guardrails (The Safety Net)
Because your agent probably shouldn't be ordering pizza for strangers.

- **[NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails)** - NVIDIA's production-grade dialogue rails
- **[DeepEval](https://github.com/confident-ai/deepeval)** - Unit test your LLM outputs
- **[PromptGuard](https://github.com/protectai/promptguard)** - Defend against prompt injection

## The Full List

It's not just these tools. The list covers:
- Load Balancing & Routing patterns
- API Management & Rate Limiting
- Observability & Logging
- SDKs & Libraries
- Community resources

**[50+ tools with real GitHub links, descriptions, and use cases](https://github.com/12britz/awesome-ai-gateways)**

## Why This List Exists

I got tired of:
- Googling "best LLM gateway" and finding 5-year-old Stack Overflow answers
- Missing tools that would've saved me weeks
- Every team reinventing the same infrastructure

This list is my gift to future-me (and you). Star it, share it, and PR your additions.

**[Check out awesome-ai-gateways on GitHub](https://github.com/12britz/awesome-ai-gateways)**

---

*What's your biggest LLM infrastructure pain point? Drop it in the comments.*
