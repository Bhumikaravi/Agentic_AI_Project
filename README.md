<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=311042,6B21A8,9333EA&height=220&section=header&text=Smart%20Inventory%20Planning%20Assistant&fontSize=38&fontColor=ffffff&fontAlignY=38&desc=Autonomous%20Multi-Agent%20Retail%20Restocking%20System%20with%20LLM%20Reasoning&descSize=16&descAlignY=62&descAlign=50" width="100%" alt="Smart Inventory Planning Assistant Header Banner"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Architecture-Multi--Agent%20System-8A2BE2?style=for-the-badge&logo=probot" alt="Architecture"/> <img src="https://img.shields.io/badge/Pattern-Planner%20Pattern-9333EA?style=for-the-badge" alt="Pattern"/> <img src="https://img.shields.io/badge/Backend-Python%20%7C%20Flask-3776AB?style=for-the-badge&logo=python" alt="Flask"/> <img src="https://img.shields.io/badge/Database-SQLite-003B57?style=for-the-badge&logo=sqlite" alt="SQLite"/> <img src="https://img.shields.io/badge/License-MIT-green?style=for-the-badge" alt="License"/>
</p>


## 📌 Table of Contents
- [📖 Executive Summary](#-executive-summary)
- [✨ Key Features & Capabilities](#-key-features--capabilities)
- [🏗️ System Architecture & Workflow](#️-system-architecture--workflow)
- [🛠️ Tech Stack Breakdown](#️-tech-stack-breakdown)
- [⚙️ Reproducible Quickstart & Setup](#️-reproducible-quickstart--setup)
- [📂 Project Directory Layout](#-project-directory-layout)
- [👩‍💻 Author & Contributions](#-author--contributions)

---

## 📖 Executive Summary
### Problem Statement
Small and medium brick-and-mortar retailers suffer significant financial losses annually due to manual stock estimation. Inaccurate replenishment triggers either costly stockouts (lost revenue) or dead overstock (blocked working capital).

### Motivation & Solution Overview
The Smart Inventory Planning Assistant automates store replenishment using an intelligent Multi-Agent workflow built around the **Planner Pattern**. Specialized autonomous agents calculate sales velocity, enforce budget constraints, handle stock anomalies, and generate natural-language restocking justifications via local LLM reasoning.

---

## ✨ Key Features & Capabilities
- **Multi-Agent Coordination:** Orchestrates 5 specialized agents collaborating via typed message passing:
  - **Planner Agent:** Calculates daily sales velocity and generates prioritized restocking proposals.
  - **Executor Agent:** Validates replenishment orders against store budget limits and commits database updates.
  - **Feedback Agent:** Evaluates system accuracy and identifies stock deviations.
  - **Replanner Agent:** Dynamically recalibrates replenishment quantities when supply anomalies arise.
  - **LLM Agent:** Generates natural language reasoning and vendor replenishment summaries.
- **Dual Operating Modes:** Operates in offline rule-based mode and online LLM-augmented mode.
- **Responsive Dashboard:** Flask web interface displaying real-time inventory levels, replenishment tables, and agent decisions.
- **Academic Verification:** Verified capstone project at Alliance University accompanied by full project report and recorded video demo.

---

## 🏗️ System Architecture & Workflow
```mermaid
flowchart TD
    UI[Flask Web Dashboard] --> Controller[app.py Orchestrator]
    Controller --> DB[(SQLite inventory.db)]
    Controller --> Planner[Planner Agent: Velocity & Stock Math]
    Planner --> Replanner{Anomalies Detected?}
    Replanner -- Yes --> ReplannerAgent[Replanner Agent]
    Replanner -- No --> Executor[Executor Agent: Budget & Order Check]
    Executor --> LLM[LLM Agent: Restock Explanation & Summaries]
    LLM --> Feedback[Feedback Agent: Validation]
    Feedback --> UI
```

---

## 🛠️ Tech Stack Breakdown
| Layer | Technologies |
|---|---|
| **Programming Language** | Python 3.10+ |
| **Agent Framework** | Custom Multi-Agent Architecture (Planner Pattern) |
| **Web & Backend** | Flask, Jinja2 Templates, HTML5/CSS3 |
| **Database & Persistence** | SQLite (`inventory.db`) |
| **LLM Integration** | Local Open-Source LLM (Ollama / Llama) |
| **Documentation & Assets** | Architecture Report (PDF), Demonstration Video (MP4) |

---

## ⚙️ Reproducible Quickstart & Setup
### Prerequisites
- Python 3.10 or higher
- Git

### Installation Steps
```bash
# 1. Clone the repository
git clone https://github.com/Bhumikaravi/Agentic_AI_Project.git
cd Agentic_AI_Project/Smart_Inventory_Planning_System

# 2. Set up virtual environment
python -m venv .venv
# On Windows:
.venv\Scripts\activate
# On Linux/macOS:
source .venv/bin/activate

# 3. Install dependencies
pip install flask

# 4. Launch the application
python app.py
```
Open `http://127.0.0.1:5000` in your browser to interact with the multi-agent dashboard.

---

## 📂 Project Directory Layout
```text
Agentic_AI_Project/
├── DEMO VIDEO.mp4                           # Complete recorded walkthrough
├── Final_Report_of_Agentic_AI_Project.pdf   # Academic project report (Alliance University)
├── LICENSE                                  # MIT License
├── Smart_Inventory_Planning_System/
│   ├── app.py                              # Flask Web Server & Orchestrator
│   ├── inventory.py                        # Inventory business logic & schema
│   ├── inventory.db                        # SQLite database
│   ├── agents/
│   │   ├── planner_agent.py                # Restock planning algorithm
│   │   ├── executor_agent.py               # Order execution & validation
│   │   ├── feedback_agent.py               # Accuracy verification
│   │   ├── replanner_agent.py              # Dynamic fallback replanning
│   │   └── llm_agent.py                    # LLM reasoning generator
│   └── templates/
│       ├── index.html                      # Dashboard UI
│       └── actions_result.html             # Agent output view
└── README.md
```

---

## 👩‍💻 Author & Contributions
Developed by **Bhumika Ravi** ([@Bhumikaravi](https://github.com/Bhumikaravi)), Bachelor of Computer Applications (BCA) at **Alliance University, Bengaluru**.

- 💻 **GitHub Profile:** [github.com/Bhumikaravi](https://github.com/Bhumikaravi)
- 🔗 **LinkedIn:** [linkedin.com/in/bhumika-ravi-b5a01b326](https://www.linkedin.com/in/bhumika-ravi-b5a01b326/)
- 📬 **Email Contact:** [bhumikaravi2006@gmail.com](mailto:bhumikaravi2006@gmail.com)

---

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=311042,6B21A8,9333EA&height=100&section=footer" width="100%" alt="Footer Banner"/>
</p>
