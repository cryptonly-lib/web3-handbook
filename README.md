# 95% of the links you might need as a Web3 (Crypto) Developer or product owner

> **Disclaimer: All information (tools, links, articles, text, images, etc.) is provided for educational purposes only! All information is based on data from public sources. You are solely responsible for your actions, not the authors!**

---

## 1. Blockchain Node Providers
Access on-chain data without running your own infrastructure.

### Multi-chain / EVM
- **[Alchemy](https://www.alchemy.com/)** – Generous free tier (300M compute units/month).
- **[Infura](https://infura.io/)** – The veteran; solid Ethereum/IPFS access, 100K requests/day free. 
- **[QuickNode](https://www.quicknode.com/)** – Pay-as-you-go, worldwide edge nodes, supports 20+ chains including Bitcoin, Solana.
- **[Chainstack](https://chainstack.com/)** – Multi-cloud, free developer plan with 3M requests/month.
- **[GetBlock](https://getblock.io/)** – Affordable shared nodes, 40K requests/day free tier; supports Bitcoin, Tron, Solana.
- **[ANKR](https://www.ankr.com/)** – Decentralized RPC service, generous free tier; supports Bitcoin, BNB Chain, Polygon, etc.

### Bitcoin / Lightning
- **[QuickNode Bitcoin](https://www.quicknode.com/chains/btc)** – Bitcoin RPC with full archival options.
- **[BlockCypher](https://www.blockcypher.com/)** – Bitcoin, Litecoin, Doge; simple REST API.
- **[Mempool.space API](https://mempool.space/docs/api)** – Free, excellent for fee estimation and mempool data.
- **[LND (Lightning Network Daemon)](https://lightning.engineering/)** – If you need your own Lightning node.
- **[Voltage](https://voltage.cloud/)** – Managed Lightning nodes, easy to spin up.

### Tron
- **[TronGrid](https://www.trongrid.io/)** – Official Tron node provider, generous free tier. (we're evaluating this)

**Pro tip:** Most node providers offer a free tier sufficient for development and small-scale apps.

---

## 2. AML / KYC & Compliance Services
If you handle user funds, compliance is not optional. Here's what's available and indicative pricing.

- **[Chainalysis](https://www.chainalysis.com/)** – The market leader for big guys. Enterprise pricing (typically $20K+/year), includes KYT and many on-chain investigation tools.
- **[OnChainRisk](https://onchainrisk.io/)** – Probably the best solution for smaller projects. API accessible for as low as $49/month.
- **[CipherTrace (Mastercard)](https://ciphertrace.com/)** – Focuses on traveler rule compliance and VASP risk assessment.
- **[Scorechain](https://www.scorechain.com/)** – EU-based, offers pay-per-use and monthly plans starting from ~€29/month for light screening. Supports Bitcoin, Ethereum, Litecoin, and stablecoins.
- **[Sanction Scanner](https://sanctionscanner.com/)** – Simple API for sanction and PEP screening, plans from $49/month.
- **[Coinfirm](https://www.coinfirm.com/)** – Covers 1500+ assets including Bitcoin, Tron, and DeFi tokens.

**Note:** Many offer sandbox environments. For early-stage projects, start with Scorechain's basic plan or OnChainRisk's entry tier.

---

## 3. Developer Documentation & SDKs
Bookmark these; you'll be back often.

### Ethereum / EVM
- **[Ethereum.org Developers Portal](https://ethereum.org/en/developers/)** – The canonical starting point.
- **[Ethers.js](https://docs.ethers.org/)** – The go-to JavaScript library for EVM interactions.
- **[Web3.js](https://web3js.readthedocs.io/)** – Still widely used, comprehensive.
- **[Viem](https://viem.sh/)** – Modern TypeScript interface with great developer experience.
- **[Solidity Documentation](https://docs.soliditylang.org/)** – Smart contract language reference.

### Bitcoin
- **[Bitcoin Developer Guide](https://developer.bitcoin.org/)** – Core documentation.
- **[Learn Me a Bitcoin](https://learnmeabitcoin.com/)** – Excellent conceptual and code walkthroughs.
- **[BitcoinJS Lib](https://github.com/bitcoinjs/bitcoinjs-lib)** – JavaScript library for Bitcoin transactions.
- **[BDK (Bitcoin Dev Kit)](https://bitcoindevkit.org/)** – Rust & Swift library for wallet building.
- **[Taproot Assets](https://docs.lightning.engineering/)** – For issuing assets on Bitcoin (used with LND).

### Tron
- **[Tron Developer Hub](https://developers.tron.network/)** – Official docs, APIs, and tutorials.
- **[TronWeb](https://tronweb.network/)** – JavaScript library similar to Web3.js for Tron.
- **[TronBox](https://github.com/tronprotocol/tron-box)** – Tron's smart contract development framework.

### Solana & others
- **[Solana Docs](https://docs.solana.com/)** – Core concepts and JSON RPC.
- **[Anchor Framework](https://www.anchor-lang.com/)** – Solana development simplified.
- **[CosmWasm](https://docs.cosmwasm.com/)** – For Cosmos SDK chains.

---

## 4. Testnet Faucets
Free test tokens to mimic real transactions.

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

### Others
- **[Stakely Faucet](https://stakely.io/en/faucet)** – Covers Bitcoin, Cosmos, Solana, and many more.
- **[Bware Labs Faucet](https://bwarelabs.com/faucets)** – Multi-chain including Avalanche, Fantom, etc.

---

## 5. Smart Contract Development Frameworks
Streamline compiling, testing, and deployment.

- **[Hardhat](https://hardhat.org/)** – Most popular EVM environment; great plugin ecosystem.
- **[Foundry](https://book.getfoundry.sh/)** – Blazing fast, Solidity-native. (used by Cryptonly for some internal tests)
- **[Remix IDE](https://remix.ethereum.org/)** – Browser-based, perfect for quick prototyping.
- **[Anchor](https://www.anchor-lang.com/)** – Solana's framework; if you're outside EVM.
- **[TronBox](https://github.com/tronprotocol/tron-box)** – Tron development and testing.

---

## 6. Block Explorers & Analytics
Inspect transactions, contracts, and network activity.

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
- **[Dune Analytics](https://dune.com/)** – Community dashboards (EVM mostly).
- **[Zapper](https://zapper.xyz/)** / **[Zerion](https://zerion.io/)** – Human-readable portfolio views.
- **[Nansen](https://www.nansen.ai/)** – Wallet labeling, but mostly EVM.

---

## 7. Wallet & Identity Infrastructure
Connect your dApp to users' wallets with ease.

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

## 8. Security & Auditing Tools
Make your smart contracts and code safer.

- **[OpenZeppelin Contracts](https://www.openzeppelin.com/contracts/)** – Standard-compliant EVM contract libraries.
- **[Slither](https://github.com/crytic/slither)** – Static analysis for Solidity.
- **[Echidna](https://github.com/crytic/echidna)** – Fuzzing for EVM smart contracts.
- **[Tenderly](https://tenderly.co/)** – Debugging, monitoring, simulation; EVM.
- **[Immunefi](https://immunefi.com/)** – Bug bounty platform for all major ecosystems.
- **For Bitcoin scripts:** Manual review is key; tools like **[Minsc](https://min.sc/)** can help visualize.
- **For Tron:** **[TronEye](https://troneye.com/)** for basic contract verification.

---

## 9. Price Oracles & Data Feeds
Trustworthy off-chain data for your contracts.

- **[Chainlink Data Feeds](https://docs.chain.link/data-feeds)** – Industry standard, available on 20+ chains (EVM).
- **[Pyth Network](https://pyth.network/)** – High-frequency financial data, popular on Solana, Sui, and also EVM.
- **[RedStone](https://redstone.finance/)** – Modular oracles, gas-efficient.
- **[API3](https://api3.org/)** – First-party oracles, DAO-governed.
- **Bitcoin/Tron:** For native oracles, you'll likely use bridging services or multi-chain oracle networks; Chainlink and Pyth have limited support. Check official docs.

---

## Bonus: On-Chain Development Kits (for non-EVM)
- **[Bitcoin Dev Kit (BDK)](https://bitcoindevkit.org/)** – Rust/Swift for wallet apps.
- **[Tron Developer Suite](https://developers.tron.network/)** - TronWeb + TronGrid.
- **[Solana](https://docs.solana.com/)**
- **[Aptos](https://aptos.dev/)**
- **[Sui](https://docs.sui.io/)**
- **[Near](https://docs.near.org/)**
- **[Starknet](https://docs.starknet.io/)**
- **[Cosmos SDK](https://tutorials.cosmos.network/)**

---

That's the toolbox. It's not an exhaustive list - there are amazing niche tools for each category — but this set will cover 95% of what a web3 developer needs to ship a working product, whether on Ethereum, Bitcoin, Tron, or the wider multi-chain world. We keep this page updated regularly. If a link you love is missing, let us know via [our website](https://cryptonly.net) and we'll add it.

*Curated with care by the Cryptonly team. We build payment tools for the same web3 you're developing on.*

---

## Contributing

This list is a community resource, and we welcome contributions from developers and product owners across the web3 space. If you've spotted a broken link, want to suggest a tool we should add, or have an idea to improve this page:

- Open an **issue** or a **pull request** in this GitHub repo
- Reach out directly on the [Cryptonly website](https://cryptonly.net)

Let's keep this reference useful for the next generation of web3 builders.
