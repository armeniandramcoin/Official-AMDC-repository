# AMDC — Armenian Dram Gold Coin

> Stable-style rebase token pegged to gold (XAU/USD) via Chainlink oracle.

- Network: BNB Chain (mainnet)  
- Contract: 0x74E4Bd21e8437c3ed2494bCE98CdeC7AFAA3da1B  
- Oracle (XAU/USD, 8 decimals): 0x86896fEB19D8A607c3b11f2aF50A0f239Bd71CD0  
- Automation: Chainlink Automation v2.1 (Custom Logic)

---

## 📌 Как это работает
- Каждое срабатывание ребейза сравнивает цену оракула с targetGoldPrice.
- Если цена выросла → минт в казну (treasury).
- Если цена упала → сжигание из казны, владелец получает процент burnFeeBps.
- Ограничение шага: maxStepBps.
- Минимальный интервал между ребейзами: minRebaseInterval.

---

## 🔧 Ключевые параметры (Owner)
- setMinRebaseInterval(uint256 s) — по умолчанию 300 сек (5 минут).
- setMaxStepBps(uint16 bps) — по умолчанию 2000 (20%), максимум 5000.
- setBurnFeeBps(uint16 bps) — максимум 2000 (20%).
- setTreasury(address t).

---

## 📊 События
- Rebased(uint256 oldSupply, uint256 newSupply, uint256 priceUsed, bool minted)
- TargetPriceSet(uint256 price)
- ParamsChanged(string key, uint256 value)
- AddressChanged(string key, address value)

---

## 📂 Структура репозитория
- contracts/ — смарт-контракты
- addresses/ — адреса в разных сетях
- automation/ — настройки Chainlink Automation
- docs/ — токеномика, whitepaper, oracle
- abi/ — ABI контрактов

---

## 🛠 Сборка и тест (Hardhat)
`bash
npm install
npx hardhat compile
