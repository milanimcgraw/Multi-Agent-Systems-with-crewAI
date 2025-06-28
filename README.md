# Build a Database Agent with Azure OpenAI

## ⚙️ Project Overview

In this repository, we'll build intelligent, multi-agent AI crews utilizing an open source library, [crewAI](https://github.com/crewAIInc/crewAI), designed for building multi-agent systems.  We implement key components within each agentic crew that collaborate to solve and automate complex real-world tasks. Each workflow demonstrates how a team of LLM-powered agents can outperform a single model in business automation tasks. 

#### **Key components include:** 
- **Role-playing:** Assign specialized roles to agents 
- **Memory:** Provide agents with short-term, long-term, and shared memory
- **Tools:** Assign pre-built and custom tools to each agent (e.g. for web search)
- **Focus:** Break down the tasks, goals, and tools and assign multiple AI agents for better performance
- **Guardrails:** Effectively handle errors, hallucinations, and infinite loops
- **Cooperation:** Perform tasks in series, in parallel, and hierarchically
role-based agents with memory, tools, and hierarchical task execution.


![GIF with slides from different lessons](https://ci3.googleusercontent.com/meips/ADKq_Nb6Q6FlA10rXNqHAjMcqMXZ0HonUtZmD-zjTknvNciDZIK3Kf5bork032gr5dSVln120iS4KEuuKF_GH_0l60pgkuOt5zz8UCBOCZfob89xjNoeNbNuNmnfmbDlkaQEZuBz5D8gWVKxnpqtba2IMijFUjBGYz1XVrQrT2w8fT4XP6F_6UCVol2Msf5qk5RH96pn3BNro-x01rJAGs5z=s0-d-e1-ft#https://info.deeplearning.ai/hs-fs/hubfs/Launch%20email%20GIFs%20(18).gif?width=1120&upscale=true&name=Launch%20email%20GIFs%20(18).gif)
## 🚀 crewAI 

[CrewAI](https://github.com/CrewAIInc/crewAI) is a high-performance, open-source Python framework for orchestrating **multi-agent AI systems**. Designed from the ground up without dependencies on LangChain or other libraries, CrewAI delivers both **simplicity for rapid prototyping** and **fine-grained control for production workflows**. 
CrewAI is built around two foundational concepts that enable powerful and scalable multi-agent systems:

- **Crews**: Structured groups of AI agents, each assigned a specific role and objective. Crews work together autonomously to divide, coordinate, and accomplish complex tasks through collaborative reasoning.
- **Flows**: Flexible, event-driven execution pipelines that control the sequence and logic of tasks across agents—ideal for building reliable, production-grade automations with stateful control.

### ✨ Why CrewAI?

- **Independent & Lightweight**: Built from scratch—no LangChain required.
- **Optimized for Speed**: Lightning-fast execution with minimal resource consumption.
- **Flexible Agent Design**: Customize behavior at every level, from individual prompts to crew-wide strategies.
- **Enterprise Ready**: Includes [Crew Control Plane](https://www.crewai.com/) for observability, security, and integration at scale.
- **Thriving Community**: Over 100,000 developers trained via [learn.crewai.com](https://learn.crewai.com).

>### 🛠️ Learn More
>- [📚 Multi-Agent Systems with CrewAI Course](https://learn.deeplearning.ai/courses/multi-ai-agent-systems-with-crewai)
>- [📘 Official Documentation](https://docs.crewai.com/)
>- [🔁 CrewAI GitHub Repo](https://github.com/CrewAIInc/crewAI)
>- [🌐 Start Free Cloud Trial](https://app.crewai.com/)

## 🤖 Agent Crews

| **Multi-Agent System** | **Description** | **Agents** |
|------------------------|-----------------|------------|
| 📈 **Financial Analysis** | A crew that performs end-to-end financial analysis and trading strategy development. Agents work collaboratively to monitor market data, design risk-aware strategies, plan optimal execution, and assess potential trade risks—leveraging statistical modeling, user preferences, and structured decision-making to deliver actionable investment insights. | `Data Analyst`<br>`Trading Strategy Developer`<br>`Trade Advisor`<br>`Risk Advisor` |
| 📄 **Job Applications** | A crew that automates personalized job application workflows using structured collaboration and role-specific expertise. Each agent contributes to crafting resumes, analyzing job descriptions, and preparing interview guidance—ensuring alignment with the target role and maximizing candidate competitiveness. | `Tech Job Researcher`<br>`Personal Profiler for Engineers`<br>`Resume Strategist for Engineers`<br>`Engineer Interview Preparer` |
| 🧠 **Research Writing** | A crew that streamlines the content creation process from planning to publishing. Agents work in sequence to brainstorm, draft, and revise technical articles—combining structured creativity, subject-matter coherence, and editing precision for high-quality outputs. | `Planner`<br>`Writer`<br>`Editor` |
| 🎧 **Customer Support** | A crew that handles end-to-end customer support resolutions by leveraging crewAI’s tool integrations, structured agent collaboration, and memory components. Each agent is assigned a distinct role in the support lifecycle, allowing them to collectively manage customer inquiries, retrieve relevant policies, and ensure clarity, consistency, and resolution quality. | `Senior Support Representative`<br>`Quality Assurance Agent` |
| 📣 **Customer Outreach** | A crew that orchestrates targeted customer outreach by combining strategy, copywriting, and execution. Each agent operates in sync to design campaigns, generate personalized messaging, and manage delivery schedules—enabling scalable, efficient engagement workflows. | `Sales Representative`<br>`Lead Sales Representative` |
| 🗓️ **Event Planning** | A crew that streamlines event planning by managing venue logistics, marketing tasks, and coordination workflows. Each agent performs a defined role—such as booking, communications, or documentation—using shared tools and memory to deliver structured outputs like venue data and campaign summaries. | `Venue Coordinator`<br>`Logistics Manager`<br>`Marketing Communications Agent` |

## 🛠️ Technical Stack
- **Agent Framework**: [`crewAI`](https://github.com/joaomdmoura/crewAI) `v0.28.8`, [`crewAI Tools`](https://github.com/joaomdmoura/crewAI-tools) `v0.1.6`
- **LLM Provider**: OpenAI (GPT-4o, GPT-3.5-turbo)
- **Agent Utilities**: `langchain`, `langchain_community v0.0.29` (tool loading, routing, memory)
- **Search Integration**: Serper.dev for web search and grounding
- **Environment Management**: `.env` with `python-dotenv`, terminal exports
- **Interface**: Jupyter Notebook
- **Setup & Dependencies**: `requirements.txt`, pip, Python 3.11+

## ⚙️ Dependencies
Dependencies are listed in `requirements.txt`. Key packages:
- **openai**: Access OpenAI’s GPT models including GPT-4o
- **crewai**: Orchestrate multi-agent workflows using role-based collaboration, tools, and memory
- **crewai-tools**: Built-in tools and memory support for crewAI agents
- **langchain**: Framework for agent routing, memory, and tool execution
- **langchain-community**: Community-maintained integrations for tools and agents

## 📁 Directory Overview

Each subfolder contains a complete multi-agent system workflow powered by [`crewAI`](https://github.com/joaomdmoura/crewAI). These notebooks are organized by use case, with supporting markdowns and datasets included per project.

| Folder | Notebook | Supporting Files |
|--------|----------|------------------|
| **Customer Outreach Campaigns/** | `multi-agent-customer-outreach.ipynb` | `enterprise_solutions_framework.md`, `small_business_engagement.md`, `tech_startups_outreach.md` |
| **Customer Support/** | `multi-agent-customer-support.ipynb` | _(none)_ |
| **Event Planning/** | `multi-agent-eventplanning.ipynb` | `marketing_report.md`, `venue_details.json` |
| **Financial Analysis/** | `multi-agent-collab-financial.ipynb` | _(none)_ |
| **Job Application/** | `multi-agent-resume-tailoring.ipynb` | `fake_resume.md`, `interview_materials.md`, `tailored_resume.md` |
| **Research Writing/** | `multi-agent-research-writing.ipynb` | _(none)_ |

## ⚙️ Getting Started
**To run the database agent workflows in this repository:**
### 1. Clone the Repository
```bash
git clone https://github.com/milanimcgraw/Multi-Agent-Systems-with-crewAI.git
cd Multi-Agent-Systems-with-crewAI
```
### 2. Install Dependencies
```bash
pip install -r requirements.txt
```
**or**
```bash
pip install crewai==0.28.8 crewai_tools==0.1.6 langchain langchain_community==0.0.29
openai
```
### 3. Set Up API Keys (via .env or Terminal)

**🗂️ If using an `.env` file:**
```python
# OpenAI
OPENAI_API_KEY=your-openai-api-key-here
OPENAI_MODEL_NAME=gpt-3.5-turbo

# Serper.dev
SERPER_API_KEY=your-serper-api-key-here
```
**Then load them in your notebook using**
```python
from utils import get_openai_api_key, get_serper_api_key

openai_key = get_openai_api_key()
serper_key = get_serper_api_key()
```
**⚡ Export from Terminal (for quick setup)**

To connect your application to Azure OpenAI, you'll need to set the following environment variables:

```bash
# OpenAI Key
export OPENAI_API_KEY="your_openai_key_here"

# Serper.dev Key
export SERPER_API_KEY="your_serper_api_key_here"
```
**Use in Python code:**
```python
import os

openai_key = os.getenv("OPENAI_API_KEY")
serper_key = os.getenv("SERPER_API_KEY")
```
>⚠️ ⚠️ Be sure to replace all placeholder values with your real credentials. Never commit .env files or API keys to source control.

### 4. Launch Jupyter Notebook
Start the notebook environment to explore the agent workflows:
```bash
jupyter notebook
```
Then run a notebook! 

## ⚙️ License
This project is released under MIT license. 

> ## 📌 Credits
> 📦  This project implements workflows from the [Multi-Agent Systems with crewAI](https://learn.deeplearning.ai/courses/multi-ai-agent-systems-with-crewai) course taught by João Moura (founder and CEO of crewAI), offered through [DeepLearning.AI](https://www.deeplearning.ai/short-courses/). While the original instructional materials provided foundational examples, this implementation has been customized and extended.
