# Strategies

Pine Script **strategy** scripts for TradingView. Each strategy lives in its own folder with versioned `.pine` files and `notes.md`.

## Structure

- **One folder per strategy** — e.g. `sweep-scalper/`, `momentum-breakout/`.
- **Versioned files** — `v1.pine`, `v2.pine` when logic or intent changes meaningfully.
- **Notes** — `README.md` (what it does), `notes.md` (hypothesis, parameters, iterations).

## Adding a New Strategy

1. Create folder: `strategies/your-strategy-name/`.
2. Copy `templates/strategy-template.pine` to `your-strategy-name/v1.pine`.
3. Add `README.md` and `notes.md` (see `docs/` for templates).
4. Implement, paste into TradingView, backtest, then record results under `backtests/`.

## Templates

- `templates/strategy-template.pine` — Strategy skeleton (inputs, plot, alerts, risk placeholders).
- `templates/indicator-template.pine` — Indicator skeleton (for overlay/panel indicators).

Use these as starting points to keep structure consistent.
