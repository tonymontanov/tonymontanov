# Professional Profile

## Trader, Managing Partner & Developer of HFT Trading Infrastructure

Managing Partner at [BDPB](https://bdpb.trading). Trading crypto perpetuals and spot with a latency-sensitive, tick-by-tick approach, and building the infrastructure behind it: low-latency exchange gateways, order-book engines, and execution tooling in Go. Author of a family of high-performance Go SDKs for centralized and on-chain exchanges (OKX, Bybit, Hyperliquid, MOEX, and more).

[![Go](https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/go-colored.svg)](https://go.dev/doc/) [![Python](https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/python-colored.svg)](https://www.python.org/) [![Ethereum](https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/ethereum-colored.svg)](https://ethereum.org/en/) [![PostgreSQL](https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/postgresql-colored.svg)](https://www.postgresql.org/) [![Docker](https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/docker-colored.svg)](https://www.docker.com/) [![Linux](https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/linux-colored.svg)](https://www.linux.org) [![Git](https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/git-colored.svg)](https://git-scm.com/)

## Professional Experience

### Managing Partner & Trader — BDPB

*Crypto derivatives (perpetuals) and spot; tick-by-tick data (trades, L2/L3); latency-sensitive execution*

#### Exchange Connectivity (Go SDK family)

- Designed and built a family of production-grade Go SDKs sharing one architecture: an allocation-conscious transport layer underneath thin, exchange-specific clients that mirror each venue's native naming and semantics.
- Centralized exchanges: [go-okx](https://github.com/tonymontanov/go-okx), [go-bybit](https://github.com/tonymontanov/go-bybit), [go-bitget](https://github.com/tonymontanov/go-bitget), [go-gate](https://github.com/tonymontanov/go-gate), [go-kucoin](https://github.com/tonymontanov/go-kucoin), [go-binance](https://github.com/tonymontanov/go-binance).
- On-chain / DEX venues: [go-hyperliquid](https://github.com/tonymontanov/go-hyperliquid), [go-lighter](https://github.com/tonymontanov/go-lighter), [go-aster](https://github.com/tonymontanov/go-aster), [go-variational](https://github.com/tonymontanov/go-variational).
- Traditional markets: [go-moex](https://github.com/tonymontanov/go-moex) — Moscow Exchange via ISS (REST), FIX 4.4 order entry and market-data feeds.

#### Low-Latency Market Data

- Order-book engines with snapshot + delta merging, sequence-gap detection, checksum verification (CRC32) and automatic resync for every supported venue.
- WebSocket layer with authentication, heartbeat, reconnect with jittered backoff, resubscription and typed dispatch for public and private channels (order book, trades, tickers, klines, orders, positions, executions, wallet).
- Zero-allocation hot path: hand-written MessagePack / JSON encoders, fixed-point `int64` price and size types instead of floats, lock-free nonce generation and rate-limit windows.

#### Execution & Order Management

- Full trading surface per venue: create / modify / cancel, batch operations, cancel-all, position and leverage management, demo and testnet modes.
- REST and WebSocket order entry behind a single API; SDK-side rate-limit accounting where the exchange provides none.
- Exchange-precision handling without floats (significant-figure and decimal rules, integer-price rules) enforced at the type level.
- Byte-for-byte signing compatibility with official reference SDKs (EIP-712 / secp256k1 for on-chain venues, HMAC-SHA256 for CEX), verified with generated reference vectors.

#### Reliability & Testing

- Contract tests on real exchange JSON fixtures, mock WebSocket server tests, property-based tests for signing, table-driven error-code mapping.
- Prometheus-shaped metrics interfaces and structured logging built into every SDK.

---

## Technical Skills

### Programming Languages

- Primary: Golang
- Secondary: Python

### Tools & Frameworks

- **Market Data**: WebSocket streams, L2/L3 order books, tick-by-tick trades, FIX 4.4
- **Backend**: PostgreSQL, Docker, Linux, Prometheus-style metrics
- **Exchange Integration**: OKX, Bybit, Bitget, Gate, KuCoin, Binance, Hyperliquid, Lighter, Aster, Variational, MOEX

### Specialized Expertise

- Latency-sensitive execution on crypto perpetuals and spot.
- Design of exchange gateways, order-book engines and low-latency infrastructure.
- Tick-by-tick data pipelines (trades, L2/L3) for research and live trading.

---

## Open Source

- Maintainer of the `go-*` exchange SDK family listed above — pure Go, minimal dependencies, HFT-oriented.

---

## Contact

- Website: [bdpb.trading](https://bdpb.trading)
- Telegram: [@tony_montanov](https://t.me/tony_montanov)
- X: [@montanovtony](https://x.com/montanovtony)
