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

LangGraph manages the execution flow between the different agents.

Each agent can perform a specific task while the overall workflow maintains the state of the research process.

### 4. Analysis

The collected information is processed by the AI system to identify important findings and organize them into a meaningful structure.

### 5. Final Research Output

The system generates a structured research response that can contain:

Introduction
Key findings
Important developments
Analysis
Supporting information
Conclusion

```text
Example Workflow
Enter Topic
     │
     ▼
Research Agent
     │
     ▼
Collect Information
     │
     ▼
Analyze Information
     │
     ▼
Organize Findings
     │
     ▼
Generate Research Report
```

### Why Multi-Agent Architecture?

A multi-agent architecture divides a complex research task into smaller specialized tasks.

Instead of relying on a single AI agent to perform searching, analysis, and report generation simultaneously, different agents can be assigned specific responsibilities.

This improves:

* Modularity
* Maintainability
* Task specialization
* Workflow control
* Extensibility

Additional agents can be added later for tasks such as:

```text
Fact Checking
     │
Citation Verification
     │
Summarization
     │
Report Generation
     │
Quality Evaluation
```

### Future Improvements

* Add multiple independent research agents
* Add source credibility scoring
* Add automatic citation generation
* Add fact-checking agent
* Add PDF research report generation
* Add persistent research history
* Add vector database for knowledge storage
* Add RAG-based research
* Add support for multiple LLM providers
* Add research quality evaluation
* Add parallel agent execution
  
### Important Note

This project is intended for research assistance and experimentation. AI-generated information should be independently verified before being used for academic, professional, financial, legal, medical, or other high-impact purposes.

### Author

Muskan Pasricha

### AI / Machine Learning | Data Science | Generative AI

### License

This project is available for educational and research purposes.
