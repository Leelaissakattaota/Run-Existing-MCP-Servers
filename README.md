# 🌐 Run Existing MCP Servers: STDIO & HTTP Protocols

![Python](https://img.shields.io/badge/Python-3.12+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastMCP](https://img.shields.io/badge/Framework-FastMCP-orange?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![GitHub Username](https://img.shields.io/badge/Maintainer-Leelaissakattaota-blue?style=for-the-badge&logo=github)

An advanced exploration into the **Model Context Protocol (MCP)**, demonstrating how to bridge Large Language Models (LLMs) with external tools and documentation using both local and remote transport protocols.

---

## 🚀 Project Overview

MCP servers are to LLMs what the App Store was to mobile phones. This project focuses on using the **FastMCP** library to connect an application to MCP servers, allowing an LLM to retrieve real-time coding documentation and library insights.

### ✨ Key Objectives
* **STDIO Transport:** Configure local connections using Standard Input/Output via subprocesses.
* **HTTP Transport:** Implement remote connections to hosted MCP servers.
* **Context7 Integration:** Fetch and query up-to-date documentation for libraries like `pandas`, `fastmcp`, and `scikit-learn`.
* **Asynchronous Operations:** Utilize `async/await` for non-blocking tool execution.

---

## 🛠️ Architecture

The project follows a modular client-server bridge architecture:

```mermaid
graph LR
    A[Python Client] <--> B{Transport Bridge}
    B <--> C[Local STDIO Server]
    B <--> D[Remote HTTP Server]
