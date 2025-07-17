# Pydantic Agent

A powerful AI agent built with Pydantic AI that combines Agentic RAG (Retrieval Augmented Generation), long-term memory, web search, image analysis, and code execution capabilities. This agent can be configured to run with either cloud-based or local LLMs. The RAG pipeline implementation has also been created in a way where you can build in your own data source as another pipeline very easily.

## Agent Capabilities

- **Agentic RAG**: Query your documents with context-aware intelligence (local or Google Drive files)
- **Long-term Memory**: The agent remembers important information from previous conversations
- **Web Search**: Search the internet using Brave API or SearXNG
- **Image Analysis**: Analyze images with vision-capable LLMs
- **Code Execution**: Generate and run Python code safely
- **Multi-LLM Support**: Works with OpenAI, OpenRouter, or local Ollama models
- **Streamlit UI**: Simple chat interface for interacting with the agent (full frontend in a later module)

## Project Structure

```
4_Pydantic_AI_Agent/
├── .env.example               # Example environment variables
├── requirements.txt           # Project dependencies
├── agent.py                   # Main Pydantic AI agent implementation
├── clients.py                 # Client config for LLMs, databases, and long term memory
├── prompt.py                  # System prompt template
├── tools.py                   # Agent tool implementations
├── streamlit_ui.py            # Basic Streamlit user interface
├── RAG_Pipeline/              # RAG Pipeline components
│   ├── common/                # Common RAG functionality
│   │   ├── db_handler.py      # DB operations for RAG
│   │   ├── text_processor.py  # Functions to prep text for vector DB
│   ├── Google_Drive/          # Google Drive integration
│   │   ├── main.py            # Entrypoint for Google Drive RAG pipeline
│   │   ├── drive_watcher.py   # Logic for Google Drive file processing
│   ├── Local_Files/           # Local file processing
│   │   ├── main.py            # Entrypoint for local file RAG pipeline
│   │   ├── file_watcher.py    # Logic for local file processing
```
