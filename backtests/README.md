# Backtests

Backtest runs and results: screenshots, notes, and short summaries. Organized by **year** and **month** so you can find runs quickly.

## Structure

```
backtests/
  2026/
    2026-03/
      experiment-name/
        README.md      # One-line summary
        notes.md       # Hypothesis, params, result summary, next steps
        screenshots/   # Charts, performance, etc.
```

- **YYYY/YYYY-MM** — When the backtest was run.
- **experiment-name** — Short, descriptive name (e.g. `sweep-scalper-bb-only`, `macd-filter-test`).

## Logging a Backtest

1. Create `backtests/YYYY/YYYY-MM/your-experiment-name/`.
2. Add `README.md` (one-line summary) and `notes.md` (use `docs/experiment-template.md` or backtest note template).
3. Save screenshots from TradingView into `screenshots/`.
4. Commit with a message like: `backtests: 2026-03 sweep-scalper MACD filter run`.

Screenshots in these folders are **tracked** by default so you have a full history. See root `.gitignore` if you need to exclude large batches.
