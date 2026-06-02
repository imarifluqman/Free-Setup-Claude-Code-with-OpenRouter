# Free Setup Claude Code with OpenRouter on WSL Ubuntu

> **Qwen CLI is gone. Gemini CLI support ends on June 16.**
>
> If you're looking for a free and reliable alternative to continue coding with AI in your terminal, this repository provides a simple way to use **Claude Code with OpenRouter** on **WSL Ubuntu**.

---

## 📖 About This Repository

This repository is dedicated to helping developers set up **Claude Code** for free using **OpenRouter** on **Ubuntu running inside Windows Subsystem for Linux (WSL)**.

The goal is to provide a straightforward, beginner-friendly setup that allows you to continue using AI-powered coding tools without depending on services that are being discontinued.

---

## ❓ Why This Matters

Many developers relied on tools such as:

- Qwen CLI
- Gemini CLI

However:

- ❌ **Qwen CLI is no longer available**
- ❌ **Gemini CLI support is ending on June 16**

As these tools disappear, developers need a stable alternative that:

- Works in the terminal
- Supports powerful AI models
- Has a free usage option
- Runs smoothly on WSL Ubuntu

**Claude Code + OpenRouter** provides that solution.

---

## 🚀 Why Claude Code + OpenRouter?

### 💸 Free to Use
No monthly subscription required. Simply create an OpenRouter account and use available free models.

### 🤖 Access to Multiple Models
OpenRouter provides access to many AI models, including:

- Claude Haiku
- Claude Sonnet
- Claude Opus
- Gemini
- Llama
- DeepSeek
- And many more

### 💻 Native CLI Experience
Continue using familiar Claude Code commands directly from your terminal.

### 🐧 WSL Friendly
Works seamlessly inside Ubuntu on Windows Subsystem for Linux.

---

## 📋 Prerequisites

Before starting, make sure you have:

- WSL Ubuntu installed
- Node.js and npm installed
- An OpenRouter account
- An OpenRouter API key
- Basic Linux command-line knowledge

### OpenRouter

Create an account and generate an API key:

👉 https://openrouter.ai

---

# 🛠️ Step-by-Step Setup Guide

## 1. Install Claude Code

Using npm:

```bash
npm install -g @anthropic-ai/claude-code
```

Or using the official installer:

```bash
curl -s https://claude.ai/cli.sh | sh
```

---

## 2. Create the Claude Configuration Directory

```bash
mkdir -p ~/.claude
```

This directory stores Claude Code configuration files.

---

## 3. Configure OpenRouter

Create or edit:

```bash
~/.claude/settings.json
```

Add the following configuration:

```json
{
  "env": {
    "ANTHROPIC_BASE_URL": "https://openrouter.ai/api",
    "ANTHROPIC_AUTH_TOKEN": "sk-or-your-key-here",
    "ANTHROPIC_API_KEY": "",
    "ANTHROPIC_MODEL": "openrouter/free"
  },
  "model": "sonnet[1m]"
}
```

---

## ⚠️ Important Configuration Rules

### Base URL

✅ Correct:

```text
https://openrouter.ai/api
```

❌ Incorrect:

```text
https://openrouter.ai/api/v1
```

Do **not** add `/v1`.

---

### Authentication

✅ Use:

```text
ANTHROPIC_AUTH_TOKEN
```

❌ Do not use:

```text
ANTHROPIC_API_KEY
```

Your OpenRouter key must be placed in:

```json
"ANTHROPIC_AUTH_TOKEN"
```

---

### Environment Variables

Do **not** modify:

- `~/.bashrc`
- `~/.zshrc`
- Shell profile files

Keep all configuration inside:

```text
~/.claude/settings.json
```

---

## 4. Verify Installation

Run:

```bash
claude --version
```

If a version number appears without errors, the installation is successful.

---

## 5. Launch Claude Code

Close the current terminal and open a fresh terminal session.

Then run:

```bash
claude
```

You should enter the Claude Code interactive interface.

---

# 🔄 Switching Models

You can specify a model directly from the command line.

Example:

```bash
claude --model meta-llama/llama-3.2-3b-instruct:free
```

---

## Popular Free Models on OpenRouter

### Claude Models

```text
anthropic/claude-3-5-haiku-20241022
anthropic/claude-3-5-sonnet-20241022
```

### Meta Models

```text
meta-llama/llama-3.2-3b-instruct:free
```

### Google Models

```text
google/gemini-2.0-flash-exp:free
```

### DeepSeek Models

```text
deepseek/deepseek-chat
```

Browse all available free models:

👉 https://openrouter.ai/models?free=true

---

# 🐞 Common Errors & Fixes

| Error | Cause | Solution |
|---------|---------|---------|
| `ANTHROPIC_API_KEY error` | Wrong environment variable | Use `ANTHROPIC_AUTH_TOKEN` |
| `Could not resolve host` | Incorrect base URL | Use `https://openrouter.ai/api` |
| `401 Authentication Failed` | Invalid API key | Verify OpenRouter API key |
| `Command not found` | Claude not in PATH | Restart terminal |
| `429 Rate Limited` | Free model limits reached | Switch to another free model |
| Empty responses | Model issue or limits | Try a different model |

---

# 🙌 Credits

The setup approach is inspired by community-driven documentation and open-source discussions around integrating **Claude Code** with **OpenRouter**.

Special thanks to the developers and contributors who shared their findings with the community.

---

# 👨‍💻 Author

**Muhammad Arif**

- GitHub: https://github.com/imarifluqman
- Portfolio: https://arifluqman.vercel.app

---

# 📢 Coming Soon

This repository will soon include:

- Complete beginner-friendly setup guide
- Screenshots for every step
- Troubleshooting section
- OpenRouter model comparison
- Claude Code productivity tips
- WSL optimization guide
- Advanced configuration examples
- Video tutorial links

Stay tuned for updates.

---

⭐ If this repository helps you, consider starring it and sharing it with other developers.
