<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&height=220&color=0:0B1020,35:1D4ED8,70:0EA5E9,100:22C55E&text=Yagna%20Siva%20Sai%20Kumar&fontSize=42&fontColor=ffffff&fontAlignY=35&desc=AI%2FML%20Engineer%20%E2%80%A2%20Agent%20Infrastructure%20Builder%20%E2%80%A2%20Production%20Systems&descAlignY=58&descSize=16" />

<p>
  <strong>Building production-grade agent systems end to end:</strong><br/>
  route, orchestrate, govern, and test with deterministic execution and safety guardrails.
</p>

<p>
  <a href="https://github.com/yagna-1/agentstack-reference"><img alt="AgentStack Reference" src="https://img.shields.io/badge/AgentStack-Reference%20Repo-0B1020?style=for-the-badge&logo=github&logoColor=white" /></a>
  <a href="https://yagna-1.vercell.app"><img alt="Portfolio" src="https://img.shields.io/badge/Portfolio-Live-16A34A?style=for-the-badge&logo=vercel&logoColor=white" /></a>
  <a href="mailto:yagnasivasaikumar@gmail.com"><img alt="Email" src="https://img.shields.io/badge/Email-Contact-0A66C2?style=for-the-badge&logo=gmail&logoColor=white" /></a>
  <a href="https://linkedin.com/in/yagna-siva-sai-kumar-984881201/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-Profile-1D4ED8?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
</p>

<p>
  <img alt="AgentStack reference stars" src="https://img.shields.io/github/stars/yagna-1/agentstack-reference?style=flat-square&label=agentstack-reference&color=0ea5e9" />
  <img alt="NexusGate stars" src="https://img.shields.io/github/stars/yagna-1/nexusgate?style=flat-square&label=nexusgate&color=22c55e" />
  <img alt="FluxRoute stars" src="https://img.shields.io/github/stars/yagna-1/fluxroute?style=flat-square&label=fluxroute&color=3b82f6" />
  <img alt="AstraGraph stars" src="https://img.shields.io/github/stars/yagna-1/astragraph?style=flat-square&label=astragraph&color=14b8a6" />
  <img alt="Recast stars" src="https://img.shields.io/github/stars/yagna-1/recast?style=flat-square&label=recast&color=f59e0b" />
  <img alt="mcp-test stars" src="https://img.shields.io/github/stars/yagna-1/mcp-test?style=flat-square&label=mcp-test&color=a855f7" />
</p>

</div>

## Executive Summary

I design and ship agent infrastructure that teams can run in production with confidence.

- deterministic orchestration and replay
- policy-first fail-closed enforcement
- workflow-level routing and budget controls
- audit-to-regression-test generation
- MCP contract and policy validation for CI

## AgentStack Platform

The combined reference repository is listed first, followed by the five core platform layers.

| Priority | Repository | Layer | What it contributes |
| --- | --- | --- | --- |
| 1 | **[agentstack-reference](https://github.com/yagna-1/agentstack-reference)** | Platform Glue | Single compose-based reference stack that wires all layers together. |
| 2 | **[nexusgate](https://github.com/yagna-1/nexusgate)** | Route | MCP/LLM ingress, provider fallback, workflow-aware spend governance. |
| 3 | **[fluxroute](https://github.com/yagna-1/fluxroute)** | Orchestrate | Deterministic DAG runtime, replay semantics, tenant-aware control-plane primitives. |
| 4 | **[astragraph](https://github.com/yagna-1/astragraph)** | Govern | Fail-closed policy enforcement and causal audit graph for MCP/A2A actions. |
| 5 | **[recast](https://github.com/yagna-1/recast)** | Test (Agent) | Compiles production traces/audit logs into static Playwright suites. |
| 6 | **[mcp-test](https://github.com/yagna-1/mcp-test)** | Test (MCP) | MCP client/test harness with policy assertion helpers for CI gates. |

## Architecture Snapshot

```mermaid
flowchart LR
    A[Client / Agent Apps] --> B[NexusGate]
    B --> C[FluxRoute]
    C --> D[AstraGraph]
    D --> E[Recast]
    D --> F[mcp-test]
    E --> G[Playwright Regression Suite]
    F --> H[MCP Contract + Policy CI Checks]
    G --> I[Ship / Block Decision]
    H --> I
```

## Current Focus

- hardening the AgentStack reference path for faster onboarding and reproducible demos
- strengthening the AstraGraph -> Recast regression loop
- making policy + contract checks first-class in CI with `mcp-test`

## Highlighted Repositories

<div align="center">
  <a href="https://github.com/yagna-1/agentstack-reference">
    <img src="https://opengraph.githubassets.com/1/yagna-1/agentstack-reference" alt="agentstack-reference" width="49%" />
  </a>
  <a href="https://github.com/yagna-1/nexusgate">
    <img src="https://opengraph.githubassets.com/1/yagna-1/nexusgate" alt="nexusgate" width="49%" />
  </a>
</div>

<div align="center">
  <a href="https://github.com/yagna-1/fluxroute">
    <img src="https://opengraph.githubassets.com/1/yagna-1/fluxroute" alt="fluxroute" width="49%" />
  </a>
  <a href="https://github.com/yagna-1/astragraph">
    <img src="https://opengraph.githubassets.com/1/yagna-1/astragraph" alt="astragraph" width="49%" />
  </a>
</div>

<div align="center">
  <a href="https://github.com/yagna-1/recast">
    <img src="https://opengraph.githubassets.com/1/yagna-1/recast" alt="recast" width="49%" />
  </a>
  <a href="https://github.com/yagna-1/mcp-test">
    <img src="https://opengraph.githubassets.com/1/yagna-1/mcp-test" alt="mcp-test" width="49%" />
  </a>
</div>

## Proof of Engineering Impact

- Contributed to the OpenAI SWE-Lancer benchmark ecosystem, evaluating LLMs on large-scale real engineering tasks.
- Built distributed inference workloads executing 1,000+ parallel tasks on AWS.
- Improved retrieval performance by roughly 25% through hybrid retrieval and evaluation-led iteration.

## Research

- [SWE-Lancer (arXiv)](https://arxiv.org/abs/2502.12115)

## Technical Focus

| Area | Tools |
| --- | --- |
| Languages | Python, Go, Rust, TypeScript, SQL |
| AI/ML | PyTorch, TensorFlow, Hugging Face, RAG, LoRA/QLoRA, eval harnesses |
| Infra | AWS, Docker, Kubernetes, FastAPI, PostgreSQL, ChromaDB, FAISS |
| Observability & Runtime | OpenTelemetry, Prometheus, replay traces, policy telemetry |

## Connect

- Portfolio: [yagna-1.vercell.app](https://yagna-1.vercell.app)
- LinkedIn: [yagna-siva-sai-kumar](https://linkedin.com/in/yagna-siva-sai-kumar-984881201/)
- Email: [yagnasivasaikumar@gmail.com](mailto:yagnasivasaikumar@gmail.com)
