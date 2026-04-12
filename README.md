<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:1a1b27&height=200&section=header&text=Emil%20Rokossovskiy&fontSize=42&fontColor=e6edf3&fontAlignY=34&desc=AI%20Systems%20Architect%20%E2%80%A2%20Language%20Designer%20%E2%80%A2%20Compiler%20Engineer&descSize=16&descAlignY=54&descColor=8b949e&animation=fadeIn" width="100%" />

<br>

```
"You can't build reliable systems on top of nondeterministic contracts."
```

<a href="https://rokoss21.tech">Website</a> · <a href="https://linkedin.com/in/rokoss">LinkedIn</a> · <a href="https://dev.to/rokoss21">DEV.to</a> · <a href="mailto:ecsiar@gmail.com">Email</a>

</div>

---

I build **the contract layer for AI execution** — compilers, specifications, and runtimes that make AI behavior deterministic, typed, and reproducible.

Think of it as **what TypeScript did for JavaScript, but applied to AI execution**. Before: prompts as strings, retries, hope. After: compile-time contracts, canonical output, explicit failure codes.

Two ecosystems. One thesis: **AI systems should be engineered, not improvised.**

---

## Why This Matters in Practice

<table>
<tr>
<td width="33%" valign="top">

#### 💳 Payments

**Without FACET:**<br>
LLM returns `{status: "ok"}` instead of `{status: "success"}`. Downstream breaks. Retry. Pray.

**With FACET:**<br>
`@output` enforces `enum: ["success","failed"]` at compile time. Invalid shape → run fails before reaching your payment service.

</td>
<td width="34%" valign="top">

#### 🔄 Multi-Step Workflows

**Without IOSM:**<br>
Refactor "feels done". No metrics. No evidence. No way to compare before/after.

**With IOSM:**<br>
Baseline → hypothesis → 4 gated phases → cycle report. Simplicity 0.51 → 0.65. Tracked, reproducible, auditable.

</td>
<td width="33%" valign="top">

#### 🤖 Agent Orchestration

**Without contracts:**<br>
8 parallel agents. 3 write to the same file. Output drift between runs.

**With Swarm + IOSM:**<br>
File locks prevent conflicts. Quality gates enforce standards. Deterministic dispatch — not chaos.

</td>
</tr>
</table>

---

## The Standard

FACET is not another framework or wrapper. It is a **formal contract layer** — a specification that treats AI behavior as compiled software, not probabilistic improvisation. Designed to outlive any single vendor, model, or SDK.

The broader ecosystem — compilers, agents, orchestrators — exists to **prove the standard in practice**, not to replace it.

> **Implementations may evolve. The contract remains.**

**IOSM** — *Improve → Optimize → Shrink → Modularize* — is the companion methodology: a reproducible engineering process with strict phases, quality gates, and six canonical metrics.

Together: **FACET constrains execution. IOSM constrains evolution.**

<br>

<div align="center">

```facet
@input  amount:   float(min=0.01)
@input  currency: enum["USD","EUR","GBP"]
@output status:   enum["success","failed"]
@output tx_id:    string(min_length=8)
```

<sub>Invalid output never reaches the payment system. The contract is enforced before generation, not after.</sub>

</div>

---

## ⚡ The Core

<table>
<tr>

<td width="25%" align="center" valign="top">

<a href="https://github.com/rokoss21/facet-standard">
  <img src="./assets/card_facet_standard.png" alt="FACET Standard" width="100%">
</a>

**[FACET Standard](https://github.com/rokoss21/facet-standard)**<br>
<sub><b>Normative Specification</b></sub>

<img src="https://img.shields.io/github/stars/rokoss21/facet-standard?style=flat-square&color=e3b341&label=%E2%98%85">

<sub>v2.1.3 · REC-PROD<br>NADL · FTS · R-DAG · Token Box<br>Policy · Guards · Conformance</sub>

</td>

<td width="25%" align="center" valign="top">

<a href="https://github.com/rokoss21/facet-compiler">
  <img src="./assets/card_facet_compiler.png" alt="FACET Compiler" width="100%">
</a>

**[facet-compiler](https://github.com/rokoss21/facet-compiler)**<br>
<sub><b>Reference Implementation</b></sub>

<img src="https://img.shields.io/github/stars/rokoss21/facet-compiler?style=flat-square&color=e3b341&label=%E2%98%85">

<sub>Rust · fct 0.1.2 · 6 crates<br>AST → FTS → R-DAG → Canonical JSON<br>Other impls must match its behavior</sub>

</td>

<td width="25%" align="center" valign="top">

<a href="https://github.com/rokoss21/IOSM">
  <img src="./assets/card_iosm_spec.png" alt="IOSM Specification" width="100%">
</a>

**[IOSM Specification](https://github.com/rokoss21/IOSM)**<br>
<sub><b>Engineering Methodology</b></sub>

<img src="https://img.shields.io/github/stars/rokoss21/IOSM?style=flat-square&color=e3b341&label=%E2%98%85">

<sub>v1.0 · JSON schemas · Validator<br>4 phases · 6 metrics · Quality gates<br>Reproducible improvement cycles</sub>

</td>

<td width="25%" align="center" valign="top">

<a href="https://github.com/rokoss21/FACET_mcp">
  <img src="./assets/card_facet_mcp.png" alt="FACET MCP" width="100%">
</a>

**[FACET MCP](https://github.com/rokoss21/FACET_mcp)**<br>
<sub><b>Execution Boundary</b></sub>

<img src="https://img.shields.io/npm/v/facet-mcp-server?style=flat-square&color=cb3837&label=npm">

<sub>SIMD 3.7× · WebSocket · 70 tests<br>execute · lenses · validate<br>Protocol adapter & host</sub>

</td>

</tr>
</table>

---

## ⚙️ IOSM CLI — The Runtime

> Not just another CLI agent. A full **AI engineering runtime** that implements the IOSM methodology as a terminal-native execution environment.

<div align="center">

<a href="https://github.com/rokoss21/iosm-cli">
  <img src="./assets/iosm_cli_screenshot.png" alt="IOSM CLI" width="80%">
</a>

<br><br>

<img src="https://img.shields.io/npm/v/iosm-cli?style=for-the-badge&color=cb3837&label=npm"> &nbsp; <img src="https://img.shields.io/github/stars/rokoss21/iosm-cli?style=for-the-badge&color=e3b341&label=%E2%98%85">

</div>

<br>

<table>
<tr>
<td width="50%" valign="top">

**What it is:**
- Terminal TUI with interactive session management
- 15+ LLM providers (OpenAI, Anthropic, Gemini, Groq, Ollama, OpenRouter…)
- MCP server integration (1/1 connected, extensible)
- Built-in skills: `astro-report`, `claude-md-master`, `mcp-builder`, `skill-creator`
- Checkpoint system for session recovery

</td>
<td width="50%" valign="top">

**What makes it different:**
- Not a chat wrapper — an **IOSM runtime**: it enforces improvement cycles, gates, and metrics
- Contract-aware: understands FACET documents natively
- Multi-mode execution: `standard`, `singular`, `semantic`, `contract`
- Project memory and context management
- RPC bridge for programmatic access

</td>
</tr>
</table>

```sh
npm install -g iosm-cli
cd your-project && iosm init
iosm                           # launches TUI — 507 models ready
```

---

## 🏗 The Stack

> FACET is not a collection of tools. It is an **architecture**.<br>
> Each project has a specific architectural responsibility. Each project exists to fulfill it and nothing else.

```
   SPECIFICATION                 COMPILERS                    RUNTIME
  ┌──────────────┐          ┌──────────────────┐        ┌──────────────────┐
  │ facet-        │          │ facet-compiler   │        │ iosm-cli         │
  │ standard     │  ──────▶ │ (Rust, fct)      │ ─────▶ │ (TypeScript)     │
  │              │          │                  │        │                  │
  │ IOSM spec    │          │ FACET Language   │        │ swarm-iosm       │
  │              │          │ (Python parser)  │        │ (Python)         │
  │ soul.md      │          │                  │        │                  │
  └──────────────┘          │ FACET MCP Server │        │ rmcp-protocol    │
    Defines the rules       │ (SIMD adapter)   │        │ (FastAPI)        │
                            └──────────────────┘        └──────────────────┘
                              Implements them             Executes & scales

                                        │
                                        ▼

                              PROOF & CONSUMERS
                            ┌──────────────────┐
                            │ FACET-AGENTS     │  ← conformance testbed
                            │ FACET-FSSG       │  ← canonical JSON consumer
                            │ astrovisor-mcp   │  ← real-world MCP adapter
                            └──────────────────┘
                              Validates the contracts
```

<table>
<tr>
<td width="50%" valign="top">

**The architecture is self-correcting.**

If FACET-AGENTS can't reproduce behavior across providers — the standard has a gap. If FSSG can't produce byte-identical output from canonical JSON — the IR spec is wrong. If swarm-iosm needs to override quality gates — the methodology is incomplete.

</td>
<td width="50%" valign="top">

**What each layer proves:**

- **Specification** → the rules are expressible and complete
- **Compilers** → the rules are implementable and enforceable
- **Runtime** → the rules hold under real execution pressure
- **Proof** → the rules survive contact with production

</td>
</tr>
</table>

---

## 🔌 Ecosystem & Proof

<table>
<tr>

<td width="25%" align="center" valign="top">

<a href="https://github.com/rokoss21/swarm-iosm">
  <img src="./assets/card_swarm_iosm.png" alt="Swarm-IOSM" width="100%">
</a>

**[swarm-iosm](https://github.com/rokoss21/swarm-iosm)**<br>
<sub><b>Parallel Orchestration</b></sub>

<img src="https://img.shields.io/github/stars/rokoss21/swarm-iosm?style=flat-square&color=e3b341&label=%E2%98%85">

<sub>Python · v2.1 · Claude Code<br>Locks · Gates · Auto-spawn<br><i>Scaling layer</i></sub>

</td>

<td width="25%" align="center" valign="top">

<a href="https://github.com/rokoss21/rmcp-protocol">
  <img src="./assets/card_rmcp_protocol.png" alt="RMCP Protocol" width="100%">
</a>

**[rmcp-protocol](https://github.com/rokoss21/rmcp-protocol)**<br>
<sub><b>Distributed Coordination</b></sub>

<img src="https://img.shields.io/badge/coverage-89%25-10B981?style=flat-square">

<sub>FastAPI · Facet Engine<br>Three-stage funnel · 89% coverage<br><i>Protocol & scheduling</i></sub>

</td>

<td width="25%" align="center" valign="top">

<a href="https://github.com/rokoss21/FACET-AGENTS">
  <img src="./assets/card_facet_agents.png" alt="FACET Agents" width="100%">
</a>

**[FACET-AGENTS](https://github.com/rokoss21/FACET-AGENTS)**<br>
<sub><b>Conformance Testbed</b></sub>

<img src="https://img.shields.io/badge/agents-15-5B47FB?style=flat-square">

<sub>15 specialists · Self-evolving<br>Orchestrator v2.1 · 6.7× faster<br><i>Validates the standard</i></sub>

</td>

<td width="25%" align="center" valign="top">

<a href="https://github.com/rokoss21/FACET-FSSG">
  <img src="./assets/card_facet_fssg.png" alt="FACET FSSG" width="100%">
</a>

**[FACET-FSSG](https://github.com/rokoss21/FACET-FSSG)**<br>
<sub><b>Canonical JSON Consumer</b></sub>

<img src="https://img.shields.io/github/stars/rokoss21/FACET-FSSG?style=flat-square&color=e3b341&label=%E2%98%85">

<sub>Static Site Generator<br>Canonical JSON → byte-stable HTML<br><i>Proves the IR works</i></sub>

</td>

</tr>
</table>

---

## 🛠 Technical Focus

I work at the boundary where language design, compiler construction, execution control, and distributed orchestration meet.

**Compilers & Systems** — Rust, compiler construction (lexer → AST → IR → codegen), SIMD pipelines, deterministic execution, snapshot testing<br>
**AI Infrastructure** — MCP servers, multi-provider LLM orchestration, agent runtimes, semantic search, tool delegation<br>
**Architecture** — Language design (NADL), protocol design (RMCP), RFC-style specification authoring, contract-first DDD<br>
**Platform** — CI/CD with conformance suites, deterministic builds, Kubernetes, Prometheus, IOSM-driven quality gates

---

## 🗺 Other Work

<table>
<tr>
<td width="25%" align="center" valign="top">

<a href="https://github.com/rokoss21/soul.md">
  <img src="./assets/card_soul_md.png" alt="soul.md" width="100%">
</a>

**[soul.md](https://github.com/rokoss21/soul.md)**<br>
<sub>Portable spec for AI agent personas<br>Provider-agnostic · MD/YAML</sub>

</td>
<td width="25%" align="center" valign="top">

<a href="https://github.com/rokoss21/astrovisor-mcp">
  <img src="./assets/card_astrovisor_mcp.png" alt="astrovisor-mcp" width="100%">
</a>

**[astrovisor-mcp](https://github.com/rokoss21/astrovisor-mcp)**<br>
<sub>50 astrology tools via MCP<br>Claude Desktop · TypeScript</sub>

</td>
<td width="25%" align="center" valign="top">

<a href="https://github.com/rokoss21/enigmo">
  <img src="./assets/card_enigmo.png" alt="enigmo" width="100%">
</a>

**[enigmo](https://github.com/rokoss21/enigmo)**<br>
<sub>E2EE messaging platform<br>Ed25519/X25519 · Dart · Zero-knowledge</sub>

</td>
<td width="25%" align="center" valign="top">

<a href="https://github.com/rokoss21/rift-spec">
  <img src="./assets/card_rift.png" alt="rift-spec" width="100%">
</a>

**[rift-spec](https://github.com/rokoss21/rift-spec)**<br>
<sub>Next-gen UDP transport protocol<br>Mobile-first · Noise crypto</sub>

</td>
</tr>
</table>

---

<div align="center">

<img src="https://github-readme-streak-stats.herokuapp.com/?user=rokoss21&theme=github-dark-blue&hide_border=true&background=0d1117&ring=58a6ff&fire=58a6ff&currStreakLabel=e6edf3" width="54%" />

<br><br>

**📜 [Standard](https://github.com/rokoss21/facet-standard)** · **🦀 [Compiler](https://github.com/rokoss21/facet-compiler)** · **📐 [IOSM](https://github.com/rokoss21/IOSM)** · **⚙️ [CLI](https://github.com/rokoss21/iosm-cli)** · **🐝 [Swarm](https://github.com/rokoss21/swarm-iosm)**

<br>

<img src="https://komarev.com/ghpvc/?username=rokoss21&label=Profile%20views&color=0e75b6&style=flat" />

<br><br>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,50:161b22,100:1a1b27&height=100&section=footer" width="100%" />

</div>
