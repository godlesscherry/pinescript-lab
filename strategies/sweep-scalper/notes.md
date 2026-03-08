# Sweep Scalper — Notes

## Hypothesis

Scalp in direction of Supertrend after a “sweep” of a fractal pivot (liquidity grab). Bollinger Bands give context; optional MACD filter avoids weak momentum.

## Versions

| Version | Change |
|--------|--------|
| v1 | ST trend + BB zone sweep (mid/outer) + fractal pivot sweep + optional MACD; pending setup → break of rejection candle; SL/TP %, time exit, optional trend-flip exit. |
| v2 | Theory-aligned: (1) Supertrend trend, (2) liquidity sweep of BB/ST/fractal (current or prior bar), (3) rejection candle with optional min body %, (4) MACD opposing-momentum filter (threshold), (5) entry on break of rejection high/low. Same exits as v1. |

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

## v2 parameters (defaults)

- **Trend:** Supertrend ATR 10, factor 2.
- **BB:** length 20, mult 2; midline and outer sweep toggles.
- **Fractals:** strength 2; optional require fractal pivot sweep.
- **MACD:** 12/26/9; “opposing threshold” — avoid long if hist < -threshold, short if hist > +threshold.
- **Setup:** Allow sweep on prior bar (rejection on current); optional min rejection body % of range.
- **Risk:** Same as v1 (SL/TP %, max hold bars, setup expiry, trend-flip exit).

## Next iteration

_Add sweep logic, tune ST/BB, or add trailing exit._
