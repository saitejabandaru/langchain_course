# 🚀 AI Job Search Agent (LangChain + OpenAI + Tavily)

## 📌 Overview
This project is a lightweight AI agent built using LangChain that autonomously searches for relevant job postings (e.g., new grad AI/ML roles) and returns structured results with sources.

The agent combines LLM reasoning with real-time web search to automate job discovery, eliminating manual searching and improving efficiency.

---

## ⚙️ Tech Stack
- **LangChain** – Agent orchestration  
- **OpenAI (ChatOpenAI)** – LLM reasoning engine  
- **Tavily Search API** – Real-time web search  
- **LangSmith** – Monitoring, tracing, and debugging agent workflows  
- **Pydantic** – Structured output schema  
- **Python**

---

## 🧠 How It Works
1. User provides a natural language query (e.g., "Find AI engineer jobs")
2. The LLM determines when to call external tools  
3. The agent invokes Tavily Search for real-time results  
4. Results are structured into:
   - Answer  
   - Source URLs  

This follows an **agentic (ReAct-style) workflow**, where the model reasons and takes actions using tools.

---

## 📊 Monitoring with LangSmith
This project integrates **LangSmith** to trace and debug agent behavior.

- 🔍 Tracks each agent run, including tool calls and LLM responses  
- 🧠 Visualizes reasoning steps (ReAct chain)  
- ⚠️ Helps identify failures, hallucinations, or tool misuse  
- 📈 Enables iterative improvement and evaluation of agent performance  

This makes the system more reliable and easier to debug in real-world scenarios.

---

## 🧩 Features
- 🔍 Automated job search using natural language queries  
- 🌐 Real-time data retrieval (not limited to static LLM knowledge)  
- 📄 Structured responses with source attribution  
- 📊 Observability using LangSmith  
- ⚡ Eliminates manual job browsing  

---

## 📦 Example Usage
```python
from langchain_core.messages import HumanMessage

result = agent.invoke({
    "messages": HumanMessage(
        content="Search for 5 new grad AI engineer jobs using LangChain on LinkedIn"
    )
})

print(result)
```

---

## 🛠️ Setup

### 1. Install dependencies
```bash
pip install langchain langchain-openai langchain-tavily python-dotenv
```

### 2. Set environment variables
Create a `.env` file:
```bash
OPENAI_API_KEY=your_openai_api_key
TAVILY_API_KEY=your_tavily_api_key
LANGCHAIN_API_KEY=your_langsmith_api_key
LANGCHAIN_TRACING_V2=true
```

### 3. Run the agent
```bash
python main.py
```

---

## 📈 Future Improvements
- Add filters (location, salary, company)
- Persist results in a database
- Build a frontend dashboard (React/Vue)
- Add ranking/relevance scoring
- Extend to other domains (research, news, monitoring)

---

## 🎯 Impact
- Reduces time spent on manual job searching  
- Demonstrates real-world **agentic AI workflow design**  
- Showcases integration of LLMs with tools and monitoring systems  
- Improves reliability through observability and debugging  

---

## 📬 Notes
This project highlights how LLM-powered agents can automate workflows by combining reasoning, tool usage, structured outputs, and monitoring.

---
