# CrewAI Research Agent

A multi-agent research crew built with [crewAI](https://crewai.com). The runnable project is in [`research_agent/`](./research_agent/).

**For cloning this repo and running it**, follow [`research_agent/README.md`](./research_agent/README.md).

---

## Creating a new crew from scratch (optional)

Use these steps only if you are scaffolding a *new* project yourself (not when using this repo).

### 1. Install `uv`

```bash
pip install uv
```

### 2. Install the CrewAI CLI

```bash
uv tool install crewai==1.14.4
uv tool list
```

### 3. Create a crew

```bash
crewai create crew research_agent
cd research_agent
```

### 4. Run CLI (main.py via crewai)

```bash
cp .env.example .env   # then add OPENAI_API_KEY
crewai install
crewai run
```
### 5. Run Gradio UI (app.py)

```bash
cp .env.example .env   # then add OPENAI_API_KEY
uv run python app.py
```

## Example output

![Gradio UI showing a company research report for Microsoft Corporation](../images/output.png)

## Docs

- CrewAI: https://docs.crewai.com
- UV: https://docs.astral.sh/uv/
