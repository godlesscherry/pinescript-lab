# Pine Script Lab

A local research repository for **Pine Script** indicators and strategies used with **TradingView**. Code is written and versioned here; execution and backtesting happen in TradingView by pasting scripts into the Pine Editor.

## What This Repo Is For

- **Store** all Pine Script indicators and strategies in one place
- **Version** strategy changes cleanly with Git
- **Archive** backtest screenshots and notes by date and experiment
- **Document** research ideas, hypotheses, and iteration history
- **Iterate** without chaos: clear structure, naming, and workflow

You develop locally (VS Code / Cursor), paste into TradingView to run and backtest, then save results and commit. No TradingView API or automation—just organized research.

## How Pine Script Development Works Locally + TradingView

1. **Edit** `.pine` files in this repo (syntax highlighting, snippets, Git).
2. **Copy** the script (or the relevant version) into [TradingView Pine Editor](https://www.tradingview.com/pine-editor/).
3. **Run** and backtest on the chart; tweak inputs as needed.
4. **Capture** screenshots and notes in `backtests/YYYY/YYYY-MM/experiment-name/`.
5. **Commit** script changes and research artifacts to Git.

No sync tool required—copy/paste keeps the workflow simple and keeps TradingView as the single execution environment.

## Recommended Workflow

```
ideate → code locally → paste into TradingView → backtest → save screenshots/results → commit to git
```

1. **Ideate** — Note ideas in `journal/trade-research-log.md` or in a strategy’s `notes.md`.
2. **Code locally** — Create or edit `.pine` files under `strategies/` or `indicators/`.
3. **Paste into TradingView** — Open Pine Editor, paste, apply to chart.
4. **Backtest** — Run strategy/indicator, adjust inputs, note parameters in `notes.md`.
5. **Save results** — Screenshots in `backtests/YYYY/YYYY-MM/experiment-name/screenshots/`, summary in `notes.md`.
6. **Commit** — Meaningful commits: e.g. `sweep-scalper: add MACD filter, v1.1 logic`.

## Project Structure

```
pinescript-lab/
├── README.md                 # This file
├── .gitignore
├── docs/                     # Workflow, naming, experiment template
├── strategies/               # Trading strategies (Pine Script)
│   ├── sweep-scalper/        # Example: one strategy per folder
│   └── templates/            # strategy-template.pine, indicator-template.pine
├── indicators/              # Standalone indicators
│   └── fractal-tools/
├── backtests/               # Backtest runs by date
│   └── 2026/2026-03/...     # screenshots + notes per experiment
├── journal/                 # Research log and ongoing notes
├── snippets/                # VS Code/Cursor Pine snippets
└── .vscode/                 # Shared editor config
```

See each folder’s `README.md` for details.

## Adding a New Strategy

1. Create a folder under `strategies/`, e.g. `strategies/my-strategy/`.
2. Copy `strategies/templates/strategy-template.pine` to `strategies/my-strategy/v1.pine`.
3. Add a `README.md` (what the strategy does) and `notes.md` (hypothesis, params, iterations).
4. Implement logic, paste into TradingView, backtest, then save screenshots and notes under `backtests/`.
5. For a new iteration, add `v2.pine` (or `v1.1.pine`) and document the change in `notes.md` and commits.

See [docs/workflow.md](docs/workflow.md) and [docs/naming-conventions.md](docs/naming-conventions.md) for details.

## Logging Backtest Results

- **Where:** `backtests/YYYY/YYYY-MM/experiment-name/`
- **What:** `README.md` (one-line summary), `notes.md` (hypothesis, params, result summary, next steps), `screenshots/` (charts, performance, etc.).
- **Naming:** Use a short, descriptive experiment name (e.g. `sweep-scalper-bb-only`, `macd-filter-test`). See `docs/naming-conventions.md`.

## Best Practices for Versioning

- **One strategy per folder** — e.g. `sweep-scalper/` with `v1.pine`, `v2.pine`.
- **Version when logic or intent changes** — New file (v2) or clearly documented change in `notes.md`.
- **Record parameters** — In `notes.md` or in the backtest folder’s `notes.md` so you can reproduce runs.
- **Meaningful commits** — e.g. `sweep-scalper: add MACD filter`, `backtests: add 2026-03 sweep run`.
- **Keep templates lean** — Use `strategies/templates/` and `indicators/` templates; avoid copy-paste sprawl.

---

Start with [docs/workflow.md](docs/workflow.md) for the full workflow and [journal/trade-research-log.md](journal/trade-research-log.md) to log ideas.
