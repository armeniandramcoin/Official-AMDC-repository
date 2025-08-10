# AMDC — Armenian Dram Gold Coin

> Stable-style rebase token pegged to gold (XAU/USD) via Chainlink oracle.

- Network: BNB Chain (mainnet)
- Contract: 0x74E4Bd21e8437c3ed2494bCE98CdeC7AFAA3da1B  
- Oracle (XAU/USD, 8 decimals): 0x86896fEB19D8A607c3b11f2aF50A0f239Bd71CD0  
- Automation: Chainlink Automation v2.1 (Custom Logic)

---

## 📌 How it works
- Each rebase triggers a comparison of the oracle price with targetGoldPrice.
- If the price has risen → mint to the treasury.
- If the price has fallen → burn from the treasury, the owner receives a percentage of burnFeeBps.
- Step limit: maxStepBps.
- Minimum interval between rebases: minRebaseInterval.

---

## 🔧 Key parameters (Owner)
- setMinRebaseInterval(uint256 s) — default 300 sec (5 minutes).
- setMaxStepBps(uint16 bps) — default 2000 (20%), maximum 5000.
- setBurnFeeBps(uint16 bps) — maximum 2000 (20%).
- setTreasury(address t).

---

## 📊 Events
- Rebased(uint256 oldSupply, uint256 newSupply, uint256 priceUsed, bool minted)
- TargetPriceSet(uint256 price)
- ParamsChanged(string key, uint256 value)
- AddressChanged(string key, address value)

---

## 📂 Repository Structure
- contracts/ — smart contracts
- addresses/ — addresses on different networks
- automation/ — Chainlink Automation settings
- docs/ — tokenomics, whitepaper, oracle
- abi/ — contract ABIs

---

## 🛠 Build and test (Hardhat)
`bash
npm install
npx hardhat compile
## 📌 Official Links

🌐 Website: [https://amdcoin.fun](https://amdcoin.fun)  
✉️ Email: [info@amdcoin.fun](mailto:info@amdcoin.fun)  
💬 Telegram: [https://t.me/amdcoin_official](https://t.me/amdcoin_official)  

---

## 📜 Contract Information

Network: BNB Chain (Mainnet)  
Token Name: Armenian Dram Gold Coin (AMDC)  
Total Supply: 100,000,000,000 AMDC  
Contract Address: [0x74E4Bd21e8437c3ed2494bCE98CdeC7AFAA3da1B](https://bscscan.com/token/0x74E4Bd21e8437c3ed2494bCE98CdeC7AFAA3da1B)  
Oracle: XAU/USD (Chainlink) — [0x689696E119D8A067c3B1112Af50AA239B6d71CD0](https://bscscan.com/address/0x689696E119D8A067c3B1112Af50AA239B6d71CD0)  
Automation: Chainlink Automation v2.1 (Custom Logic)  

---

