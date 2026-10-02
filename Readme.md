# 🔬 Multi-Agent Research System

An AI-powered research assistant that uses multiple specialized agents to research a topic, gather relevant information, generate a structured report, and evaluate the final output.

## 📌 Overview

The **Multi-Agent Research System** is designed to automate the research process using Large Language Models (LLMs) and agent-based workflows.

Instead of relying on a single LLM prompt, the system separates research into multiple stages, allowing specialized agents to handle information retrieval, content analysis, report generation, and quality evaluation.

The goal is to produce structured, informative research reports while reducing the manual effort required to search, organize, and synthesize information.

## ✨ Features

* 🤖 **Multi-Agent Architecture:** Divides the research workflow into specialized tasks.
* 🔍 **Automated Research:** Retrieves relevant information using web-search tools.
* 📄 **Content Extraction:** Processes source material to gather useful information.
* ✍️ **AI Report Generation:** Converts collected information into a structured research report.
* 🧐 **Quality Evaluation:** Reviews generated reports and identifies potential improvements.
* 🔗 **Tool Integration:** Connects language models with external information sources.
* ⚡ **Automated Workflow:** Coordinates the research process from input to final output.

## 🏗️ System Architecture

The research workflow follows a sequence of specialized stages:

```text
          ┌──────────────────────┐
          │   User Research Query │
          └──────────┬───────────┘
                     │
                     ▼
          ┌──────────────────────┐
          │    Research Agent    │
          │ Search & Information │
          │      Retrieval       │
          └──────────┬───────────┘
                     │
                     ▼
          ┌──────────────────────┐
          │    Reader Agent      │
          │ Extract & Analyze    │
          │    Source Content    │
          └──────────┬───────────┘
                     │
                     ▼
          ┌──────────────────────┐
          │     Writer Agent     │
          │ Synthesize Findings  │
          │  into a Report       │
          └──────────┬───────────┘
                     │
                     ▼
          ┌──────────────────────┐
          │     Critic Agent     │
          │ Review & Evaluate    │
          │    the Report        │
          └──────────┬───────────┘
                     │
                     ▼
          ┌──────────────────────┐
          │   Final Research     │
          │        Report        │
          └──────────────────────┘
```

## ⚙️ How It Works

1. **Research:** The system accepts a research topic and retrieves relevant information from available sources.
2. **Content Analysis:** Retrieved information is processed to extract useful facts and context.
3. **Report Generation:** The collected findings are synthesized into a coherent, structured report.
4. **Quality Review:** A separate evaluation stage reviews the generated report and identifies possible gaps or improvements.
5. **Final Output:** The research report is presented to the user.

## 🛠️ Technology Stack

| Technology               | Purpose                                    |
| ------------------------ | ------------------------------------------ |
| Python                   | Core application logic                     |
| LangChain                | LLM orchestration and agent workflows      |
| Large Language Models    | Reasoning, analysis, and report generation |
| Web Search API           | Retrieving relevant online information     |
| BeautifulSoup / Requests | Web-page content extraction, if used       |
| Streamlit                | Interactive user interface, if used        |
| python-dotenv            | Environment variable management            |

*The table lists the expected stack; retain only the technologies actually used in the project.*

## 📂 Project Structure

```text
Multi-Agent-Research-System/
│
├── agents.py           # Agent and LLM chain definitions
├── tools.py            # Search and information retrieval tools
├── pipeline.py         # Research workflow orchestration
├── app.py              # User interface, if applicable
├── requirements.txt    # Python dependencies
├── .env                # API keys (not committed to Git)
├── .gitignore
└── README.md
```

## 🚀 Getting Started

### Prerequisites

* Python 3.10 or later
* An API key for your chosen LLM provider
* An API key for your web-search provider, if required
* Git

### 1. Clone the Repository

```bash
git clone https://github.com/divyanshu8903/Multi-Agent-Research-System.git

cd Multi-Agent-Research-System
```

### 2. Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

On macOS or Linux:

```bash
source .venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure Environment Variables

Create a `.env` file in the project root and add the API keys required by your implementation.

For example, if using OpenAI and Tavily:

```env
OPENAI_API_KEY=your_openai_api_key
TAVILY_API_KEY=your_tavily_api_key
```

Replace the placeholders with your own API keys. Never commit your `.env` file or expose API keys in your source code.

## ▶️ Running the Project

Run the command corresponding to your implementation.

**Option 1: Web interface**

If the project includes a Streamlit interface:

```bash
streamlit run app.py
```

**Option 2: Command-line workflow**

If `pipeline.py` is the main entry point:

```bash
python pipeline.py
```

## 💡 Example Use Cases

The system can be adapted for research tasks such as:

* Exploring emerging technologies and AI developments.
* Researching industry trends and market developments.
* Comparing technical approaches and methodologies.
* Collecting information for academic projects.
* Preparing structured background research on a topic.

## 🔮 Future Improvements

* Parallel execution of independent research agents.
* Source citations and reference validation.
* Iterative research with feedback-driven refinement.
* Improved error handling and retry mechanisms.
* Research history and persistent memory.
* Evaluation against a single-agent baseline.
* Support for exporting reports to PDF and other formats.
* Cost, latency, and token-usage tracking.

## ⚠️ Limitations

* Generated reports may contain factual errors or incomplete information.
* The quality of the output depends on the underlying LLM and retrieved sources.
* External API availability, rate limits, and usage costs may affect execution.
* Important claims should be verified against the original sources.

## 🔐 Security

* Store API keys in environment variables.
* Keep `.env` excluded from version control.
* Avoid sharing credentials or other sensitive information in logs.

## 👨‍💻 Author

**Divyanshu**

* GitHub: [@divyanshu8903](https://github.com/divyanshu8903)

