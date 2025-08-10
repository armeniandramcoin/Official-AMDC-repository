# AMDC — Armenian Dram Gold Coin

Idea. A token with a floating supply (rebase) based on the price of gold (XAU/USD). 
Goal: to maintain the price within the chain *through total supply* rather than through trading books.

## Mechanism
- Oracle: Chainlink XAU/USD (8 decimals).
- Each trigger:
  - If price > target → mint the difference to the treasury.
  - If price < target → burn from the treasury and pay the owner the burnFeeBps percentage.
  - Update targetGoldPrice = price.
- Step limit: maxStepBps (default 2000 = 20%).
- Minimum interval between rebases: minRebaseInterval (default 65 sec).

## Risks
- Oracle risk and rare large price gaps (limited by maxStepBps).
- Sufficient treasury balance is required to reduce supply.
- External markets/liquidity pools may provide a price different from the target price until the next rebase.

## Controllable parameters (owner)
- setMinRebaseInterval(uint256 s) — 60…86400 sec.
- setMaxStepBps(uint16 bps) — 1…5000 bps.
- setBurnFeeBps(uint16 bps) — maximum 2000 bps.
- setTreasury(address t).
