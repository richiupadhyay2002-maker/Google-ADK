# Google ADK — Agentic AI with Tools & Memory

## Overview

A hands-on notebook working through Google's Agent Development Kit (ADK) with the Gemini 2.5 Flash model, covering three core agentic AI patterns:

1. **Custom Tools (`FunctionTool`)** — giving an agent a real, callable Python function (e.g. a live weather API lookup) so it can act on real-time data, not just generate text.
2. **Agent-as-a-Tool orchestration** — a top-level "orchestrator" agent that delegates sub-tasks to specialist agents (e.g. a data-lookup agent and a concierge agent), rather than one agent trying to do everything.
3. **Session-based conversational memory** — a direct, side-by-side comparison of an agent's behavior *with* a persistent session (it correctly remembers prior turns and adapts a multi-day trip plan) versus *without* one (it "forgets" prior context and asks the user to repeat themselves).

## What's built

- **Day Trip Genie** — a single-agent itinerary generator that takes budget and mood constraints and produces a full-day plan.
- **Weather-Aware Planner** — an agent using a custom `FunctionTool` to call a live weather API before recommending outdoor activities.
- **Trip Data Concierge** — an orchestrator agent that delegates to a data-lookup agent and a concierge agent using the Agent-as-a-Tool pattern.
- **Adaptive Multi-Day Trip Agent** — demonstrates session memory by re-planning part of an itinerary based on user feedback mid-conversation, and includes a deliberate "memory failure" demo (same query, separate sessions) to show why session management matters.

## Stack

- Google ADK (`google-adk`)
- Gemini 2.5 Flash (via Vertex AI)
- Python, `asyncio`

## How to run

```bash
pip install google-adk google-generativeai -q
```

Set `PROJECT_ID` and `LOCATION` for your Google Cloud project, authenticate, and run `Google ADK.ipynb` top to bottom. Each section is self-contained and demonstrates one pattern.

## Note

This is a guided, hands-on build following Google's ADK tutorial structure — it's real, working agentic AI code (not a toy demo), but it's a learning exercise rather than an original production system designed from scratch. Framed honestly, it demonstrates practical fluency with tool integration, multi-agent orchestration, and memory management — the same building blocks used in production agentic systems.

## Author

**Richi Upadhyay** — Data Science & Machine Learning
