# Indicators

Pine Script **indicator** scripts (overlays, panel studies). Each indicator can live in its own folder with `.pine` files and optional `notes.md`.

## Structure

- **One folder per indicator or family** — e.g. `fractal-tools/`, `volatility-band/`.
- **README.md** — What the indicator does and how to use it.
- **Optional notes.md** — Parameters, tweaks, and research notes.

## Adding a New Indicator

1. Create folder: `indicators/your-indicator-name/`.
2. Copy `strategies/templates/indicator-template.pine` into the folder (or use `fractal-tools/` as reference).
3. Implement logic, paste into TradingView, then commit.

Indicators are often reused inside strategies; keep them modular and well-commented.
