VROMLIX GENESIS: Polymath Cognitive Architecture
"Simplicity is the ultimate sophistication." - Da Vinci.
🚀 Overview
VROMLIX Genesis is an enterprise-grade ETL (Extract, Transform, Load) pipeline designed to architect a personal "Second Brain". It serves as the intelligent backend for VROMLIX Prime (a custom Gemini Gem), enabling Dynamic Context Injection and Cross-Domain Reasoning.
Unlike traditional RAG (Retrieval-Augmented Generation) systems that simply perform keyword search, VROMLIX employs a custom "Da Vinci Protocol". This approach prioritizes latent semantic connections, bridging disparate domains (e.g., applying Physics principles to Business Strategy) to emulate polymathic thinking.
🏗️ System Architecture
The system operates on a Hybrid Cloud Architecture (Google Colab + Google Drive + Gemini API) utilizing four distinct cognitive modules:
1. Module 1: The Refinery (Ingestion & Resilience)
Input: Unstructured data (WhatsApp logs, Raw Notes, Google Docs).
The "Zipper Maneuver": Implements a custom merging algorithm that stitches raw narrative text with AI-generated metadata into a single, coherent JSON object.
Enterprise Resilience (New in V4.1):
JSON-Schema Enforcement: Forces the LLM to output strict JSON Arrays, eliminating parsing errors common in raw text processing.
Auto-Failover Protocol: Features an Intelligent Key Rotator. If the primary API Key hits a Rate Limit (429 Error), the system automatically swaps to a backup identity in milliseconds, ensuring zero downtime during batch processing.
Temporal Logic: Automatically infers "Status" (Legacy vs. Current) to handle contradictory data over time (e.g., updating beliefs or job status).
2. Module 2: The Evolutionary Mirror
Function: Manages the perfil_dinamico.xml artifact.
Logic: A recursive feedback loop that analyzes the user's most recent "Current" thoughts against their historical "Legacy" profile. It resolves psychological and professional contradictions automatically (Last-in Wins strategy) to maintain an up-to-date user persona.
3. Module 3: The Neural Weaver (Semantic Graph)
Function: Constructs the hidden connective tissue of the brain.
Technology: Utilizes SentenceTransformers (all-MiniLM-L6-v2) to generate high-dimensional vector embeddings and calculate Cosine Similarity matrices.
Cognitive Routing: Classifies connections as either "Reinforcement" (Same Domain) or "Polymath" (Cross-Domain), enriching the Knowledge Graph with non-obvious links.
4. Module 4: The Cartographer (High-Speed Indexing)
Function: Generates a lightweight navigation map (00_INDICE_GENERADO.csv).
Purpose: Provides the LLM with a "Table of Contents" of the user's mind. This allows the Gem to "scan" the entire knowledge base structure to select the correct files before performing deep retrieval, optimizing context window usage.
📊 Output Schema (CSV Index)
The system enforces a strict quality control schema for the navigation index:
ID_Hash | Title | Role | Score (1-5) | Status | Summary | Key_Connections
Note: The 'Score' field enables automated filtering of high-value insights (Score 5) vs. trivial daily logs.
🛠️ Usage
Configuration: Define GOOGLE_API_KEY (and optional backup keys GOOGLE_API_KEY_01, _02...) in your Environment Secrets.
Ingestion: Place raw .txt files in the watched Chats_Nuevos directory.
Execution: Run the VROMLIX_GENESIS.ipynb pipeline.
Deployment: The system automatically updates the Master JSONL database and deploys the new CSV Index to the Gem's context folder.
🔮 Future Roadmap
Temporal Simulation: Query the Gem to simulate user responses from specific past years.
Psychological Audit: Automated detection of bias shifts over time.
Content Synthesis: Generation of articles mimicking the user's specific writing style and worldview.
💻 Tech Stack
Core: Python 3.10+
LLM: Google Gemini 3.0 / 2.0 Flash (via Google GenAI SDK).
Resilience: Custom API Key Rotation Manager (Failover).
Vector Engine: Sentence-Transformers (Hugging Face).
Data Processing: Pandas, JSON, Regex.

Architected by Roger & Gemini.
