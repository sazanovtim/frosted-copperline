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
  
- contracts/  
  Solidity contracts deployed to Base Sepolia for testnet validation:
  - control.sol — example contract showcasing conditional logic, assertions, and custom errors through classic FizzBuzz rules and time-based access control responses  
  - storage.sol — contract illustrating persistent state storage via constructor initialization, variable visibility (public vs private), storage packing inspection, and custom error–based validation logic   

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

Copyright (c) 2025

---

## Author

GitHub: https://github.com/sazanovtim  
Email: ozzisyreetapdeansaw@gmail.com  
Public contact: https://x.com/sazanovtim  

---

## Testnet Deployment (Base Sepolia)

As part of pre-production validation, one or more contracts may be deployed to the Base Sepolia test network to confirm correct behavior and tooling compatibility.

Network: Base Sepolia  
chainId (decimal): 84532  
Explorer: https://sepolia.basescan.org  

Contract "control" address:  
0xe5e5812910af30dc15792b6a1d52ca9f3d13b867

Deployment and verification:
- https://sepolia.basescan.org/address/0xe5e5812910af30dc15792b6a1d52ca9f3d13b867
- https://sepolia.basescan.org/0xe5e5812910af30dc15792b6a1d52ca9f3d13b867/0#code  

Contract "storage" address:  
0x2fb6828b539854258b62af995fcac94a6476d72c

Deployment and verification:
- https://sepolia.basescan.org/address/0x2fb6828b539854258b62af995fcac94a6476d72c
- https://sepolia.basescan.org/0x2fb6828b539854258b62af995fcac94a6476d72c/0#code  

These testnet deployments provide a controlled environment for validating Base tooling, account abstraction flows, and read-only onchain interactions prior to Base Mainnet usage.
