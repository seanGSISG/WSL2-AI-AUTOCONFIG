# Your Agent Commands

**Goal:** Login to your coding agents and understand the shortcuts.

---

## The Three Agents

You have three powerful coding agents installed:

| Agent | Command | Alias | Company |
|-------|---------|-------|---------|
| Claude Code | `claude` | `ccd` | Anthropic |
| Codex CLI | `codex` | `cod` | OpenAI |
| Gemini CLI | `gemini` | `gmi` | Google |

---

## What The Aliases Do

The aliases are configured for **maximum power** (vibe mode):

### `ccd` (Claude Code)
```bash
NODE_OPTIONS="--max-old-space-size=32768" \
  ENABLE_BACKGROUND_TASKS=1 \
  claude --dangerously-skip-permissions
```
- Extra memory for large projects
- Background task support
- No permission prompts

### `cod` (Codex CLI)
```bash
codex --dangerously-bypass-approvals-and-sandbox
```
- Bypass safety prompts
- No approval/sandbox checks

### `gmi` (Gemini CLI)
```bash
gemini --yolo
```
- YOLO mode (no confirmations)

---

## First Login

Each agent needs to be authenticated once:

### Claude Code
```bash
claude auth login
```
Follow the browser link to authenticate with your Anthropic account.

### Codex CLI
```bash
codex login
```
Follow the browser prompts to authenticate with your **ChatGPT Pro/Plus/Team account**.

> **Note: OpenAI Has TWO Account Types:**
>
> | Account Type | For | Auth Method | How to Get |
> |--------------|-----|-------------|------------|
> | **ChatGPT** (Pro/Plus/Team) | Codex CLI, ChatGPT web | OAuth via `codex login` | [chat.openai.com](https://chat.openai.com) subscription |
> | **API** (pay-as-you-go) | OpenAI API, libraries | `OPENAI_API_KEY` env var | [platform.openai.com](https://platform.openai.com) billing |
>
> Codex CLI uses **ChatGPT OAuth**, not API keys. If you have an `OPENAI_API_KEY`, that's for the API—different system!
>
> **If login fails:** Check ChatGPT Settings → Security → "API/Device access"

### Gemini CLI
```bash
gemini
```
Follow the prompts to authenticate with your Google account.

---

## Test Your Agents

Try each one:

```bash
ccd "Hello! Please confirm you're working."
```

```bash
cod "Hello! Please confirm you're working."
```

```bash
gmi "Hello! Please confirm you're working."
```

---

## Quick Tips

1. **Start simple** - Let agents do small tasks first
2. **Be specific** - Clear instructions get better results
3. **Check the output** - Agents can make mistakes
4. **Use multiple agents** - Different agents have different strengths

---

## Practice This Now

Let's verify your agents are ready:

```bash
# Check which agents are installed
which claude codex gemini

# If you haven't logged in yet, start with Claude:
claude auth login
```

---

## Next

You're ready to start coding with AI agents! Try navigating to a project:

```bash
cd /data/projects/my_first_project
ccd "Help me create a simple hello world script"
```
