# Chainlink Automation (Upkeep)

- Registry (v2.1): 0xDc2E1e2799348F6721CaDFDd112Dafb3261f09AC
- Upkeep type: Custom logic
- Target contract: 0x74E4Bd21e8437c3ed2494bCE98CdeC7AFAA3da1B
- Gas limit: 500,000
- LINK funding: see balance in UI
- Trigger: rebase is performed if:
  - minRebaseInterval has passed (default 65 sec)
  - absolute deviation of price from targetGoldPrice > 0
  - step does not exceed maxStepBps

## Manual poke
- updateFromOracle() — takes price from oracle and rebasizes.
- performUpkeep(bytes) — rebasizes with passed price (uses Automation).
