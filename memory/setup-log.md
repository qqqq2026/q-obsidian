# OpenClaw Setup Log
> #config #openclaw #setup #integration
> Chronological log of all configuration changes and integrations.

---

## 2026-03-12

### Model Configuration
- Default model changed: `openai/gpt-5.4` → `anthropic/claude-sonnet-4-6`
- Fallback chain set: `gpt-5.2` → `claude-haiku-4-5` → `gpt-5-mini` → `gpt-4.1`
- Added alias: `gpt-mini` → `openai/gpt-5-mini`
- Gateway restarted cleanly

### Audio Transcription (inbound voice messages)
- Enabled: `tools.media.audio.enabled: true`
- Provider: OpenAI `gpt-4o-mini-transcribe`
- Cost: ~$0.003/min (~$0.0005 per 10s voice message)
- Status: ✅ tested and working (D. confirmed with test voice message)

### Edge TTS (text-to-speech)
- Installed: `node-edge-tts@1.2.10` globally via npm
- Provider: `edge` (Microsoft Edge Neural TTS — no API key required)
- Voice: `en-US-MichelleNeural`
- Auto-TTS: **OFF** — only use voice when D. explicitly asks
- Status: ✅ tested and working

### Web Search
- `web_fetch`: ✅ active, no key needed
- `web_search` (Brave): ⚠️ requires `BRAVE_API_KEY` — not yet configured
- Workaround: using `web_fetch` directly on URLs for research

### Q-Dashboard
- Location: `/data/.openclaw/workspace/revenue-lab/dashboard.html`
- Data: `/data/.openclaw/workspace/revenue-lab/tasks.json`
- HTTP server: python3 http.server on port 18790 (spun up on demand)
- Trigger: "show dashboard" or "show revenue lab" → Q renders via browser screenshot

### Memory Library
- Built: `/data/.openclaw/workspace/memory/LIBRARY.md`
- Structured into: preferences, model-config, setup-log, decisions, companies/, revenue-lab/
- Semantic search: via `memory_search` tool (OpenAI embeddings)

---

*Last updated: 2026-03-12*
