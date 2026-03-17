# 🪙 Simple Token Smart Contract

## 📌 Introduction
This project demonstrates the design, development, and deployment of a custom ERC-20–style token on a local blockchain environment using Solidity. It was created as part of a hands-on blockchain development session to gain a deeper practical understanding of how cryptocurrencies work at a fundamental level. The project covers key concepts such as smart contracts, token creation, deployment, and interaction within a decentralized setup, helping to illustrate how digital assets like Bitcoin and tokens operate within a blockchain ecosystem.

<img width="1600" height="580" alt="image" src="https://github.com/user-attachments/assets/ed134c03-83ba-4746-98ba-4120a6b68233" />

<img width="1863" height="500" alt="image" src="https://github.com/user-attachments/assets/c85fdc91-7988-48a1-b387-688d50f0ef98" />



## 📜 Project Description
The smart contract implements a simple fungible token with a fixed supply. Once deployed, tokens are minted to the contract deployer's address. Users can transfer tokens to any other wallet on the same network.

This project helps beginners understand key blockchain concepts such as:
- Smart contracts
- State variables
- Token balance tracking
- Deployment workflow
- Local blockchain testing

## ✅ What It Does
- Creates a token with a fixed supply
- Allows wallet-to-wallet transfers
- Stores balances on-chain
- Shows real blockchain transaction behavior
- Teaches deployment steps and verification flow

## 🚀 Features
- 🔐 Decentralized – runs on blockchain, not a server
- 💸 Transferable tokens between accounts
- 📦 Fixed total supply
- 🧾 Transparent on-chain balances
- ⚙️ Easy to deploy locally (Ganache/Hardhat)

## 🌐 Network
- **Network used:** HeLa Testnet
- **RPC URL:** `https://testnet-rpc.helachain.com`
- **Chain id:** 666888

## 🧾 Verified Source
Source code is uploaded in this repository under `/contracts`.

> Verification on block explorers is optional for local networks.

## 🔗 Contract Address
Network: HeLa Testnet 

Contract Address: `0xA17048cc69F67C8A05226049718109F15fbD21d9`

Verified Source: Verified through Remix (Sourcify & Metadata Match)


## 🧠 Smart Contract Code

```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.9;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

/// @title MyToken - A basic ERC20 Token on HeLa Chain
/// @custom:dev-run-script ./scripts/deploy.js

contract MyToken is ERC20 {
    constructor(uint256 initialSupply) ERC20("KritHela", "KG") {
       _mint(msg.sender, initialSupply * 10 ** decimals());
    }
}
