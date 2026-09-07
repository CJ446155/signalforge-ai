# SignalForge AI

![SignalForge AI cover](cover.png)

An explainable, read-only Trade Readiness Agent built for the Binance Agent OS Mini Hackathon (Track 1).

SignalForge scans normal high-liquidity Binance spot assets — BTC, ETH, BNB, SOL and XRP — then converts market evidence into one of three decisions: **WATCH**, **WAIT**, or **NO TRADE**. Every verdict includes its score, reasons and invalidation condition.

## Why it exists

Most market bots output a direction without showing why. SignalForge keeps the human in control: it reads market data, applies deterministic risk rules, explains the conclusion, and has no order permission.

## Agent OS integration

- `SKILL.md` is the Agent entry point and follows the Binance Skills Hub structure.
- Market data is designed to come from Binance Agent OS / Binance MCP public tools.
- The default permission boundary is read-only; execution requires a separate, confirmed layer.
- The web dashboard is a submission-ready visual demo of the Agent workflow.

## Live demo

https://signalforge-ai.a1046434848.chatgpt.site

## Run the demo

Serve `dist/` with any static server, for example:

```bash
npx serve dist
```

Open the displayed local URL, choose a symbol, timeframe and risk preference, then click **运行 Agent 分析**.

## Suggested demo flow

1. Show the five supported spot assets.
2. Select BNB and a 1-hour timeframe.
3. Run the Agent and point out the score, verdict and evidence.
4. Emphasize the read-only badge and human confirmation guardrail.

## Disclaimer

For research and demonstration only. This project does not provide investment advice and does not execute trades.

## License

MIT
