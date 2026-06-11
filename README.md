# Chat Assessment · In-Chat Psychological Scale Assessment for AI Conversations

English | [简体中文](./README.zh-CN.md)

A demo of administering standardized psychological scales naturally within an AI chat: triggered either by the user's explicit request or proactively recommended based on conversational signals. The full flow — trigger → consent → item-by-item administration → scoring → tiered report — happens inside the chat window.

**Live demo**: https://stavedl.github.io/chat-assessment/

## Features

- **Active trigger**: detects user intent ("I'd like to take an assessment") and starts after explicit consent
- **Passive trigger**: four signal types (keyword / semantic / emotional / behavioral) accumulate toward a threshold; a recommendation is made only after passing four decision gates (crisis bypass, timing, frequency control & cooldown, user preference). The side panel visualizes signals in real time
- **Crisis bypass**: expressions of self-harm risk block any assessment recommendation and switch to crisis-support responses
- **Conversational administration**: one item per message with option buttons, fuzzy text-answer mapping, go-back to previous item, minimum answer interval, exit anytime
- **Scoring & report**: factor-formula scoring, score-band interpretation, expert advice, disclaimer, and a straight-lining (identical answers) warning
- **Config-driven**: scales are plugged in via a standard JSON config — adding a new scale requires no code changes

## Demo Scale

Acceptance and Action Questionnaire–II (AAQ-II, code hs1051), single factor "Experiential Avoidance", 7 items on a 7-point scale, total score 7–49:

| Score | Level |
|---|---|
| 7–12 | Low |
| 13–28 | Moderate |
| 29–49 | High |

## Files

| File | Description |
|---|---|
| `index.html` | Interactive demo; single file, zero dependencies, opens directly in a browser |
| `aaq2_config.json` | Standard AAQ-II scale config (items, options, factor formula, interpretations, trigger rules); serves as a template for adding new scales |

## Run Locally

No setup required — download `index.html` and open it in any browser.

## Usage

Open the page, then click "Scenario 1" (active trigger) or "Scenario 2" (auto-plays a venting conversation so you can watch signals accumulate until a recommendation fires). You can also chat freely in the input box — messages containing trigger keywords accumulate signals.

## Contact

📮 lcl3@163.com

## Disclaimer

This is a product-design demo. Scale results are self-report screening references only and do not constitute a clinical diagnosis. If emotional distress persists or worsens, please seek professional psychological counseling or medical help.
