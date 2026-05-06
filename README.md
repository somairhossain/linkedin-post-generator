# AI-Powered LinkedIn Post Generator

An AI Agent built with LangChain and Groq (Llama 3) that generates
professional LinkedIn posts based on topic and language.

## Agent Workflow
1. User provides a **Topic** and **Language**
2. **Classifier Agent** labels the topic as `tech` or `general`
3. **Router** sends it to the correct writer agent
4. **Writer Agent** generates a 2–4 paragraph LinkedIn post in the chosen language

## Routing Logic
| Topic type | Agent used |
|---|---|
| Technology, AI, science | Tech Writer Agent |
| Business, lifestyle, culture | General Writer Agent |

## Demo Examples
- `"AI in Healthcare"` + English → Tech Writer Agent
- `"Remote Work Productivity"` + Bengali → General Writer Agent

## Demo Video
[Watch here](https://youtu.be/4iwwB2RnxjU)

## Setup

### Install dependencies
pip install langchain-groq langchain-core

### Set your API key
Get a free Groq key at https://console.groq.com

import os
os.environ["GROQ_API_KEY"] = "your-key-here"

### Run
Open `linkedin_post_generator.ipynb` in Google Colab and run all cells.

## Tech Stack
- [LangChain](https://python.langchain.com) — agent framework
- [Groq](https://groq.com) — free LLM API (Llama 3)
- Python 3.12
