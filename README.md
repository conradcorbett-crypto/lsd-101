# LangSmith Deployments 101

## Overview

This repository is a hands-on lab that teaches you how to deploy LangGraph agents to LangSmith Deployments (LSD). You'll learn the complete workflow from building a containerized agent to deploying it on the LangSmith platform and interacting with it via API.

## What You'll Learn

- How to containerize a LangGraph agent using the LangGraph CLI
- Building and pushing Docker images to a container registry
- Deploying agents to LangSmith Deployments
- Interacting with deployed agents through API calls
- Best practices for agent deployment workflows

## Project Structure

```
lsd-101/
├── agents/                  # Agent implementation
│   ├── simple_text2sql.py  # Text-to-SQL agent
│   ├── prompts.py          # Agent prompts
│   └── utils.py            # Utility functions
├── notebooks/              # Interactive lab notebooks
│   └── lsd-101.ipynb      # Main lab notebook
├── part-1.md              # Setup and deployment instructions
├── requirements.txt       # Python dependencies
├── langgraph.json        # LangGraph configuration
└── .env.example          # Environment variables template
```

## Getting Started

### Prerequisites

- Docker Desktop installed and running
- Docker Hub account (or another container registry)
- LangSmith account with deployment access
- Python 3.11+ and [uv](https://github.com/astral-sh/uv) package manager
- OpenAI API key

### Running the Lab

1. **Follow the setup and deployment guide**: Start with [part-1.md](part-1.md) for detailed step-by-step instructions on:
   - Setting up your local environment
   - Building and pushing your Docker image
   - Deploying to LangSmith

2. **Work through the notebook**: Once your agent is deployed, open and run the Jupyter notebook:
   ```bash
   jupyter notebook notebooks/lsd-101.ipynb
   ```

   The notebook will guide you through interacting with your deployed agent.

## Agent Description

This lab uses a simple text-to-SQL agent that demonstrates the core concepts of LangSmith Deployments. The agent can convert natural language questions into SQL queries and execute them against a database.

## Troubleshooting

- **Docker build fails**: Ensure Docker Desktop is running and you have sufficient disk space
- **Push fails**: Verify you're logged in to Docker Hub with `docker login`
- **Deployment fails**: Check that your environment variables are correctly set and your LangSmith API key has deployment permissions

## Additional Resources

- [LangSmith Documentation](https://docs.smith.langchain.com)
- [LangGraph Documentation](https://langchain-ai.github.io/langgraph)
- [Docker Hub](https://hub.docker.com)

## WIP/Future Work

- Creating and running Assistants via sdk
- Advanced langgraph like memory, checkpointing, and time travel
