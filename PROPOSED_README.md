# 🌐 NetScan-IP-Geolocation-Visualizer-Streamlit-App

## 🚀 Apex Architectural Proposal & Blueprint

This document details the architectural and operational guidelines for the `NetScan-IP-Geolocation-Visualizer-Streamlit-App`, ensuring compliance with December 2025 Apex Standards.

---

<details>
<summary>🤖 **AI AGENT DIRECTIVES (APEX STANDARD 4.0)**</summary>

### 1. IDENTITY & PRIME DIRECTIVE
**Role:** You are a Senior Principal Software Architect and Master Technical Copywriter. Your mandate is to maintain and enhance this codebase to the highest professional standard.
**Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

### 2. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)
**PRIMARY SCENARIO: DATA / SCRIPTS / AI (Python)**
*   **Stack:** Python 3.10+ utilizing **uv** for dependency management, **Ruff** for static analysis and formatting (enforcing strict compliance with PEP 8 and security best practices), and **Pytest** for comprehensive testing.
*   **Architecture:** **Modular Monolith** applied to the Streamlit structure. Core logic (IP lookup handlers, data processing) must be strictly separated from the presentation layer (`pages/` or main `app.py`).
*   **Data Flow:** External API interactions (e.g., `ipapi.co`) must be encapsulated behind an **Adapter Pattern** (a dedicated `services/` module) to isolate network failures and allow for easy swapping of providers.

### 3. DEVELOPMENT STANDARDS & VERIFICATION
*   **LINTING/FORMATTING:** All Python files must be validated using `ruff check . --fix` before committing.
*   **Testing Mandate:** Unit tests (`tests/unit/`) must cover 90%+ of the data transformation and service adapter logic. Integration tests (`tests/integration/`) must verify successful Streamlit rendering hooks.
*   **VERIFICATION COMMANDS (Agent Execution):**
    bash
    # 1. Setup Environment (uv)
    uv venv
    source .venv/bin/activate
    uv sync

    # 2. Lint & Format Check (Ruff)
    ruff check .

    # 3. Run Tests (Pytest)
    pytest

    # 4. Run Application (Streamlit)
    streamlit run app.py
    

### 4. APEX PRINCIPLES ENFORCEMENT
*   **SOLID:** High adherence to Single Responsibility (SRP) in utility functions and Open/Closed (OCP) in data source adapters.
*   **DRY:** Avoid repeating API call logic or mapping schemas.
*   **YAGNI:** Only implement features explicitly required by the geolocation diagnostics mandate. Avoid speculative abstraction.

</details>

---

## 💡 BLUF: Value Proposition
This Streamlit application provides an advanced, real-time geospatial intelligence dashboard using Python, visualizing IP address data sourced from external APIs onto OpenStreetMap tiles. It serves as an indispensable utility for network forensics and location mapping.

## 🏛️ Architecture Overview (Modular Monolith in Streamlit)

The structure isolates configuration, data fetching, and presentation to maximize testability and maintainability, fitting within the Streamlit execution model.

ascii
NetScan-IP-Geolocation-Visualizer-Streamlit-App/
├── .github/
│   └── workflows/ci.yml
├── pages/                      # Streamlit pages/views
│   └── 1_Dashboard.py          
├── services/                   # Data Adapters (SOLID/Adapter Pattern)
│   ├── ip_api_adapter.py       # Interface to ipapi.co
│   └── osm_map_renderer.py     # Map rendering logic
├── core/                       # Business Logic / Utilities
│   └── validation.py
├── requirements.txt            # Dependencies (Managed by uv)
├── app.py                      # Main entry point
└── README.md


## 📋 Table of Contents
1.  [🚀 Apex Architectural Proposal & Blueprint](#-apex-architectural-proposal--blueprint)
2.  [💡 BLUF: Value Proposition](#-bluf-value-proposition)
3.  [🏛️ Architecture Overview (Modular Monolith in Streamlit)](#-architecture-overview-modular-monolith-in-streamlit)
4.  [📋 Table of Contents](#-table-of-contents)
5.  [✨ Features At A Glance](#-features-at-a-glance)
6.  [🛠️ Apex Toolchain & Development Setup](#-apex-toolchain--development-setup)
7.  [✅ Verification & CI/CD](#-verification--cicd)
8.  [⚖️ License](#-license)

## ✨ Features At A Glance
*   **Real-Time Mapping:** Interactive display of IP location on OpenStreetMap.
*   **Comprehensive Data Points:** Fetches and displays ASN, Organization, ISP, Timezone, and Currency data.
*   **Flag Visualization:** Instant display of the associated country flag for rapid identification.
*   **High Performance:** Optimized data fetching pipeline leveraging Python concurrency for minimal UI lag.

## 🛠️ Apex Toolchain & Development Setup
This project adheres strictly to the Late 2025 Python standards outlined in the Agent Directives.

### Prerequisites
Ensure you have Python 3.10+ installed.

### Setup Commands
bash
# 1. Clone the repository
git clone https://github.com/chirag127/NetScan-IP-Geolocation-Visualizer-Streamlit-App.git
cd NetScan-IP-Geolocation-Visualizer-Streamlit-App

# 2. Environment Management (using uv)
uv venv
source .venv/bin/activate

# 3. Install Dependencies
uv sync  # Installs from requirements.txt


### Development Scripts
| Command | Description |
| :--- | :--- |
| `uv run dev` | Installs and runs the application via Streamlit. |
| `ruff check .` | Runs static analysis and lints the codebase. |
| `pytest` | Executes unit and integration tests. |
| `uv lock` | Updates the frozen dependency lock file. |

## ✅ Verification & CI/CD
Continuous Integration is managed via the standard `ci.yml` workflow, enforcing code quality checks before any merge.

**Key Principles Enforced:**
1.  **DRY:** Data fetching schemas are abstracted in `services/`.
2.  **SOLID (SRP):** Map rendering logic is separate from IP data parsing.

## ⚖️ License
This project is released under the **Creative Commons Attribution-NonCommercial 4.0 International License**.

---

*Authored by Apex Technical Authority on behalf of chirag127.*
