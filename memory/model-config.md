# Model Configuration
> #model #routing #fallback
> Permanent model-routing rules set by D. on 2026-03-12.

---

## Default Routing

| Use Case | Primary | Fallback |
|---|---|---|
| **Default / general** | Claude Sonnet 4.6 | ChatGPT 5.2 |
| **Coding tasks** | Claude Opus 4.6 | ChatGPT 5.1 Codex |
| **Planning / complex reasoning** | Claude Opus 4.6 | → delegate execution to cheaper sub-agent |
| **Routine / cheap tasks** | Claude Haiku 4.5 | ChatGPT 5 Mini → ChatGPT 4.1 |

## Notes
- Always state which model is being used when running a task
- ChatGPT 5 Mini alias: `gpt-mini` → `openai/gpt-5-mini` (configured 2026-03-12)
- Global fallback chain in OpenClaw config: `gpt-5.2` → `claude-haiku-4-5` → `gpt-5-mini` → `gpt-4.1`
- Default model set in openclaw.json: `anthropic/claude-sonnet-4-6`

## Configured Aliases (openclaw.json)
- `ChatGPT 5.4` → openai/gpt-5.4
- `ChatGPT 5.4 Pro` → openai/gpt-5.4-pro
- `ChatGPT 5.2` → openai/gpt-5.2
- `ChatGPT 5.1 Codex` → openai/gpt-5.1-codex
- `ChatGPT 4.1` → openai/gpt-4.1
- `Claude Opus 4.6` → anthropic/claude-opus-4-6
- `Claude Sonnet 4.6` → anthropic/claude-sonnet-4-6
- `Claude Haiku 4.5` → anthropic/claude-haiku-4-5
- `gpt-mini` → openai/gpt-5-mini

---

*Last updated: 2026-03-12*
