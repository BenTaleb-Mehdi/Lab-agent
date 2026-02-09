---
marp: true
theme: gaia
class: invert
paginate: true
style: |
  @import url('https://fonts.googleapis.com/css2?family=JetBrains+Mono:wght@400;700&family=Roboto:wght@400;700&display=swap');

  section {
    font-family: 'Roboto', sans-serif;
    background-color: #1e1e1e;
    color: #e0e0e0;
    font-size: 26px;
  }

  /* Tech Headlines */
  h1, h2, h3 {
    font-family: 'Roboto', sans-serif;
    color: #38bdf8;
    text-transform: uppercase;
    letter-spacing: 1px;
  }
  
  h1 { 
    font-size: 3.5em; 
    text-shadow: 0 0 20px rgba(56, 189, 248, 0.4);
  }

  blockquote {
    background: #2d2d2d;
    border-left: 5px solid #38bdf8;
    padding: 20px;
    border-radius: 0 8px 8px 0;
  }

  .title-info {
    padding-left:10px;
    display: inline-block;
    text-align: left;
    margin-top: 1rem;
    font-family: 'JetBrains Mono', monospace;
  }



  .subtitle {
    display: block;
    font-size: 0.6em;
    color: #94a3b8;
    text-transform: none;
    
  }

  img { border: 2px solid #38bdf8; border-radius: 8px; }

---

# LAB Agent

<div class="title-info">

**Dev:** Ben Taleb Mehdi
**Lead:** Mr.ESSARRAJ Fouad
**Lab:** Agent
**Date:** 05/01/2026

</div>

---

## Sommaire

1. **The Agent**
   <span class="subtitle">The Autonomous Brain & Reasoning Engine</span>

2. **Rules**
   <span class="subtitle">Passive Governance & System Constraints</span>

3. **Workflows**
   <span class="subtitle">Active Procedures & Slash Commands (/todo)</span>

4. **Skills**
   <span class="subtitle">Dynamic Expertise & Tool-Use Extension</span>

---



## 00. Agent Definition

> The autonomous "Brain" capable of reasoning and environmental interaction.

* **Identity:** An AI entity (Gemini 3) that moves beyond static chat into goal-driven action.
* **Cognition:** Uses a **Reasoning Engine** to decompose high-level prompts into granular technical tasks.
* **Autonomy:** Operates via a **Self-Correction Loop**—observing errors and adjusting strategy without human intervention.
* **Memory:** Maintains a persistent state of the codebase, project history, and developer preferences.



---

## 01. Rules (Governance)

Passive constraints that define the project's "DNA."

* **Persistence:** Always active (e.g., `~/.gemini/GEMINI.md` or `.agent/rules/`).
* **Activation Modes:**
    * **Always On:** Strict adherence to coding standards.
    * **Glob Pattern:** Applies only to specific files (e.g., `**/*.test.php`).
    * **Model Decision:** Agent applies rule only when contextually relevant.

---

## 02. Workflows (Procedures)

Active "Playbooks" for repeatable technical tasks.

* **Triggered on Demand:** Invoked via `/` commands (e.g., `/create-crud`).
* **Sequential Trajectory:** Guides the agent through complex logic chains.
* **Self-Correction:** If a step fails, the workflow forces a debug iteration.
* **Chaining:** Workflows can call other workflows for modular automation.

---

## 03. Skills (Modular Expertise)

Ephemeral "Knowledge Packs" loaded only when needed.

* **Context Efficiency:** Prevents prompt bloating by loading tools on-demand.
* **Executable Assets:** Bundles Python/Bash scripts with instructions.
* **Workspace vs. Global:**
    * **Workspace:** Project-specific (e.g., Laravel MCP servers).
    * **Global:** Universal utilities (e.g., Security Auditor, Image Optimizer).

---
## Example: Creating a "Product" Feature
#### Trigger: /build-feature Product

* **Architecture** (Rule 1): Agent creates ProductService.php.

* **Testing** (Rule 2): Agent writes ProductServiceTest.php in tests/Unit.

* **Security** (Skill 4): Agent asks, "Which role can delete products?" and applies Spatie tags.

* **Execution** (Workflow 3): Agent runs tests, fixes errors, and finally delivers the Blade views.

---
##  Lab Directory Structure (Autonomous Agent Example)

```
.agent/
├── rules/
│   └── instructions-frontend.md 
├── skills/
│   └── expert-service.md  
│   └── expert-http.md  
│   └── expert-database.md  
│   └── expert-frontend.md  
├── workflows/
    └── develop.md  

```

---
