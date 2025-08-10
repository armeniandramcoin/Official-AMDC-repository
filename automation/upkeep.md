# Chainlink Automation (Upkeep)

- Registry (v2.1): 0xDc2E1e2799348F6721CaDFDd112Dafb3261f09AC
- Upkeep type: Custom logic
- Target contract: 0x74E4Bd21e8437c3ed2494bCE98CdeC7AFAA3da1B
- Gas limit: 500,000
- LINK funding: см. баланс в UI
- Trigger: ребейз выполняется, если:
  - прошло minRebaseInterval (по умолчанию 65 сек)
  - абсолютное отклонение цены от targetGoldPrice > 0
  - шаг не превышает maxStepBps

## Manual poke
- updateFromOracle() — берёт цену из оракула и ребейзит.
- performUpkeep(bytes) — ребейз с переданной ценой (используется Automation).
