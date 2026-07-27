# ResearchAgent Crew

A multi-agent research crew powered by [crewAI](https://crewai.com).

## Clone and run

### Prerequisites

- Python **>=3.10** and **<3.14**
- An OpenAI API key (and a Serper key if your tools use web search)

### 1. Clone the repo and open this project

```bash
git clone <your-repo-url>
cd <repo>/research_agent
```

If this folder is the repo root, just:

```bash
cd research_agent
```

### 2. Install `uv`

```bash
pip install uv
```

Or: https://docs.astral.sh/uv/getting-started/installation/

### 3. Install the CrewAI CLI

```bash
uv tool install crewai==1.14.4
uv tool list
```

### 4. Configure `.env`

Copy the example file and add your keys (`.env` is gitignored — never commit secrets):

```bash
cp .env.example .env
```

Edit `.env`:

```
OPENAI_API_KEY=sk-...
OPENAI_MODEL=gpt-4o-mini
SERPER_API_KEY=...
```

### 5. Install project dependencies

From this directory (`research_agent/`):

```bash
crewai install
```

This reads `pyproject.toml` (and `uv.lock` if present) and installs everything, including Gradio.

### 6. Run the crew

```bash
crewai run
```

---

## Customizing

- Agents: `src/research_agent/config/agents.yaml`
- Tasks: `src/research_agent/config/tasks.yaml`
- Logic / tools: `src/research_agent/crew.py`
- Entrypoint / inputs: `src/research_agent/main.py`

## Dependencies

Managed only via `pyproject.toml` + `uv` / `crewai install`. No `requirements.txt`.

## Support

- [CrewAI docs](https://docs.crewai.com)
- [CrewAI GitHub](https://github.com/joaomdmoura/crewai)
- [Discord](https://discord.com/invite/X4JWnZnxPb)
