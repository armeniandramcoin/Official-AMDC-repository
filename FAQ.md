# AMDC — Часто задаваемые вопросы

## 1. Что такое AMDC?
AMDC (Armenian Dram Gold Coin) — алгоритмический стейблкоин, привязанный к цене золота (XAU/USD) через Chainlink oracle.

## 2. На какой сети работает AMDC?
- Сеть: BNB Chain Mainnet
- Адрес контракта: 0x74E4Bd21e8437c3ed2494bCE98CdeC7AFAA3da1B
- Оракул: XAU/USD (6 decimals) 0x6899f6E19D8A067c3b01112F5A00A2398d71CD0D

## 3. Как работает ребейс?
Ребейс — это автоматическая корректировка количества токенов в обращении, чтобы цена оставалась вблизи целевой (цена золота).
- Интервал между ребейсами: 65 секунд
- Максимальный шаг изменения: ±20% (2000 BPS)

## 4. Как финансируется upkeep?
Через Chainlink Automation v2.1, баланс пополняется в токенах LINK.
- Апкип-адрес: 0x74E4Bd21e8437c3ed2494bCE98CdeC7AFAA3da1B
- Баланс и лог можно посмотреть на [Automation UI](https://automation.chain.link/bsc)

## 5. Где найти больше информации?
- Сайт: [https://amdcoin.fun](https://amdcoin.fun)
- Telegram: [@amdcoin_official](https://t.me/amdcoin_official)
- Email: info@amdcoin.fun
