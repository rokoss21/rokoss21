<table width="100%" border="0" style="border: none; border-collapse: collapse;">
  <tr>
    <td align="center" valign="middle" style="padding: 10px;">
      <a href="https://github.com/rokoss21/FACET">
        <img src="https://github.com/rokoss21/FACET/blob/main/assets/banner.png?raw=true" alt="FACET Logo" height="200">
      </a>
    </td>
    <td align="center" valign="middle" style="padding: 10px;">
      <a href="https://github.com/rokoss21/rmcp-protocol">
        <img src="https://github.com/rokoss21/rmcp-protocol/blob/main/assets/logo.png?raw=true" alt="RMCP+FACET: Operating System for AI Ecosystems" height="200">
      </a>
    </td>
  </tr>
</table>

---

### 👋 About Me

I am an AI and Platform Engineer passionate about building developer tools founded on the principles of **determinism, predictability, and engineering rigor**. My work bridges the gap between creative AI potential and the reliability required for production systems.

This philosophy led to the creation of the **[FACET Language](https://github.com/rokoss21/FACET)**, a deterministic foundation upon which a larger ecosystem of high-performance AI tools is built.

---

### 🚀 The FACET Ecosystem

My work is centered around the **FACET ecosystem**, a full-stack solution designed to make AI interactions as rigorous, predictable, and scalable as modern cloud infrastructure. Each layer builds upon the last — from a deterministic language foundation to a global-scale AI orchestration engine.

```mermaid
%%{init: {
  "flowchart": { "htmlLabels": false, "curve": "basis" },
  "theme": "base",
  "themeVariables": {
    "fontFamily": "ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Ubuntu",
    "primaryBorderColor": "#111827",
    "primaryTextColor": "#111827",
    "lineColor": "#374151"
  }
}}%%
flowchart LR
    %% ========= LAYERS =========
    subgraph F["👑 FACET Language — Deterministic Markup & Contracts"]
        F1["Determinism"]
        F2["Typed Contracts"]
        F3["Pure Lenses"]
        F4["Parsers & Validators"]
    end

    subgraph M["⚡ FACET MCP Server — Agent-First Runtime"]
        M1["Tool Adapters"]
        M2["Policy & Guards"]
        M3["Streaming I/O"]
        M4["Sandboxes & Rate Limits"]
    end

    subgraph R["🧠 RMCP Orchestrator — OS-Level Scheduling & Observability"]
        R1["Scheduler & Queues"]
        R2["Tracing & Metrics"]
        R3["Multi-Agent Topologies"]
        R4["Registry & Discovery"]
    end

    %% ========= SHARED / SIDE SERVICES =========
    subgraph S["Shared Services"]
        S1["Schema Registry"]
        S2["Policy Store"]
        S3["Event Bus / Topics"]
        S4["Artifacts (Prompts, Lenses, Contracts)"]
    end

    %% ========= MAIN FLOW =========
    F -->|normalized specs| M -->|orchestrated tasks| R

    %% Feature mappings (dashed ribbons)
    F2 -. contracts .-> M2
    F3 -. structure .-> M1
    F4 -. validation .-> M4

    M1 -. fleet .-> R3
    M2 -. SLOs .-> R2
    M3 -. throughput .-> R1
    M4 -. registry .-> R4

    %% Shared services wiring
    F4 --- S1
    M2 --- S2
    M3 --- S3
    R1 --- S3
    F2 --- S4
    R4 --- S4

    %% Clickable deep-links (внутренние узлы)
    click F1 "https://github.com/rokoss21/FACET" _blank
    click F2 "https://github.com/rokoss21/FACET" _blank
    click M1 "https://github.com/rokoss21/FACET_mcp" _blank
    click M2 "https://github.com/rokoss21/FACET_mcp" _blank
    click R1 "https://github.com/rokoss21/rmcp-protocol" _blank
    click R3 "https://github.com/rokoss21/rmcp-protocol" _blank

    %% ========= STYLES =========
    style F fill:#e3f2fd,stroke:#111827,stroke-width:2px
    style M fill:#e8f5e9,stroke:#111827,stroke-width:2px
    style R fill:#f3e5f5,stroke:#111827,stroke-width:2px
    style S fill:#fff7ed,stroke:#92400e,stroke-width:1.5px

    style F1 fill:#ffffff,stroke:#60a5fa
    style F2 fill:#ffffff,stroke:#60a5fa
    style F3 fill:#ffffff,stroke:#60a5fa
    style F4 fill:#ffffff,stroke:#60a5fa

    style M1 fill:#ffffff,stroke:#34d399
    style M2 fill:#ffffff,stroke:#34d399
    style M3 fill:#ffffff,stroke:#34d399
    style M4 fill:#ffffff,stroke:#34d399

    style R1 fill:#ffffff,stroke:#a78bfa
    style R2 fill:#ffffff,stroke:#a78bfa
    style R3 fill:#ffffff,stroke:#a78bfa
    style R4 fill:#ffffff,stroke:#a78bfa

    style S1 fill:#ffffff,stroke:#f59e0b
    style S2 fill:#ffffff,stroke:#f59e0b
    style S3 fill:#ffffff,stroke:#f59e0b
    style S4 fill:#ffffff,stroke:#f59e0b

 ```

Each layer is a direct application of the core FACET philosophy:

---

### 👑 **[FACET Language](https://github.com/rokoss21/FACET)**

> The **foundation and source code of the philosophy**. A deterministic markup language for AI instructions, featuring first-class contracts and pure lenses.

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Language_Design-007ACC?style=for-the-badge" alt="Language Design">
  <img src="https://img.shields.io/badge/Parsing-orange?style=for-the-badge" alt="Parsing">
</p>

---

### ⚡ **[FACET MCP Server](https://github.com/rokoss21/FACET_mcp)**

> The **application layer**. A high-performance, "Agent-First" execution engine that makes the power of FACET accessible to AI agents as a reliable tool.

<p>
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/WebSockets-000000?style=for-the-badge&logo=websocket&logoColor=white" alt="WebSockets">
  <img src="https://img.shields.io/badge/SIMD-red?style=for-the-badge" alt="SIMD">
</p>

---

### 🧠 **[FACET Orchestrator (RMCP)](https://github.com/rokoss21/rmcp-protocol)**

> The **scaling layer**. An AI Operating System & Orchestration Engine that uses the principles of FACET to coordinate entire fleets of AI agents and tools at scale.

<p>
  <img src="https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white" alt="Rust">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" alt="FastAPI">
  <img src="https://img.shields.io/badge/Distributed_Systems-blueviolet?style=for-the-badge" alt="Distributed Systems">
</p>

---

### 🛠️ Core Competencies & Skills

* **AI & Machine Learning:** AI Orchestration, Multi-Agent Systems, AI Agent Tooling, Prompt Engineering, Structured Data Extraction.
* **Platform & Backend Engineering:** High-Performance Computing (SIMD), API Design, Asynchronous Services, Distributed Systems, Systems Programming.
* **Software Architecture:** Clean Architecture, Protocol Design (MCP), Domain-Driven Design (DDD).
* **Languages & Ecosystems:**

  * **Python:** Expert-level, including performance tuning (Numba, NumPy) and packaging (PyPI).
  * **Rust:** Proficient, with a focus on high-performance, memory-safe systems programming.
  * **JavaScript/TypeScript:** Proficient, including Node.js and packaging (NPM).
* **DevOps & Tooling:** CI/CD (GitHub Actions), Docker, Test-Driven Development (TDD), Release Management.

---

### 💬 Let's Connect

* **Email:** `ecsiar@gmail.com`
* **GitHub Discussions:** Feel free to start a conversation on any of the project repositories.
* **Contributing:** I welcome contributions to my open-source projects. Check out the `CONTRIBUTING.md` files to get started.
