# Naming Conventions

Consistent names make the repo easy to search and maintain.

## Pine Script Files

- **Format:** `vN.pine` or descriptive name (e.g. `fractal-template.pine`)
- **Strategy versions:** `v1.pine`, `v2.pine`, …
- **Templates:** `strategy-template.pine`, `indicator-template.pine`
- Lowercase, hyphens for multi-word names. No spaces.

## Strategy Folders

- **Format:** short, descriptive, lowercase, hyphens
- **Examples:** `sweep-scalper`, `momentum-breakout`, `range-fade`
- One folder per strategy; versioning is inside the folder via `v1.pine`, `v2.pine`.

## Backtest Folders

- **Path:** `backtests/YYYY/YYYY-MM/experiment-name/`
- **experiment-name:** short, lowercase, hyphens
- **Examples:** `sweep-scalper-bb-only`, `macd-filter-test`, `v2-daily-spy`
- No spaces; include strategy name or variant when it helps.

## Screenshot Files

- **Format:** descriptive-name.ext (e.g. `.png`, `.jpg`)
- **Examples:** `chart-daily.png`, `strategy-tester.png`, `drawdown.png`, `entry-zoom.png`
- Lowercase, hyphens. Optional date suffix if you have many: `chart-2026-03-09.png`.

## Markdown Research Notes

- **Strategy/indicator:** `notes.md` inside the strategy or indicator folder.
- **Backtest:** `notes.md` inside the backtest experiment folder.
- **Journal:** `trade-research-log.md` (single log file).
- Use `README.md` for a short “what this is” in each folder; use `notes.md` for hypothesis, params, and iteration details.

## Commit Messages

- **Format:** `scope: short imperative description`
- **Examples:**
  - `sweep-scalper: add MACD filter`
  - `backtests: 2026-03 sweep-scalper run`
  - `docs: update naming conventions`
- Scope = strategy name, `backtests`, `indicators`, `docs`, `journal`. Keep the description short and actionable.
