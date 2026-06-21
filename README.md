# The Web3 developer link stack

> **Note:** This is an educational resource, not financial, legal, or security advice. Always verify tooling, pricing, limits, and compliance requirements before you put anything in production.

This repository is a practical Web3 handbook from the Cryptonly team. It started as a messy internal bookmark folder: RPC providers we compare, docs we send to new engineers, faucets we forget until testnet day, wallets we test, compliance tools we keep an eye on, and explorers we open when something looks odd.

It is not meant to be a “top 100 crypto tools” SEO dump. It is a practical starting stack for developers and product owners building with crypto payments, wallets, smart contracts, or on-chain data. Some links are tools we use, some are tools we are evaluating, and some are simply useful defaults when you need to orient yourself quickly.

---

## What's inside

- [How to use this repository](#how-to-use-this-repository)
- [1. Blockchain node providers](#1-blockchain-node-providers)
- [2. AML, KYT, KYC, and compliance services](#2-aml-kyt-kyc-and-compliance-services)
- [3. Developer documentation and SDKs](#3-developer-documentation-and-sdks)
- [4. Testnet faucets](#4-testnet-faucets)
- [5. Smart contract development frameworks](#5-smart-contract-development-frameworks)
- [6. Block explorers and analytics](#6-block-explorers-and-analytics)
- [7. Wallet and identity infrastructure](#7-wallet-and-identity-infrastructure)
- [8. Security and auditing tools](#8-security-and-auditing-tools)
- [9. Price oracles and data feeds](#9-price-oracles-and-data-feeds)
- [Bonus: on-chain development kits for non-EVM ecosystems](#bonus-on-chain-development-kits-for-non-evm-ecosystems)
- [Contributing](#contributing)

---

## How to use this repository

If you are building a product, do not try to adopt everything here. Start with the category that blocks your next decision:

- Need balances, transactions, or contract reads? Start with node providers and explorers.
- Need to launch a checkout, wallet flow, or dApp? Read the SDK and wallet sections.
- Touching customer funds? Look at compliance and security before you ship.
- Testing a prototype? Grab faucets, use a testnet, and keep mainnet keys far away from experiments.

Our bias is simple: prefer boring infrastructure for production and fun tools for prototypes.

---

## 1. Blockchain node providers

Most teams should not run their own blockchain infrastructure on day one. A managed RPC provider lets you read balances, submit transactions, listen for events, and build product flows without babysitting nodes.

### Multi-chain / EVM

- **[Alchemy](https://www.alchemy.com/)** - A strong default for EVM teams, especially if you want dashboards, enhanced APIs, and good developer docs.
- **[Infura](https://infura.io/)** - Still one of the standard Ethereum/IPFS choices. Useful when you want something established and widely documented.
- **[QuickNode](https://www.quicknode.com/)** - Good multi-chain coverage, including Bitcoin and Solana, with add-ons when a plain RPC endpoint is not enough.
- **[Chainstack](https://chainstack.com/)** - Worth comparing if you care about cloud/provider flexibility and predictable infrastructure setup.
- **[GetBlock](https://getblock.io/)** - Broad chain support with shared and dedicated node options.
- **[ANKR](https://www.ankr.com/)** - Useful when you want a decentralized RPC angle or broad EVM coverage.

### Bitcoin / Lightning

- **[QuickNode Bitcoin](https://www.quicknode.com/chains/btc)** – Bitcoin RPC with full archival options.
- **[BlockCypher](https://www.blockcypher.com/)** – Bitcoin, Litecoin, Doge; simple REST API.
- **[Mempool.space API](https://mempool.space/docs/api)** – Great for fee estimation, mempool data, and transaction inspection.
- **[LND (Lightning Network Daemon)](https://lightning.engineering/)** – The serious route if you need to run your own Lightning node.
- **[Voltage](https://voltage.cloud/)** – Managed Lightning nodes when you want to avoid the operational burden early.

### Tron

- **[TronGrid](https://www.trongrid.io/)** – Official Tron node provider. We are evaluating it because Tron is still hard to ignore for stablecoin payment flows.

**Cryptonly note:** RPC providers look interchangeable until you depend on them for payment status. Test rate limits, latency, retries, and historical data access before the provider becomes part of your checkout flow.

---

## 2. AML, KYT, KYC, and compliance services

If your product touches customer funds, compliance is not optional. The right setup depends on your jurisdiction, asset support, risk appetite, and whether you need wallet screening, transaction monitoring, sanctions checks, or full onboarding.

- **[Chainalysis](https://www.chainalysis.com/)** - Enterprise-grade KYT, investigations, and risk tooling. Often the name larger teams start with.
- **[OnChainRisk](https://onchainrisk.io/)** - Interesting for smaller projects that still need API-based wallet or transaction risk checks.
- **[CipherTrace (Mastercard)](https://ciphertrace.com/)** - Focuses on VASP risk, traveler rule workflows, and institutional compliance needs.
- **[Scorechain](https://www.scorechain.com/)** - EU-based platform with screening and analytics across major assets.
- **[Sanction Scanner](https://sanctionscanner.com/)** - Useful if you need sanctions, PEP, and onboarding checks alongside crypto-specific tooling.
- **[Coinfirm](https://www.coinfirm.com/)** - Broad asset coverage, including Bitcoin, Tron, and DeFi-related risk signals.

**Watch out:** Do not choose a compliance provider from a pricing page alone. Ask what chains they support, how they score stablecoin transfers, what evidence you can export, and how false positives are handled.

---

## 3. Developer documentation and SDKs

Good docs save more time than clever abstractions. These are the references we would rather have open before guessing from an old Stack Overflow answer.

### Ethereum / EVM

- **[Ethereum.org Developers Portal](https://ethereum.org/en/developers/)** – The canonical starting point.
- **[Ethers.js](https://docs.ethers.org/)** – The long-running JavaScript library many EVM projects still rely on.
- **[Web3.js](https://web3js.readthedocs.io/)** – Older, still common, and useful when maintaining existing integrations.
- **[Viem](https://viem.sh/)** – A modern TypeScript-first interface that is pleasant for new EVM codebases.
- **[Solidity Documentation](https://docs.soliditylang.org/)** – Smart contract language reference.

### Bitcoin

- **[Bitcoin Developer Guide](https://developer.bitcoin.org/)** – Core documentation.
- **[Learn Me a Bitcoin](https://learnmeabitcoin.com/)** – Excellent conceptual and code walkthroughs.
- **[BitcoinJS Lib](https://github.com/bitcoinjs/bitcoinjs-lib)** – JavaScript library for Bitcoin transactions.
- **[BDK (Bitcoin Dev Kit)](https://bitcoindevkit.org/)** – Rust & Swift library for wallet building.
- **[Taproot Assets](https://docs.lightning.engineering/)** – For teams exploring asset issuance on Bitcoin through the Lightning ecosystem.

### Tron

- **[Tron Developer Hub](https://developers.tron.network/)** – Official docs, APIs, and tutorials.
- **[TronWeb](https://tronweb.network/)** – JavaScript library similar to Web3.js for Tron.
- **[TronBox](https://github.com/tronprotocol/tron-box)** – Tron's smart contract development framework.

### Solana & others
- **[Solana Docs](https://docs.solana.com/)** – Core concepts and JSON RPC.
- **[Anchor Framework](https://www.anchor-lang.com/)** – Solana development simplified.
- **[CosmWasm](https://docs.cosmwasm.com/)** – For Cosmos SDK chains.

---

## 4. Testnet faucets

Faucets are boring until you need them five minutes before a demo. Keep a few options bookmarked because limits, outages, and account requirements change often.

### Ethereum & EVM
- **[Paradigm Faucet](https://faucet.paradigm.xyz/)** – Multi-chain (Sepolia, Holesky, Optimism, etc.).
- **[Chainlink Faucet](https://faucets.chain.link/)** – For Chainlink-related testnets.
- **[Alchemy Faucet](https://www.alchemy.com/faucets/)** – Sepolia ETH, Polygon Mumbai. Requires Alchemy account.
- **[QuickNode Multi-Chain Faucet](https://faucet.quicknode.com/)** – Supports many testnets.

### Bitcoin
- **[Coinfaucet.eu](https://coinfaucet.eu/en/btc-testnet/)** – Reliable Bitcoin testnet faucet.
- **[Bitcoin Testnet Faucet (testnet-faucet.com)](https://testnet-faucet.com/btc-testnet/)** – Drip every few hours.
- **[Mempool.space Testnet Faucet](https://mempool.space/testnet/faucet)** – Convenient, integrated with explorer.

### Tron
- **[Shasta Faucet (official)](https://www.trongrid.io/shasta/#request)** – Tron's Shasta testnet faucet.
- **[Tronscan Faucet](https://www.tronscan.org/)** – Test TRX on Shasta.

### Other chains

- **[Stakely Faucet](https://stakely.io/en/faucet)** – Covers Bitcoin, Cosmos, Solana, and many more.
- **[Bware Labs Faucet](https://bwarelabs.com/faucets)** – Multi-chain including Avalanche, Fantom, etc.

**Small habit that helps:** Write down which testnet, asset, and faucet you used in the issue or pull request. Future you will thank past you when a test address looks unfamiliar.

---

## 5. Smart contract development frameworks

If you are writing contracts, your framework should make testing and deployment repeatable. If it only helps you compile, it is not doing enough.

- **[Hardhat](https://hardhat.org/)** – Most popular EVM environment; great plugin ecosystem.
- **[Foundry](https://book.getfoundry.sh/)** – Fast, Solidity-native, and great for test-heavy workflows. We use it for some internal contract testing.
- **[Remix IDE](https://remix.ethereum.org/)** – Browser-based, perfect for quick prototyping.
- **[Anchor](https://www.anchor-lang.com/)** – Solana's framework; if you're outside EVM.
- **[TronBox](https://github.com/tronprotocol/tron-box)** – Tron development and testing.

---

## 6. Block explorers and analytics

Explorers are your first debugging UI. When a payment, transfer, contract call, or balance looks wrong, this is where you check whether the chain agrees with your backend.

### Ethereum & EVM
- **[Etherscan](https://etherscan.io/)** – Essential.
- **[PolygonScan](https://polygonscan.com/)**, **[BscScan](https://bscscan.com/)** – Chain-specific.
- **[Blockscout](https://www.blockscout.com/)** – Open-source explorer for many EVM chains.

### Bitcoin
- **[Mempool.space](https://mempool.space/)** – Beautiful real-time Bitcoin explorer.
- **[Blockchair](https://blockchair.com/)** – Universal blockchain explorer, covers Bitcoin, Litecoin, etc.

### Tron
- **[Tronscan](https://tronscan.org/)** – Official Tron explorer.

### Cross-chain analytics

- **[Dune Analytics](https://dune.com/)** – Community dashboards and SQL-based analysis, mostly around EVM ecosystems.
- **[Zapper](https://zapper.xyz/)** / **[Zerion](https://zerion.io/)** – Human-readable portfolio and wallet views.
- **[Nansen](https://www.nansen.ai/)** – Wallet labels and analytics, especially useful for EVM research.

---

## 7. Wallet and identity infrastructure

Wallet connection is not just a button. It affects onboarding, support, recovery, fraud handling, and whether non-crypto-native users can complete the flow.

### EVM
- **[WalletConnect](https://walletconnect.com/)** – Universal bridge for mobile wallets.
- **[RainbowKit](https://www.rainbowkit.com/)** – Beautiful React wallet connection.
- **[Privy](https://www.privy.io/)** – Embeddable wallets and auth.
- **[Magic](https://magic.link/)** – Passwordless login with auto-created wallet.

### Bitcoin
- **[Leather (formerly Hiro)](https://leather.io/)** – Bitcoin wallet for Stacks and plain BTC.
- **[UniSat](https://unisat.io/)** – Popular for BRC-20 and Ordinals; provides API.
- **[Xverse](https://www.xverse.app/)** – Bitcoin wallet with Stacks and BNS support.

### Tron
- **[TronLink](https://www.tronlink.org/)** – Official browser extension and mobile wallet.
- **[TronWeb's wallet integration](https://developers.tron.network/docs/tronlink-integration)** – Docs for connecting dApps.

---

## 8. Security and auditing tools

Security tooling is not a substitute for review, but it catches mistakes humans miss and forces teams to write down assumptions.

- **[OpenZeppelin Contracts](https://www.openzeppelin.com/contracts/)** – Standard-compliant EVM contract libraries.
- **[Slither](https://github.com/crytic/slither)** – Static analysis for Solidity.
- **[Echidna](https://github.com/crytic/echidna)** – Fuzzing for EVM smart contracts.
- **[Tenderly](https://tenderly.co/)** – Debugging, monitoring, simulation; EVM.
- **[Immunefi](https://immunefi.com/)** – Bug bounty platform for all major ecosystems.
- **For Bitcoin scripts:** Manual review is key; tools like **[Minsc](https://min.sc/)** can help visualize script behavior.
- **For Tron:** **[TronEye](https://troneye.com/)** for basic contract verification.

**Production rule:** If a contract can move funds, it deserves tests, review, monitoring, and a rollback or pause story. Tools help, but process matters more.

---

## 9. Price oracles and data feeds

Any product that prices assets, triggers contract logic, or calculates payment amounts from market data needs to be careful about where that data comes from.

- **[Chainlink Data Feeds](https://docs.chain.link/data-feeds)** – Industry standard, available on 20+ chains (EVM).
- **[Pyth Network](https://pyth.network/)** – High-frequency financial data, popular on Solana, Sui, and also EVM.
- **[RedStone](https://redstone.finance/)** – Modular oracles, gas-efficient.
- **[API3](https://api3.org/)** – First-party oracles, DAO-governed.
- **Bitcoin/Tron:** Native oracle options are more limited. You will likely use bridging services, multi-chain oracle networks, or backend-side pricing depending on the product.

---

## Bonus: on-chain development kits for non-EVM ecosystems

Not every crypto product is EVM-first. If your users or assets live elsewhere, start with the native ecosystem instead of forcing an Ethereum mental model onto every chain.

- **[Bitcoin Dev Kit (BDK)](https://bitcoindevkit.org/)** – Rust/Swift for wallet apps.
- **[Tron Developer Suite](https://developers.tron.network/)** - TronWeb + TronGrid.
- **[Solana](https://docs.solana.com/)**
- **[Aptos](https://aptos.dev/)**
- **[Sui](https://docs.sui.io/)**
- **[Near](https://docs.near.org/)**
- **[Starknet](https://docs.starknet.io/)**
- **[Cosmos SDK](https://tutorials.cosmos.network/)**

---

## Contributing

This README is the canonical version of the Web3 handbook. We keep it updated as we discover new tools, retire old ones, and hear from developers building real things.

Repository: **[github.com/cryptonly-lib/web3-handbook](https://github.com/cryptonly-lib/web3-handbook)**

- Open an issue if a link is broken, outdated, or misleading.
- Open a pull request if you want to add a tool, improve a description, or reorganize a section.
- Include a short reason for every suggested tool so the list stays curated instead of becoming a dump.

## About Cryptonly

Curated with care by the Cryptonly team. We build payment tools for the same web3 you are developing on.

Questions or suggestions? Visit [cryptonly.net](https://cryptonly.net).
