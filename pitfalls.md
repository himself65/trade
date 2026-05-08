# Trading Analysis Pitfalls

15 analytical biases to avoid when evaluating directional/options trades. Derived from real trade experience.

---

## 1. Do not treat "price at analyst consensus" as a bearish signal

**Rule**: Analyst consensus is a **trailing indicator**. Price leads analysts, not the reverse. When stock reaches consensus target, consensus is usually being revised higher.

**Why it matters**: Anchoring bearish because "price = consensus" ignores that the consensus itself has been rising. If last-month avg >> last-quarter avg, analysts are catching up to momentum, not capping it.

**How to apply**: Check the *velocity* of consensus revisions. Rising consensus with rising price = trend intact, not exhaustion.

---

## 2. A single large options trade ≠ "smart money" signal

**Rule**: One big institutional order reflects **one desk's positioning**, not market consensus. Institutions lose too.

**Why it matters**: A $800k+ LEAP call seller can be wrong. Using "they sold big at strike X" as a directional edge is flawed when the underlying fundamentals shift.

**How to apply**:
- Require *confluence* — multiple institutions same direction + price action same direction
- Aggressive sweeps > sitting orders
- Options flow is a **positioning snapshot**, not a **directional prediction**

---

## 3. Tape > opinion > DCF for short-term trades

**Rule**: For trades held <30 days, prioritize:
1. Price action (what the tape is doing)
2. Sentiment / catalysts (what's driving flow)
3. Valuation (DCF, multiples)

**Why it matters**: Starting with DCF and forcing the tape to fit leads to fighting trends. A stock can stay "overvalued" for months on momentum.

**How to apply**: Open every short-term analysis by describing the tape first (last 3 daily closes, volume profile, support/resistance), then layer sentiment, then valuation.

---

## 4. When thesis premise is invalidated, FLIP — don't hold

**Rule**: If the *precondition* for your thesis stops being true, exit or reverse. Holding through invalidation is sunk-cost bias.

**Why it matters**: Example — "sell-the-news" requires weak tape. If the stock holds strong through expected weakness, the setup is dead. Flipping early > stubborn holding.

**How to apply**:
- Write down the thesis *preconditions* at entry
- Review them each time new info arrives
- If a precondition breaks, trigger position review immediately
- Reversing a position is not weakness — it's the highest-order trading skill

---

## 5. Don't overreact to a single news event — check if it's priced in

**Rule**: Post-market news that moves stock <3% is often already 60-80% priced in. A small reaction doesn't mean the news is unimportant — it means the market already expected it.

**Why it matters**: Flipping strategies based on "big news" that the market barely responds to is overreaction. The magnitude of reaction tells you how much was unexpected.

**How to apply**: Estimate NPV of news → compare to actual price reaction → if reaction ≈ NPV, news is correctly priced. Recommend action only if reaction is materially off.

---

## 6. "Finding clever structures" signals fading conviction

**Rule**: When your instinct shifts from vanilla spreads to ratio spreads, butterflies, diagonals, ask: **Am I being clever because the simple structure is optimal, or because my conviction is dropping?**

**Why it matters**: Complex structures can mask uncertainty. Better to reduce size or close than dress up diminishing conviction in sophistication.

**How to apply**: When recommending a complex structure, explicitly check: "Is this really optimal, or am I hedging for a thesis I no longer fully believe?" If the latter, close instead of restructure.

---

## 7. IV crush benefits SHORT premium structures, not long ones

**Rule**: High IV Rank (>70) favors **selling** premium (credit spreads, short puts, iron condors). It hurts long premium (debit spreads, naked long options), even if direction is right.

**Why it matters**: A long put at IV 95% with IV crush to 50% can lose money even on a correct bearish call. Direction right + structure wrong = loss.

**How to apply**:
- High IV Rank + directional view → default to credit structures (sell premium)
- Only buy premium when IV is low OR directional conviction is very high
- Always ask: "Does my structure benefit from or suffer from IV crush?"

---

## 8. "Priced in" is not binary — estimate the percentage

**Rule**: Events are partially priced in. Use "what % is priced in" framing rather than "is it priced in yes/no".

**Why it matters**: 70% priced in is very different from 100% priced in. The 30% residual uncertainty still drives multi-day price action.

**How to apply**: For any news event:
- Estimate theoretical NPV of the news
- Compare to actual price reaction
- If reaction ≈ NPV × X%, then (100 - X)% is still unpriced
- Size positions to the residual uncertainty, not the nominal news

---

## 9. Preconditions met ≠ stock direction

**Rule**: Hitting all your fundamental preconditions does NOT guarantee positive stock reaction. Sentiment, forward guidance, and sector mood are independent variables that can override fundamentals in the short term.

**Why it matters**: A name can print every metric above the threshold you set in advance and still fall on the print. "Thesis correct" and "stock will go up" are different claims. The market trades on a blend of fundamentals + forward expectations + cohort mood, not fundamentals alone.

**How to apply**:
- Track **two** precondition sets: fundamental AND sentiment.
- Add forward guidance preconditions, not just current-quarter ones (e.g., "next-quarter segment growth must be guided ≥ X%").
- Add sector mood preconditions (e.g., "cohort bellwether not down ≥ N% on earnings day").
- When buy-side previews are widely circulated, treat them as the new consensus and raise thresholds 10-20% above their stated levels.

---

## 10. T+1 reverse drift — AH price doesn't predict next-day open

**Rule**: Initial AH reaction (16:00-20:00 earnings night) often reverses by next-day open. Sell-side notes drop overnight, rating actions hit pre-market, and T+1 sentiment can flip the AH read entirely.

**Why it matters**: A stock that recovers from a sharp AH dip to nearly flat by 21:00 EST can still gap down the next morning and drift further intraday. Extrapolating "AH stabilization" forward leads to over-confident hold decisions overnight.

**How to apply**:
- Don't anchor decisions on 16:00-17:00 AH (still active price discovery).
- 18:00-20:00 AH is more informative but still only ~50% of the eventual T+1 reaction.
- Plan for a **2-day window**: T+0 AH + T+1 open. T+1 morning is the "real" price discovery moment.
- Sell-side downgrades typically post 6-9 PM EST and hit pre-market.
- Default exit/reload decisions to T+1 morning unless a position is already at structural max profit (in which case lock at T+0 AH).

---

## 11. LEAPS through earnings = unhedged vega tax

**Rule**: Long-dated long options carry meaningful vega. Earnings IV crush represents a guaranteed loss component independent of direction. Holding a LEAPS through earnings without hedging is implicitly a short-vol bet.

**Why it matters**: A LEAPS with vega ~1.4/share loses ~$140 per 1pp of IV crush per contract. Earnings IV crush of 4-6pp on LEAPS = ~$500-800 of guaranteed bleed per contract regardless of stock direction. The stock has to rally meaningfully just to break even on the IV component before any direction P&L kicks in.

**How to apply**:
- **Calculate vega tax explicitly** before earnings: `vega × 100 × estimated IV crush in pp`.
- Choose one explicit response:
  1. Buy short-dated put as vega-tax insurance (cheap relative to vega bleed if direction goes wrong).
  2. Convert LEAPS to diagonal (sell front-week call against LEAPS) — short call IV crush partially offsets.
  3. Close LEAPS pre-earnings, re-enter post-IV-crush at lower IV.
  4. Accept the bleed and reduce sizing.
- Never hold LEAPS through earnings without consciously choosing one of these.
- Sector mood + capex panic can compound vega tax with delta loss → catastrophic LEAPS days exist.

---

## 12. Recognize "manipulator-tape" names — sell premium, don't buy direction

**Rule**: Some high-IV names trade with heavy market-maker / large-trader pump-dump patterns. Frequent ±3% intraday swings without news, $10–20 AH wicks on thin liquidity, and programmatic algo selling on specific keywords. **For these names, premium-selling and oscillation-scalping outperform directional buying.**

**Why it matters**: A correct directional thesis can still lose money in a manipulator tape because the price oscillates faster than your conviction window. Buying calls in these names is paying for vol that will be harvested by the next pump-dump cycle.

**How to apply**:
- Tickers that fit the pattern (initial list, expand over time): APP, MSTR, COIN, PLTR, DJT, TSLA (occasional)
- Default structure: Jade Lizard / Iron Condor / Bull Put Spread (sell premium)
- Pair with: scalp leveraged proxy (APPX for APP, MSTU for MSTR, etc.) on the oscillation
- **Avoid**: Long-dated call buying — vol will be harvested out from under you

---

## 13. Take-profit discipline beats target-price obsession (in volatile tapes)

**Rule**: In manipulator/high-vol names, **book 60–70% of expected move** rather than waiting for full target. The marginal last 30% of expected move is rarely worth the hold-time risk.

**Why it matters**: APP case (May 2026): I quoted $510 6M target. User exited APPX at $490 — left ~$20 on the table but avoided 3+ days of pump-dump risk. Each subsequent round-trip earned more than the marginal $20 would have.

**How to apply**:
- For trades held days-to-weeks: book at 60–70% of expected move
- For credit spreads / Jade Lizards: close short legs at +50% of max credit (mechanical Tasty rule)
- For long premium: scale out — 1/3 at +50%, 1/3 at +100%, 1/3 trail with stop
- Never wait for theoretical max profit on event-driven structures

---

## 14. Single channel-check is a sample, not a population

**Rule**: One agency / one customer / one expert call is **n=1**. Aggressive growth signals from a single source are usually self-selection — agencies willing to take channel-check calls tend to be the ones with the most aggressive spending.

**Why it matters**: APP case — agency reported +19% QoQ Q4→Q1 spending; I extrapolated to APP-wide trend. Reality was +11% QoQ. The agency was a top-quartile spender, not a market average.

**How to apply**:
- Discount any single channel-check by 30–40% before using it as a base case
- Require **2–3 independent sources** before lifting the base case
- Look for confirming sources from *different demand profiles* (large advertiser + small advertiser + agency, not 3 agencies)
- Never let a single call swing your beat estimate by more than 1pp

---

## 15. AH order-book lopsidedness is a fade signal at extremes

**Rule**: When AH bid/ask size ratio exceeds 5:1 in either direction at a price extreme (within 1% of AH high or low), the move is being driven by thin liquidity and is highly likely to revert.

**Why it matters**: APP case — AH peak $483.5 had ask size 310 vs bid size 30 (10:1). Reverted to $476 within 40 minutes. Selling Call Spread or shorting leveraged proxy at the lopsided extreme captures this reversion.

**How to apply**:
- Check bid/ask size ratio at AH extremes
- 5:1 ask-heavy at AH high → fade with short call spread or leveraged-proxy short
- 5:1 bid-heavy at AH low → fade with bull put spread or leveraged-proxy long
- Best between 18:00–20:00 ET (book is real but retail asleep — good signal-to-noise)
- **Not a position trade** — book within 30–60 minutes
