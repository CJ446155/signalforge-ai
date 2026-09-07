# SignalForge AI — Track 1 Submission

## One-line pitch

SignalForge AI turns Binance spot-market evidence into an explainable trade-readiness verdict before a human decides whether to act.

## Problem

Traders often see a directional signal without knowing which evidence produced it or when it becomes invalid. That encourages impulsive decisions and makes an AI recommendation hard to audit.

## Solution

SignalForge reads market evidence for BTC, ETH, BNB, SOL and XRP, evaluates trend, liquidity and volatility safety, then returns one of three outcomes: WATCH, WAIT or NO TRADE. The result contains a 0–100 score, the strongest factors, an invalidation condition and a risk notice.

## Binance Agent OS usage

The repository-root `SKILL.md` is the Agent entry point. It instructs a compatible agent to retrieve public Binance market data through Binance Agent OS / MCP, validate freshness, apply deterministic weights and return a structured verdict. The skill is read-only and explicitly prohibits order execution.

## Links

- Live demo: https://signalforge-ai.a1046434848.chatgpt.site
- GitHub: add the public repository URL after publishing

## Track

Track 1 — Build an AI Agent with Binance Agent OS.
