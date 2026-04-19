# 🛠️ Coder Buddy

**Coder Buddy** is an AI-powered coding assistant built with [LangGraph](https://github.com/langchain-ai/langgraph). It works like a multi-agent development team that can take a natural language request and transform it into a complete, working project — file by file — using real developer workflows.

---

## ✨ Features

- 🤖 **Multi-Agent Architecture** – Leverages specialized agents for planning, architecting, and coding
- 📝 **Natural Language Requests** – Simply describe what you want, and Coder Buddy builds it
- 🔄 **Iterative Development** – Breaks complex projects into manageable tasks with proper context
- 💾 **File Generation** – Creates and manages project files automatically
- 🛠️ **Tool Integration** – Agents use real developer workflows and best practices
- 🚀 **Ready-to-Run Projects** – Generated projects are immediately functional

---

## 🏗️ Architecture

The Coder Buddy system consists of three main agents:

- **Planner Agent** – Analyzes your natural language request and generates a detailed, step-by-step project plan
- **Architect Agent** – Breaks down the plan into specific engineering tasks with explicit context for implementation
- **Coder Agent** – Implements each task, writes code directly into files, and uses available tools like a real developer

<div style="text-align: center;">
    <img src="resources/coder_buddy_diagram.png" alt="Coder Buddy Agent Architecture" width="90%"/>
</div>

---

## 🚀 Getting Started

### Prerequisites

Before you begin, ensure you have the following:

- **Python 3.8+** installed on your system
- **uv package manager** – [Installation guide](https://docs.astral.sh/uv/getting-started/installation/)
- **Groq API Key** – Create a free account at [Groq Console](https://console.groq.com/keys)

### ⚙️ Installation and Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/tiirth22/CoderBuddy.git
   cd coder-buddy
   ```

2. **Create Virtual Environment**
   ```bash
   uv venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install Dependencies**
   ```bash
   uv pip install -e .
   ```

4. **Configure Environment Variables**
   - Copy the `.sample_env` file to create a `.env` file:
     ```bash
     cp .sample_env .env
     ```
   - Edit `.env` and add your Groq API key:
     ```
     GROQ_API_KEY=your_api_key_here
     ```

5. **Run Coder Buddy**
   ```bash
   python main.py
   ```

---

## 📚 Usage Examples

Coder Buddy can generate various types of projects. Here are some example prompts:

### Web Applications
- "Create a to-do list application using HTML, CSS, and JavaScript"
- "Create a simple calculator web application with a modern UI"
- "Build a weather app that fetches data from a weather API"

### Backend Projects
- "Create a simple blog API in FastAPI with SQLite database"
- "Build a REST API for managing a task management system"
- "Create a Flask application with user authentication"

### Data Projects
- "Create a Python script that scrapes product data and stores it in a CSV"
- "Build a data analysis dashboard using Pandas and Matplotlib"

---

## 📂 Project Structure

```
coder-buddy/
├── main.py                          # Entry point of the application
├── pyproject.toml                   # Project dependencies and configuration
├── .env                             # Environment variables (create from .sample_env)
├── .sample_env                      # Sample environment file
├── agent/                           # AI agent implementations
│   ├── __init__.py
│   ├── graph.py                     # LangGraph workflow definition
│   ├── states.py                    # Agent state definitions
│   ├── prompts.py                   # Prompt templates for agents
│   └── tools.py                     # Tool definitions for agents
├── pre_generated_project_calculator/ # Example: Calculator project
├── pre_generated_project_todo_app/  # Example: Todo app project
└── resources/                       # Documentation and diagrams
    ├── coder_buddy_diagram.mmd
    └── coder_buddy_diagram.png
```

---

## 🔧 Configuration

### Environment Variables

The `.env` file should contain the following:

```env
GROQ_API_KEY=your_groq_api_key_here
```

### Customization

You can customize the behavior by modifying:
- `agent/prompts.py` – Adjust agent prompts and instructions
- `agent/tools.py` – Add or modify available tools for agents
- `main.py` – Modify the flow and configuration

---

## 🎯 How It Works

1. **Input** – User provides a natural language description of the desired project
2. **Planning** – The Planner Agent analyzes the request and creates a detailed plan
3. **Architecture** – The Architect Agent breaks down the plan into implementable tasks
4. **Coding** – The Coder Agent implements each task and generates project files
5. **Output** – A complete, functional project is created and ready to use

---

## 🆘 Troubleshooting

### Issue: "GROQ_API_KEY not found"
**Solution:** Ensure your `.env` file is in the project root directory and contains your valid Groq API key.

### Issue: "Module not found" errors
**Solution:** Make sure you've activated the virtual environment and installed dependencies:
```bash
source .venv/bin/activate  # or .venv\Scripts\activate on Windows
uv pip install -e .
```

### Issue: Generated code has syntax errors
**Solution:** Review the generated files and fix any issues. You can also refine your prompt to be more specific about requirements.

---

## 📝 Example Pre-Generated Projects

This repository includes two example projects:

1. **Calculator** (`pre_generated_project_calculator/`) – A functional web calculator
2. **Todo App** (`pre_generated_project_todo_app/`) – A simple task management application

These serve as examples of what Coder Buddy can generate.

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues and pull requests to help improve Coder Buddy.

---

## 📄 License

Copyright © Codebasics Inc. All rights reserved.

---

## 🙋 Support

For questions, issues, or feature requests, please open an issue on GitHub or contact the development team.

---

**Built by Tirth J Dalal
