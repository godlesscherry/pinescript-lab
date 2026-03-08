# Sweep Scalper — Notes

## Hypothesis

Scalp in direction of Supertrend after a “sweep” of a fractal pivot (liquidity grab). Bollinger Bands give context; optional MACD filter avoids weak momentum.

## Versions

| Version | Change |
|--------|--------|
| v1 | ST trend + BB zone sweep (mid/outer) + fractal pivot sweep + optional MACD; pending setup → break of rejection candle; SL/TP %, time exit, optional trend-flip exit. |

## Parameters (v1 defaults)

- **Supertrend:** ATR length 10, factor 2.
- **Bollinger Bands:** length 20, mult 2; optional midline and outer band sweep.
- **Fractal:** strength 2; optional “require fractal sweep” for liquidity grab.
- **MACD (filter):** 12, 26, 9.
- **Risk:** SL 0.35%, TP 0.60%; max hold 4 bars; setup expires after 2 bars; optional exit on trend flip.

## Entry / Exit (v1)

- **Long:** Bull trend (ST) + zone sweep (ST line / BB mid / BB lower) + bullish rejection candle + (optional) fractal sweep low + (optional) MACD bullish. Pending → entry on break above rejection high.
- **Short:** Bear trend + zone sweep + bearish rejection + (optional) fractal sweep high + (optional) MACD bearish. Pending → entry on break below rejection low.
- **Exits:** SL/TP % from avg entry; time exit after max hold bars; optional close on Supertrend flip.

## Observations

_Log here after backtests: what worked, what didn’t, regime dependence._

## Next iteration

_Add sweep logic, tune ST/BB, or add trailing exit._
