---
type: documentation
version: 1.0
date: 2026-07-20
tags: [system, obsidian, rag, stress_test]
---

# Obsidian Usage Rules — Activation & RAG Stress Test

## 1. Obsidian Usage Rules

- **Rule 1: Mandatory Prior Search**  
  Before answering technical queries or questions about past projects, you MUST use the search tools in the Obsidian Vault (`search_files`, `read_file`) to verify historical data. Do not rely on model memory without cross-checking against the Vault.

- **Rule 2: Automatic Decision Logging**  
  Upon generating an important design, architecture, or decision during chat, ask the user if they wish to create a summary note in the Vault. If there is no immediate response, create it automatically in Obsidian's `01_Inbox/` folder.

- **Rule 3: Source Citation**  
  When citing data extracted from Obsidian, always mention the source note's name (the file title).
## 2. File Scope & Fresh File Creation Protocol
- **SYSTEM FILES ISOLATION:** The files located in `00_System/` (e.g., `Hermes_Instructions.md`, `Obsidian_Usage_Rules.md`) are STRICTLY for agent rules and system configuration. 
  - **NEVER** append project notes, technical data, meeting logs, or conversation summaries to system files.
- **START FRESH FILES:** Whenever new technical decisions, project details, code snippet archives, or LTM entries are generated during a session:
  - ALWAYS create a **brand-new `.md` file** inside `01_Inbox/` or the specific project directory (e.g., `01_LTM/Projects/<Project_Name>/`).
  - Do NOT modify existing reference notes unless specifically requested to update a living document.

---

