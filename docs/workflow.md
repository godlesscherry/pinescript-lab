# Workflow

How to create, version, and document strategies and backtests in this repo.

## Creating a New Strategy Version

1. **First version** — Create `strategies/your-strategy/v1.pine` from `strategies/templates/strategy-template.pine`. Add `README.md` and `notes.md`.
2. **Iteration** — Either:
   - **Edit v1.pine** for small tweaks (e.g. input defaults), and document in `notes.md` and commit message, or
   - **Create v2.pine** when you change logic, entry/exit rules, or risk structure so you keep a clear history.

## When to Create v2, v3, etc.

- **New file (v2, v3)** when:
  - Entry or exit logic changes in a meaningful way
  - You add/remove a filter (e.g. MACD, Supertrend)
  - Risk or position sizing logic changes
  - You want a reproducible snapshot before a big experiment
- **Stay on same file** when:
  - Only input defaults or cosmetic plot changes
  - Minor parameter tuning you’ve already recorded in `notes.md`

Document every version in the strategy’s `notes.md` (what changed and why).

## Recording Parameter Changes

- **In strategy folder:** `strategies/your-strategy/notes.md` — list versions (v1, v2) with main parameters and logic summary.
- **In backtest folder:** `backtests/YYYY/YYYY-MM/experiment-name/notes.md` — exact inputs used for that run (length, mult, etc.) so you can reproduce.

Always note symbol and timeframe in backtest notes.

## Saving Screenshots from TradingView

1. Run your strategy/indicator on the chart.
2. Take a screenshot (TradingView snapshot, or OS screenshot) of the chart and/or Strategy Tester panel.
3. Save into `backtests/YYYY/YYYY-MM/experiment-name/screenshots/`.
4. Use clear names: e.g. `chart-daily.png`, `strategy-tester.png`, `drawdown.png`. See [naming-conventions.md](naming-conventions.md).

Screenshots in `backtests/` are tracked in Git by default.

## Naming Backtest Folders

- **Format:** `backtests/YYYY/YYYY-MM/short-experiment-name/`
- **Examples:** `sweep-scalper-bb-only`, `macd-filter-test`, `v2-daily-spy`
- Keep names short, lowercase, hyphenated. No spaces. See [naming-conventions.md](naming-conventions.md).

## Writing Useful Commit Messages

- **Strategy/indicator:** `sweep-scalper: add MACD filter`, `fractal-tools: fix pivot lookback`
- **Backtests:** `backtests: 2026-03 sweep-scalper MACD run`, `backtests: add v2 daily SPY screenshots`
- **Docs/journal:** `docs: update workflow`, `journal: log BB width idea`

Start with the area (strategy name, backtests, docs), then a short, imperative description.
