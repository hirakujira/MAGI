# MAGI System

A fan-made web application inspired by the MAGI supercomputer from _Neon Genesis Evangelion_. Enter a yes/no question and watch three AI units deliberate simultaneously, then reach a verdict by majority vote.

**[繁體中文](README.zh.md) | [日本語](README.ja.md)**

![Demo](demo.gif)

---

## The Three Units

| Unit          | AI Model         | Perspective                             |
| ------------- | ---------------- | --------------------------------------- |
| MELCHIOR • 1  | OpenAI GPT         | Scientist — logic and rational analysis |
| BALTHASAR • 2 | Anthropic Claude | Mother — protection and care-oriented   |
| CASPER • 3    | Google Gemini    | Woman — intuition and emotional insight |

## Verdicts

| Result               | Meaning                      |
| -------------------- | ---------------------------- |
| **承認（APPROVE）**  | Majority voted yes           |
| **否決（REJECT）**   | Majority voted no            |
| **棄権（ABSTAIN）**  | At least two units abstained |
| **膠着（DEADLOCK）** | No majority reached          |

> **Critical Matter**: If two or more units assess the topic as irreversible and potentially catastrophic (e.g. self-destruction, killing), the system automatically switches to a unanimous rule — all three units must approve for the action to proceed; any dissent or abstention results in rejection. Click any unit to see whether it flagged the topic as critical.

## Getting Started

### Prerequisites

You will need API keys for the following services:

- [OpenAI](https://platform.openai.com/api-keys) — for MELCHIOR-1
- [Anthropic](https://console.anthropic.com/settings/keys) — for BALTHASAR-2
- [Google AI Studio](https://aistudio.google.com/apikey) — for CASPER-3

### Local Development

```bash
# 1. Clone the repository
git clone https://github.com/hirakujira/MAGI.git
cd MAGI

# 2. Set up environment variables
cp .env.local.example .env.local
# Edit .env.local and fill in your API keys

# 3. Install dependencies
npm install

# 4. Start the development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000).

### Docker

```bash
# Copy and configure your environment variables first
cp .env.local.example .env.local

docker compose up
```

## Environment Variables

| Variable            | Description                     | Default            |
| ------------------- | ------------------------------- | ------------------ |
| `OPENAI_API_KEY`    | OpenAI API key (MELCHIOR-1)     | —                  |
| `OPENAI_MODEL`      | GPT model name                 | `gpt-5.6-luna`      |
| `OPENAI_REASONING_EFFORT` | GPT reasoning effort (`low`, `medium`, or `high`) | `low` |
| `ANTHROPIC_API_KEY` | Anthropic API key (BALTHASAR-2) | —                  |
| `ANTHROPIC_MODEL`   | Anthropic model name            | `claude-haiku-4-5` |
| `GOOGLE_API_KEY`    | Google AI API key (CASPER-3)    | —                  |
| `GOOGLE_MODEL`      | Google model name               | `gemini-3.5-flash-lite` |

## How to Use

1. Type a yes/no question in the input field and press **Enter**
2. All three units begin deliberating simultaneously and independently
3. Each unit stops flickering and shows its result as soon as it finishes
4. The final verdict is determined by majority vote once all three complete
5. Click any unit to read its detailed reasoning

## Copyright Notice

This project is a fan work created as a tribute to _Neon Genesis Evangelion_ by Hideaki Anno / GAINAX / khara. All Evangelion-related names and concepts are the property of their respective copyright holders.

## Acknowledgements

### Sponsors

Special thanks to the following for sponsoring API token costs:

- 天上天下唯我翻車大皮粉
