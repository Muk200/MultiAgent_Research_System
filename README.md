# MultiAgent_Research_System


An AI-powered multi-agent research system designed to automate the process of researching a given topic, collecting relevant information, and generating a structured research response.

The project uses **LangGraph and LangChain** to coordinate multiple AI agents and **Streamlit** to provide an interactive user interface.

## Features

* 🤖 Multi-agent AI research workflow
* 🔎 Automated information searching and research
* 🧠 LLM-powered analysis and reasoning
* 🔄 Agent orchestration using LangGraph
* 📝 Structured research output
* 🌐 Web-based interactive interface using Streamlit
* ⚡ Modular architecture that can be extended with additional agents and tools

## Architecture

The system follows a multi-agent research pipeline:

```text
                    User Topic
                        │
                        ▼
              ┌──────────────────┐
              │   Streamlit UI   │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Research Pipeline│
              └────────┬─────────┘
                       │
              ┌────────▼─────────┐
              │   Search Agent   │
              │                  │
              │ Finds relevant   │
              │ information      │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Analysis Agent   │
              │                  │
              │ Processes and    │
              │ evaluates data   │
              └────────┬─────────┘
                       │
                       ▼
              ┌──────────────────┐
              │ Research Output  │
              │                  │
              │ Structured final │
              │ response         │
              └──────────────────┘
```

## Technologies Used

* **Python**
* **LangChain**
* **LangGraph**
* **OpenAI API**
* **Streamlit**
* **LLM-based Agents**
* **Web Search / Research Tools**

## Project Structure

```text
Multi agent research/
├── __pycache__/
├── .venv/
├── .env
├── app.py
├── pipeline.py
├── agents.py/
│   ├── search_agent.py
│   └── writer_agent.py
└── tools/
    └── web_search.py
├── requirements.txt

```

> `.env` should not be uploaded to GitHub because it may contain API keys.

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/multi-agent-research.git
cd multi-agent-research
```

### 2. Create a virtual environment

Windows:

```bash
python -m venv .venv
```

Activate it:

```bash
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

## Environment Variables

Create a `.env` file in the project directory:

```env
OPENAI_API_KEY=your_openai_api_key
```

Never commit your `.env` file to GitHub.

## Running the Application

Start the Streamlit application:

```bash
streamlit run app.py
```

If the project path contains spaces, use:

```bash
streamlit run "C:\Users\MUSKAAN\Projects\Multi agent research\app.py"
```

The application will open in your browser.

## How It Works

### 1. User Input

The user enters a research topic through the Streamlit interface.

Example:

```text
Impact of Generative AI on the Software Industry
```

### 2. Research Agent

The research agent receives the topic and searches for recent and relevant information.

Its objective is to identify:

* Relevant sources
* Recent developments
* Important facts
* Supporting information

### 3. Agent Processing

LangGraph manages the execution flow between the di
