
# VROMLIX: AI Engine & Cognitive Orchestrator

> *"Simplicity is the ultimate sophistication." - Da Vinci*

## 🚀 Overview
**VROMLIX Engine** (v8.0.0) is an enterprise-grade Cognitive ETL pipeline designed to architect a personal "Second Brain". Unlike traditional RAG systems that rely on simple keyword search, VROMLIX employs a **Greedy Vectorization Strategy** and a **Split-Brain Topology** to build a persistent, high-fidelity Knowledge Graph.

It acts as the backend orchestration layer, transforming unstructured entropy (logs, notes, docs) into structured, retrieval-ready vectors.

### 📐 System Design
This engine has been refactored from a procedural script into a **Modular Monolith** using strict Python 3.12+ typing and Dependency Injection.

👉 **[View Full System Architecture & Logic Flow](./docs/ARCHITECTURE.md)**

## 🏗️ Core Modules: Da Vinci Protocol v8.0

The system operates on a Hybrid Cloud Architecture (Python Native + Google GenAI SDK + FAISS), orchestrating three core services:

### Service 1: The Refinery (Micro-Analysis Layer)
* **Engine:** `gemma-3-27b-it` (Atomic Extraction).
* **Function:** Ingests raw text and extracts deep metadata dimensions:
    * *Cronos:* Temporal anchoring and sequence logic.
    * *Logos/Pathos:* Belief systems, mental models, and emotional tone.
    * *Techne:* Tool stacks and technical solutions.
* **Resilience:** Features a **RobustParser** class that sanitizes "dirty" LLM outputs and handles JSON anomalies automatically.

### Service 2: The Mirror (Profile Surgery Layer)
* **Engine:** `gemini-3-flash-preview` (Macro-Synthesis).
* **Safety Protocol - Kernel Isolation:** Implements a "Split-Brain" technique. The Orchestrator physically separates the Profile XML into `Static` (Immutable) and `Dynamic` (Mutable) blocks. The LLM *never* has write access to the core kernel, preventing "hallucination drift".

### Service 3: The Neural Weaver (Greedy Vectorization)
* **Engine:** Sentence-Transformers (`all-MiniLM-L6-v2`) + FAISS.
* **Strategy:** "If it's not vectorized, it doesn't exist."
    Instead of summarizing, the indexing engine concatenates deeply extracted metadata into a dense vector payload. This creates an **"Engram-like"** retrieval system, prioritizing hard concepts (N-Grams) over soft narrative.

## 📊 Data Structures
* **The Ledger (JSONL):** A strictly formatted, append-only database of every interaction.
* **The Map (CSV):** A lightweight, human-readable index with "Deep Context" snippets for rapid auditing.
* **The Profile (XML):** A dynamic ontology of the user's state, hardware constraints, and operational preferences.

## 🛠️ Usage

### Prerequisites

```bash
pip install -r requirements.txt

```

### Execution (CLI)

The v8.0 engine supports argument parsing for modular execution:

```bash
# Full Pipeline (Ingest -> Surgery -> Index)
python main.py --run-all

# Modular Execution (e.g., only rebuild vector index)
python main.py --index

```

## 🔮 Roadmap & Version History

* **v6.0 (Genesis):** Initial script with basic RAG.
* **v7.5 (Active Inference):** Introduction of XML "Split-Brain" logic.
* **v8.0 (Current - Industrial Standard):** Complete refactor to OOP, Python 3.12+ Typing, `pathlib` safety, and migration to Google GenAI SDK v0.5.
* **v9.0 (Future - Voice Core):** Direct audio stream processing for real-time debate simulation.

## 💻 Tech Stack

* **Orchestration:** Python 3.12+ (Type Hinted).
* **LLM Inference:** Google GenAI SDK (Unified Client).
* **Vector Database:** FAISS (CPU Optimized).
* **Serialization:** JSONL (Ledger) & XML (Profile).

---

*Architected by Rogelio Lozano.*

