# Professional Profile

## Trader, Managing Partner & Developer of HFT Trading Infrastructure

Managing Partner at [BDPB](https://bdpb.trading). Trading crypto perpetuals and spot with a latency-sensitive, tick-by-tick approach, and building the infrastructure behind it: low-latency exchange gateways, order-book engines, and execution tooling in Go. Former head of the market-microstructure direction and developer of the SpreadFighter analytics platform. Author of a family of high-performance Go SDKs for centralized and on-chain exchanges (OKX, Bybit, Hyperliquid, MOEX, and more).

<p align="left">
  <a href="https://go.dev/doc/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/go-colored.svg" width="36" height="36" alt="Go" /></a>
  <a href="https://www.rust-lang.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/rust-colored.svg" width="36" height="36" alt="Rust" /></a>
  <a href="https://isocpp.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/cplusplus-colored.svg" width="36" height="36" alt="C++" /></a>
  <a href="https://www.python.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/python-colored.svg" width="36" height="36" alt="Python" /></a>
  <a href="https://www.typescriptlang.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/typescript-colored.svg" width="36" height="36" alt="TypeScript" /></a>
  <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/javascript-colored.svg" width="36" height="36" alt="JavaScript" /></a>
  <a href="https://ethereum.org/en/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/ethereum-colored.svg" width="36" height="36" alt="Ethereum" /></a>
  <a href="https://www.postgresql.org/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/postgresql-colored.svg" width="36" height="36" alt="PostgreSQL" /></a>
  <a href="https://www.docker.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/docker-colored.svg" width="36" height="36" alt="Docker" /></a>
  <a href="https://www.linux.org" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/linux-colored.svg" width="36" height="36" alt="Linux" /></a>
  <a href="https://git-scm.com/" target="_blank" rel="noreferrer"><img src="https://raw.githubusercontent.com/danielcranney/readme-generator/main/public/icons/skills/git-colored.svg" width="36" height="36" alt="Git" /></a>
</p>

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

- Full trading surface per venue: from primitives — create / modify / cancel, batch operations, cancel-all, etc. — up to complex algorithmic execution (TWAP, Implementation Shortfall, Grid, Chase, etc.). Position and leverage management, demo and testnet modes.
- REST and WebSocket order entry behind a single API; SDK-side rate-limit accounting where the exchange provides none.
- Exchange-precision handling without floats (significant-figure and decimal rules, integer-price rules) enforced at the type level.
- Byte-for-byte signing compatibility with official reference SDKs (EIP-712 / secp256k1 for on-chain venues, HMAC-SHA256 for CEX), verified with generated reference vectors.

#### Reliability & Testing

- Contract tests on real exchange JSON fixtures, mock WebSocket server tests, property-based tests for signing, table-driven error-code mapping.
- Prometheus-shaped metrics interfaces and structured logging built into every SDK.

---

### Head of Market Microstructure & Analytics Platform Developer — SpreadFighter

*1.5 years, analytical platform for crypto markets*

- Led the market-microstructure direction: research on order-flow, spreads, liquidity and execution quality across crypto venues.
- Developed the SpreadFighter analytical platform (JavaScript / TypeScript): real-time and historical analytics on tick-by-tick trades and order-book data.
- Turned microstructure research into tools and metrics used by traders for venue selection, timing and execution.

---

## Technical Skills

### Programming Languages

- Primary: Golang, Rust, C++
- Secondary: Python, TypeScript / JavaScript, Pinescript

### Tools & Frameworks

- **Market Data**: WebSocket streams, L2/L3 order books, tick-by-tick trades, FIX 4.4
- **Frontend / Analytics**: TypeScript, JavaScript
- **TradingView**: Pinescript indicators and strategies
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
