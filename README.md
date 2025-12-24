# Frosted Copperline (Built for Base)

Frosted Copperline is a browser-first Base utility designed to validate Base network identity and observe public onchain state through strictly read-only operations.

---

## What this project provides

This repository exists as a practical verification surface for Base developers. It emphasizes clarity over abstraction and is suitable for diagnostics, demos, and tooling validation without signing or broadcasting transactions.

Key use cases include:
- Confirming Base RPC connectivity  
- Validating chainId values (8453 / 84532)  
- Inspecting balances, nonces, and blocks  
- Jumping to Basescan for independent confirmation  

---

## Repository layout

- app.frosted-copperline.ts  
  Browser entry script handling wallet connection, chain validation, and read-only RPC queries.

- config/base.networks.json  
  Static Base network configuration including chainIds, RPC endpoints, and explorers.

- docs/architecture.md  
  Design notes describing the read-only model, Base alignment, and dependency choices.

- docs/validation-notes.md  
  Chronological record of Base Sepolia validation steps and verification links.

- scripts/sample-addresses.json  
  Example addresses used for repeatable read-only checks.

- contracts/  
  Solidity contracts deployed to Base Sepolia for testnet validation:
  - your_contract.sol — minimal contract used to validate deployment and verification flow  
  - your_contract.sol — simple stateful contract for interaction testing  
  - your_contract.sol — lightweight contract used for read-only queries  

- package.json  
  Dependency manifest referencing Coinbase SDKs and multiple Base and Coinbase repositories.

- README.md  
  Primary technical documentation.

---

## Supported networks

Base Mainnet  
chainId (decimal): 8453  
Explorer: https://basescan.org  

Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

---

## Tooling and ecosystem alignment

This project intentionally pulls from official ecosystems:
- Coinbase Wallet SDK for EIP-1193 wallet access  
- OnchainKit references for Base-aligned primitives and account abstraction context  
- viem for typed, efficient, read-only RPC communication  
- Multiple Base and Coinbase GitHub repositories included as dependencies  

---

## License

MIT License

Copyright (c) 2025 YOUR_NAME

---

## Author

GitHub: https://github.com/your-handle  
Email: you@example.com  
Public contact: https://x.com/your-handle  

---

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract #1 address:  
your_address

Deployment and verification:
- https://sepolia.basescan.org/address/your_address
- https://sepolia.basescan.org/your_address/0#code  

Contract #2 address:  
your_address

Deployment and verification:
- https://sepolia.basescan.org/address/your_address
- https://sepolia.basescan.org/your_address/0#code  

Contract #3 address:  
your_address

Deployment and verification:
- https://sepolia.basescan.org/address/your_address
- https://sepolia.basescan.org/your_address/0#code  

These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.
