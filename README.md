AI Agent System with Automated Testing & Sandbox Execution
📌 Overview

This project implements an AI Agent System that can:

Process user inputs intelligently
Execute tasks using tools (calculator, Python execution, search)
Use Azure OpenAI (LLM) for reasoning
Perform automated testing without manual intervention
Run in a sandboxed environment using Docker
🎯 Objective

To build a production-ready AI agent system that is:

Scalable
Testable
Secure
Modular
🏗️ Architecture
Client (Test Runner / UI)
        ↓
FastAPI (API Layer)
        ↓
LangGraph Agent (Core)
        ↓
Planner (Decision Making)
        ↓
Worker (Execution)
        ↓
Tools (Calculator / Search)
        ↓
Response
        ↓
Validator (Testing Layer)
🔗 How the Agent Works
Client sends request
Example: "calculate (5*10)+20"
FastAPI receives request
Acts as communication layer
Graph (Agent) executes
Planner decides what to do
Worker executes the task
Tools perform execution
Calculator / Python / Search
Response returned to client
🤖 Agent Design

This project follows a Tool-Based Agent Architecture:

LLM (Azure OpenAI) → reasoning
Planner → decision making
Worker → execution
Tools → perform tasks
⚙️ Features
✅ Tool-based execution (calculator, search)
✅ Azure OpenAI integration
✅ LangGraph-based agent orchestration
✅ FastAPI backend
✅ Automated testing system
✅ Docker sandbox environment
🧪 Automated Testing
🔥 Why?

Manual testing is slow and unreliable.

✅ Solution

A test runner automatically validates outputs:

python tests/test_runner.py
🔁 Testing Flow
Test Case → API → Agent → Response → Validator → PASS/FAIL
📌 Example Test Case
{
  "input": "calculate (5*10)+20",
  "expected": "70"
}
✅ Validation System
🟢 Simple Validator
Rule-based matching
Fast and free
🔴 LLM Validator
Uses Azure OpenAI
Checks semantic correctness
🐳 Sandbox Concept
🟢 Demo Sandbox (Current)
Built using Docker
Used for development & testing
🔴 Execution Sandbox (Industry)
Fully isolated environment
Secure code execution
Used in production systems
🆚 Demo vs Execution Sandbox
Feature	Demo Sandbox	Execution Sandbox
Purpose	Testing	Production
Security	Medium	High
Scale	Local	Cloud
Tools	Docker	Kubernetes
🚀 Why Docker?
Environment consistency
Isolation
Easy deployment
Reproducibility
🔐 Why Execution Sandbox Matters
Prevents malicious code execution
Protects system resources
Enables safe AI agent operations
📂 Project Structure
app/
 ├── agents/
 │    ├── planner.py
 │    ├── worker.py
 ├── tools/
 │    ├── tools.py
 ├── graph.py
 ├── api/
 │    ├── main.py

tests/
 ├── test_runner.py
 ├── test_cases.py
 ├── validator.py
⚡ Installation & Setup

# Clone repo
git clone <your-repo>

# Install dependencies
pip install -r requirements.txt

# Run server
uvicorn app.api.main:app --reload

# Run tests
python tests/test_runner.py

🔑 Environment Variables
AZURE_OPENAI_API_KEY=your_key
AZURE_OPENAI_ENDPOINT=your_endpoint
AZURE_OPENAI_DEPLOYMENT=your_deployment
🧠 Key Learnings
LLM is not an execution engine
Tools perform actual execution
Agents require structured orchestration
Automated testing is essential for reliability
🔥 Industry Relevance

This system reflects real-world practices:

Agent orchestration (LangGraph)
Tool-based AI systems
Automated validation pipelines
Sandbox-based execution
API-driven architecture
🚀 Future Improvements
Multi-step reasoning agent
Memory (conversation history)
Dynamic tool selection using LLM
UI (chat interface)
Kubernetes deployment
🏁 Conclusion

This project demonstrates a complete AI agent pipeline with:

Intelligent decision-making
Safe execution
Automated testing
Scalable architecture
