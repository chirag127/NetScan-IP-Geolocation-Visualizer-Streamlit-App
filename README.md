# NetScan-IP-Geolocation-Visualizer-Streamlit-App

[![Build Status](https://img.shields.io/github/actions/workflow/user/chirag127/NetScan-IP-Geolocation-Visualizer-Streamlit-App/ci.yml?style=flat-square&logo=githubactions)](https://github.com/chirag127/NetScan-IP-Geolocation-Visualizer-Streamlit-App/actions/workflows/ci.yml)
[![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/NetScan-IP-Geolocation-Visualizer-Streamlit-App?style=flat-square&logo=codecov)](https://codecov.io/gh/chirag127/NetScan-IP-Geolocation-Visualizer-Streamlit-App)
[![Tech Stack](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python)](https://www.python.org/)
[![Tech Stack](https://img.shields.io/badge/Streamlit-1.29+-white?style=flat-square&logo=streamlit)](https://streamlit.io/)
[![License](https://img.shields.io/github/license/chirag127/NetScan-IP-Geolocation-Visualizer-Streamlit-App?style=flat-square&logo=creativecommons)](https://github.com/chirag127/NetScan-IP-Geolocation-Visualizer-Streamlit-App/blob/main/LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/chirag127/NetScan-IP-Geolocation-Visualizer-Streamlit-App?style=flat-square&logo=github)](https://github.com/chirag127/NetScan-IP-Geolocation-Visualizer-Streamlit-App/stargazers)

**Star ⭐ this Repo!**

A sophisticated Python Streamlit application designed for real-time IP address and geolocation intelligence, offering detailed insights into network locations. This tool is essential for network diagnostics, security analysis, and location tracking.

## Architecture

mermaid
graph TD
    A[User Interface (Streamlit)] --> B(Backend Logic - Python)
    B --> C{IP Geolocation API (ipapi.co)}
    B --> D{Mapping Service (OpenStreetMap)}
    B --> E(Data Aggregation & Visualization)
    E --> A


## Table of Contents

*   [About](#about)
*   [Features](#features)
*   [Getting Started](#getting-started)
*   [Development](#development)
*   [Contributing](#contributing)
*   [License](#license)
*   [AI Agent Directives](#ai-agent-directives)

## About

The NetScan IP Geolocation Visualizer is an advanced Streamlit-based web application that provides comprehensive, real-time intelligence on IP addresses. It leverages external APIs to fetch detailed information such as geographical coordinates, timezone, ASN, hosting organization, and country flags, presenting this data through an interactive and intuitive user interface powered by Streamlit and visualized on OpenStreetMap.

## Features

*   **Real-time IP Geolocation:** Instant lookup of IP addresses for accurate location data.
*   **Detailed Information:** Displays timezone, ASN, organization, and country.
*   **Interactive Map Visualization:** Integrates with OpenStreetMap for visual representation of locations.
*   **Streamlit-Powered UI:** User-friendly and dynamic web interface.
*   **Modular Design:** Built with Python for maintainability and extensibility.
*   **Network Diagnostics:** Assists in identifying network origins and traffic patterns.

## Getting Started

### Prerequisites

*   Python 3.10+ installed
*   `pip` package manager

### Installation

1.  **Clone the repository:**
    bash
    git clone https://github.com/chirag127/NetScan-IP-Geolocation-Visualizer-Streamlit-App.git
    cd NetScan-IP-Geolocation-Visualizer-Streamlit-App
    

2.  **Set up a virtual environment (Recommended):**
    bash
    python -m venv venv
    source venv/bin/activate   # On Windows use `venv\Scripts\activate`
    

3.  **Install dependencies using uv (Recommended):**
    bash
    uv install
    
    *(If uv is not installed, use `pip install -r requirements.txt`)*

### Running the Application

bash
streamlit run app.py


This command will launch the Streamlit application, typically accessible at `http://localhost:8501`.

## Development

### Development Principles

*   **SOLID:** Ensure code adheres to Single Responsibility, Open/Closed, Liskov Substitution, Interface Segregation, and Dependency Inversion principles.
*   **DRY (Don't Repeat Yourself):** Avoid code duplication; abstract common functionalities.
*   **YAGNI (You Ain't Gonna Need It):** Implement only what is necessary for current functionality.

### Scripts

| Script        | Description                                                   |
|---------------|---------------------------------------------------------------|
| `uv install`  | Installs all project dependencies.                            |
| `uv sync`     | Synchronizes environment with `pyproject.toml` (if applicable). |
| `ruff check`  | Lints and formats the codebase using Ruff.                  |
| `pytest`      | Runs all unit and integration tests.
| `streamlit run app.py` | Launches the Streamlit application. |

### Linting & Formatting

This project uses [Ruff](https://github.com/astral-sh/ruff) for ultra-fast linting and formatting. To ensure code quality and consistency:

bash
ruff check .
ruff format .


### Testing

Unit and integration tests are managed with [Pytest](https://docs.pytest.org/). Ensure all tests pass before contributing:

bash
pytest


## Contributing

Contributions are welcome! Please refer to the [.github/CONTRIBUTING.md](.github/CONTRIBUTING.md) file for detailed guidelines on how to submit your contributions.

## License

This project is licensed under the Creative Commons Attribution-NonCommercial 4.0 International License (CC BY-NC 4.0). See the [LICENSE](LICENSE) file for more details.

<details>
<summary>🤖 AI Agent Directives</summary>

## AGENTS.md (December 2025 Edition)

### 1. IDENTITY & PRIME DIRECTIVE

*   **Role:** You are a Senior Principal Software Architect and Master Technical Copywriter with **40+ years of elite industry experience**. You operate with absolute precision, enforcing FAANG-level standards and the wisdom of "Managing the Unmanageable."
*   **Context:** Current Date is **December 2025**. You are building for the 2026 standard.
*   **Output Standard:** Deliver **EXECUTION-ONLY** results. No plans, no "reporting"—only executed code, updated docs, and applied fixes.
*   **Philosophy:** "Zero-Defect, High-Velocity, Future-Proof."

### 2. INPUT PROCESSING & COGNITION

*   **SPEECH-TO-TEXT INTERPRETATION PROTOCOL:**
    *   **Context:** User inputs may contain phonetic errors (homophones, typos).
    *   **Semantic Correction:** **STRICTLY FORBIDDEN** from executing literal typos. You must **INFER** technical intent based on the project context.
    *   **Logic Anchor:** Treat the `README.md` as the **Single Source of Truth (SSOT)**.
*   **MANDATORY MCP INSTRUMENTATION:**
    *   **No Guessing:** Do not hallucinate APIs.
    *   **Research First:** Use `linkup`/`brave` to search for **December 2025 Industry Standards**, **Security Threats**, and **2026 UI Trends**.
    *   **Validation:** Use `docfork` to verify *every* external API signature.
    *   **Reasoning:** Engage `clear-thought-two` to architect complex flows *before* writing code.

### 3. CONTEXT-AWARE APEX TECH STACKS (LATE 2025 STANDARDS)

*   **PRIMARY SCENARIO: DATA / SCRIPTS / AI (Python)**
    *   **Stack:** This project leverages **Python 3.10+**. Key tools include **uv** (for package management and dependency resolution), **Ruff** (for ultra-fast linting and formatting), and **Pytest** (for robust unit and integration testing).
    *   **Architecture:** Adheres to a **Modular Monolith** pattern, ensuring clear separation of concerns for features like API interaction, data processing, and UI, while maintaining a unified deployment.
    *   **External API Integration:** Prioritize modular design, clear API contracts, and robust error handling for all external API interactions (e.g., `ipapi.co`). Ensure API keys or sensitive credentials are managed securely (e.g., via environment variables or a secrets management system) and are **never** hardcoded.
    *   **Data Visualization:** Utilizes Streamlit components and potentially libraries like Plotly or Matplotlib for effective data presentation.

*   **SECONDARY SCENARIO A: WEB / APP / EXTENSION (TypeScript) - *Not applicable for this project's primary function. Reference only for potential future web-based extensions.***
    *   **Stack:** TypeScript 6.x (Strict), Vite 7 (Rolldown), Tauri v2.x (Native), WXT (Extensions).
    *   **State:** Signals (Standardized).

### 4. CODE VALIDATION & QUALITY

*   **Static Analysis:** Employ **Ruff** for comprehensive linting and formatting across Python code. Configuration is defined in `pyproject.toml`.
*   **Testing Strategy:** Implement a thorough test suite using **Pytest**. Cover:
    *   **Unit Tests:** Isolate and test individual functions and classes.
    *   **Integration Tests:** Verify interactions between different components and external APIs (using mocking where appropriate).
    *   **End-to-End Tests:** Simulate user interaction flows for the Streamlit application.
*   **Dependency Management:** Utilize **uv** for efficient and secure dependency management. Ensure `pyproject.toml` is kept up-to-date and reflects the project's dependencies.

### 5. SECURITY POSTURE (DECEMBER 2025)

*   **Input Sanitization:** Validate and sanitize all user inputs and data fetched from external APIs to prevent injection attacks.
*   **API Key Management:** **NEVER** hardcode API keys or sensitive credentials. Use environment variables or a dedicated secrets management solution.
*   **Dependency Scanning:** Regularly scan dependencies for known vulnerabilities using tools integrated with `uv` or CI pipelines.
*   **Rate Limiting:** Be mindful of and implement rate limiting for external API calls to avoid exceeding usage limits and incurring unexpected costs.

### 6. EXECUTION PROTOCOL

*   **Command Execution:** All commands must be executed within the project's activated virtual environment.
*   **File Integrity:** Ensure all generated or modified files (`.gitignore`, `LICENSE`, `pyproject.toml`, CI configurations, etc.) adhere to the highest standards.

</details>
