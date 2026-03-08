# Sweep Scalper

Sweep-based scalping strategy using Supertrend for trend bias, Bollinger Bands for context, and optional fractal pivot “sweep” and MACD filter. Kept simple for local iteration and backtesting in TradingView.

## Concept

- **Trend:** Supertrend defines bias (long/short or flat).
- **Context:** Bollinger Bands for volatility and mean reversion.
- **Sweep:** Placeholder for fractal pivot sweep (liquidity grab) detection.
- **Filter:** Optional MACD filter to avoid low-momentum entries.

## Files

- `v1.pine` — Current strategy script (paste into Pine Editor).
- `notes.md` — Hypothesis, parameters, and version history.

## Usage

1. Open `v1.pine`, copy full contents.
2. Paste into TradingView Pine Editor, apply as Strategy.
3. Backtest on your symbol/timeframe; tune inputs.
4. Save screenshots and summary in `backtests/YYYY/YYYY-MM/experiment-name/`.
