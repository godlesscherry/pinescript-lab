# Sweep Scalper — Notes

## Hypothesis

Scalp in direction of Supertrend after a “sweep” of a fractal pivot (liquidity grab). Bollinger Bands give context; optional MACD filter avoids weak momentum.

## Versions

| Version | Change |
|--------|--------|
| v1 | Initial: ST trend + BB + sweep placeholder + optional MACD filter. |

## Parameters (v1 defaults)

- **Supertrend:** length 10, mult 3.
- **Bollinger Bands:** length 20, mult 2.
- **MACD (filter):** 12, 26, 9.
- **Risk:** SL/TP in ticks (tune per symbol).

## Entry / Exit (v1)

- Long: Supertrend up + price above BB basis (or in lower band for mean reversion) + sweep placeholder true + (optional) MACD filter.
- Short: Supertrend down + symmetric short logic.
- Exits: SL/TP in ticks; optional trailing later.

## Observations

_Log here after backtests: what worked, what didn’t, regime dependence._

## Next iteration

_Add sweep logic, tune ST/BB, or add trailing exit._
