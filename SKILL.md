---
name: signalforge-ai
description: Analyze major Binance spot assets and produce an explainable trade-readiness verdict with deterministic risk controls. Use when the user asks whether BTC, ETH, BNB, SOL, or XRP is ready to trade, requests a market scan, or wants a risk-first setup review.
---

# SignalForge AI

Use Binance Agent OS public market-data capabilities to inspect the requested spot symbol. Default to `BTCUSDT` and `1h` only when the user gives neither.

## Workflow

1. Fetch the latest 24-hour ticker, recent klines, and best bid/ask for the symbol.
2. Reject stale, incomplete, or mismatched data. Never invent a missing value.
3. Evaluate trend (43%), liquidity (34%), and volatility safety (23%).
4. Return a score from 0–100 and exactly one verdict: `WATCH`, `WAIT`, or `NO TRADE`.
5. Explain the three strongest factors and state what would invalidate the verdict.

## Safety rules

- Operate read-only by default.
- Never claim guaranteed returns or present the score as financial advice.
- Never place, cancel, or modify an order from this skill.
- If the user asks to trade, show the proposed symbol, side, amount, order type, and risk first; require explicit human confirmation through the execution layer.
- Refuse analysis when required market data is stale or unavailable.

## Output format

Return: symbol, timeframe, data timestamp, score, verdict, evidence list, invalidation condition, and risk notice.
