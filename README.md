# Drive Ready – AI Agents | One Person Company (OPC) Initiative

> **Department of Technical Training, Aditya University**  
> *Hands-on Curriculum: Building Production-Grade AI Agents and LLM Applications for One Person Companies (OPC)*

---

## 📌 Repository Overview

This repository houses the complete practical coursework and implementation artifacts for the **Drive Ready – AI Agents | One Person Company (OPC) Initiative** at **Aditya University (Department of Technical Training)**.

The program guides engineers from foundational LLM mechanics (temperature, prompt engineering, tokenization, grounding, stateless APIs) to building real-world, enterprise-ready AI agents for an autonomous **One Person Company (OPC)**: **KLG Ancient World** ([klgancientworld.com](https://klgancientworld.com)), a digital cultural heritage initiative preserving ancient scripts, sacred routes, and interactive storytelling via AI.

---

## 📂 Repository Structure

```text
.
├── README.md                      # Global repository documentation
│
├── Day-1/
│   ├── README.md                  # Comprehensive documentation for Day 1
│   └── task.py                    # Implementation: Prompting, temperature, tokens & grounding
│
├── Day-2/
│   ├── README.md                  # Comprehensive documentation for Day 2
│   └── task.py                    # Implementation: Few-shot, JSON parsing & memory buffers
│
└── Day-3/
    ├── README.md                  # Comprehensive documentation for Day 3
    └── task.py                    # Implementation: LCEL chains, automated testing & agent architecture
```

---

## 🗓️ Curriculum & Day-by-Day Roadmap

| Day | Topic | Highlights & Practical Implementations | Task Implementation | Documentation |
| :--- | :--- | :--- | :--- | :--- |
| **Day 1** | **LLM Foundations & Prompt Engineering** | • Temperature tuning (`0.2` vs `1.2`)<br>• Grounding & hallucination prevention<br>• Statelessness vs. full conversation history<br>• Token efficiency: English (125) vs Telugu (136)<br>• KLG Ancient World OPC domain adaptation | [`Day-1/task.py`](Day-1/task.py) | [**Day-1 Documentation**](Day-1/README.md) |
| **Day 2** | **Few-Shot, Structured Outputs & State** | • Negative constraint enforcement<br>• Few-shot intent classification (`epigraphy`, `route`, `bug`)<br>• Zero-shot structured JSON extraction<br>• `@log_call` function decorator & tool auditing<br>• Sliding window buffer comparison (`MAX_TURNS=2` vs `MAX_TURNS=8`) | [`Day-2/task.py`](Day-2/task.py) | [**Day-2 Documentation**](Day-2/README.md) |
| **Day 3** | **LCEL, Automated Evaluation & Agents** | • Declarative chains with LCEL (`prompt \| llm \| parser`)<br>• Multi-turn `MessagesPlaceholder` state management<br>• Automated testing harness (`run_tests`) with 10/10 (100%) pass rate<br>• Prompt iteration benchmarking (`v1` vs `v3`)<br>• Temperature stability testing (`temperature=1.0`)<br>• System architecture: *Plain Code vs Single LLM vs AI Agent* | [`Day-3/task.py`](Day-3/task.py) | [**Day-3 Documentation**](Day-3/README.md) |

---

## 🛠️ Global Tech Stack & Prerequisites

* **Python:** 3.10+
* **LLM Model:** Google Gemini (`gemini-3.5-flash-lite`)
* **Frameworks & SDKs:**
  * `langchain` / `langchain-core`
  * `langchain-google-genai`
  * `openai` (used with Google's OpenAI-compatible endpoint)

### Installation

```bash
pip install -q langchain langchain-core langchain-google-genai openai
```

### Environment Variable Setup

All scripts and notebooks require a Google Gemini API key. Set it as an environment variable or add it to your Google Colab Secrets under `GEMINI_API_KEY`:

```bash
# On Linux / macOS:
export GEMINI_API_KEY="your-gemini-api-key"

# On Windows (Command Prompt):
set GEMINI_API_KEY=your-gemini-api-key

# On Windows (PowerShell):
$env:GEMINI_API_KEY="your-gemini-api-key"
```

In Python / Google Colab:
```python
import os
from google.colab import userdata

os.environ["GEMINI_API_KEY"] = userdata.get("GEMINI_API_KEY")
```

> ⚠️ **Security Warning:** Never hardcode or commit API keys into source code or Git repositories.

---

## 🏢 The OPC Enterprise Context: KLG Ancient World

Throughout this training program, tasks apply real-world enterprise engineering principles to build AI capabilities for **KLG Ancient World** ([klgancientworld.com](https://klgancientworld.com)):

* **Domain Facts:**
  * **Ancient Scripts:** Brahmi, Grantha, Latin, and Sanskrit.
  * **Narratives:** Puranic narratives and local Sthala Puranas.
  * **Sacred Landscape Routes:** Alqueva and St. Peter of the Orchards.
  * **Application:** **MythiLens** — a heritage exploration app with interactive quests, educational modules, and offline support.
* **Agent Capabilities Developed:**
  * Deterministic catalogue pricing/access fee lookups.
  * Guardrails that gracefully decline unverified claims or out-of-scope queries (*"I'll check with the KLG team"*).
  * Seamless bilingual engagement in English and Telugu.
  * End-to-end regression evaluation suite to prevent quality degradation across prompt iterations.

---

## 🚀 Running the Tasks

1. **Local CLI Execution:**
   Navigate into any day folder and run the python script:
   ```bash
   cd Day-1
   python task.py
   ```
2. **Interactive / Cloud Execution:**
   Upload or run the respective `task.py` file in Google Colab or your preferred Python IDE. Ensure your `GEMINI_API_KEY` secret or environment variable is configured.

---

## 📜 Acknowledgements

Developed as part of the **Drive Ready – AI Agents | One Person Company (OPC) Initiative** at **Aditya University – Department of Technical Training**.
