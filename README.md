# inequality-feed

A live wire on economic inequality worldwide: who owns what, who is priced out,
who writes the rules of the market, and who carries the loss when it breaks.

Built after the *Economic Inequality Within It* section on Welcome to Your
Galaxy, and scoped to the subjects raised there.

## What it does

`harvest_inequality.py` reads 178 wires every two hours — regulators and
central banks, the IMF, World Bank, OECD and BIS, research institutes, tax and
debt justice and corporate-accountability groups, and Google News across 26
languages — and writes `wire_inequality.json`. `index.html` renders it; the
Weebly embed carries the same document inside an iframe.

Standard library only. No dependencies, no API keys, no model calls.

## The fourteen subjects

It opens where the section opens, with self-sufficiency and the freedom to
leave, then covers the facets the section lists:

| | |
|---|---|
| Self-sufficiency and the freedom to leave | Wages, executive pay and job security |
| Wealth, inheritance and dynasty | Social mobility and opportunity |
| Purchasing power and basic necessities | Access to credit and capital |
| Regional and spatial inequality | Discrimination in the labour market |
| Access to public services | Taxation and who pays |
| Unequal access to lawmakers | |

The section calls the market the most powerful driver, and three subjects carry
that — kept only where the market bears on who ends up with what:

- **Who owns the market** — the section's point that a tiny group concentrates
  the wealth everyone else produces: shareholder concentration, blockholders,
  how little of it households hold, capital's share against labour's
- **The ladder pulled up** — a field made by experts for experts, priced in
  research, technology and time, plus the terminology that hides the door in
- **Private markets and who is allowed in** — accredited-investor thresholds,
  club deals, shrinking public listings, community lenders crowded out

Market machinery on its own is not the subject. Trading plumbing, enforcement
actions, systemic-risk warnings and tax mechanics — front running, dark pools,
insider dealing cases, derivatives clearing, stress tests, buybacks, carried
interest — are refused unless a story ties them to who ends up with what.

## The gate

Every subject term carries the words it must appear beside, so the daily ticker
cannot reach the wire. Shares rose, earnings beats, price targets, analyst
upgrades and stock tips are refused, along with sponsored content and trading
promotion.

## Weight

Each story is scored on what it carries: a decision (2), institutional material
(2), a measured figure (1), a pending decision with a date (1), a named
jurisdiction (1), a primary source (1). At three or more it is marked
consequential.

## Sources

`sources_inequality.json` has three blocks. `direct` is institutional and
research feeds; those carried over from the sibling repos are already proven
working, and any that does not answer is reported as unreachable rather than
hidden. `gnews` is Google News locale searches, whose URLs the harvester builds
from `hl`/`gl`/`ceid`. `events` is subject searches for recurring publications
and enforcement actions.

## Running it

    python3 harvest_inequality.py
    python3 harvest_inequality.py --dry-run
    python3 verify_sources.py
