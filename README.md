# AlstraNet

## Introduction

Welcome to the AlstraNet project, a Zero-Knowledge (ZK) Rollup solution. AlstraNet is designed to enhance blockchain scalability, security, and privacy while maintaining decentralization.

## Project Structure

This README provides an overview of the project's technical aspects. We use a monorepo project structure, TypeScript for development, Hardhat for smart contract development, and Docker for containerization.

### 1. Core Infrastructure

#### 1.1 On-Chain Contracts

##### Rollup Smart Contracts

- **Rollup Manager Contract:** Manages the state and interactions within the ZK Rollup. It tracks user balances, contract states, and data availability using a Merkle tree.

- **Verifier Contract:** Specializes in verifying cryptographic proofs (e.g., zk-SNARKs) for off-chain transactions and state transitions.

- **Data Availability Contract:** Ensures data availability using a Merkle tree and tracks the availability of transaction and state data.

#### 1.2 Off-Chain Virtual Machine: Execution Engine

- Utilizes zkEVM for transaction processing, offering privacy-preserving computations and efficient verification of smart contract code.

- Responsible for executing user transactions, maintaining off-chain state, creating batches of transactions, and generating Merkle roots.

- Ensures data availability and validation through zero-knowledge proofs (zk-SNARKs or zk-STARKs).

- Submits validated batches to the Rollup Manager Contract on Ethereum Layer 1 (L1).

### 2. Decentralized Network Architecture

- **Sequencers:** Independently operate to collect and sequence transactions, organizing them for off-chain execution.

- **Executors:** Execute transactions within batches off-chain, adhering to Rollup rules.

- **Provers:** Collaborate with Sequencers to generate efficient zero-knowledge proofs.

- **Validator Network:** Forms a decentralized network to validate transactions and proofs.

- **Relayer:** Acts as an intermediary between the off-chain ZK Rollup network and Ethereum Layer 1 (L1) contracts.

### 3. P2P Network Protocol

- **Protocol Version:** 1.0

- Network involves Sequencers, Executors, Provers, Validators, and Relayers.

- Structured data exchange format and message format for efficient communication.

- Operations include discovery, data propagation, data validation, data relaying, L1 submission, data availability, governance, and monitoring.

### Protocol Events

1. Node Discovery and Connection
2. Transaction Broadcasting
3. Proof Generation
4. Proof Validation
5. State Update Propagation
6. Data Relaying for L1 Submission
7. Submission to Layer 1 (L1)
8. Data Availability and Monitoring
9. Governance and Upgradability

## Getting Started

To get started with AlstraNet, follow these steps:

1. Clone the AlstraNet repository from our monorepo.

2. Navigate to the project's root directory and install the required dependencies using NPM.

3. Set up the Ethereum development environment using Hardhat and Docker.

4. Run the provided scripts for deploying smart contracts and starting the ZK Rollup network.

5. Interact with the network and contribute to its development.

## Contributing

We welcome contributions from the community. Please refer to our contribution guidelines in the project repository for details on how to get involved.

## Support

For questions, issues, or support, please contact our team or create an issue in the project repository.
## Donate

If you find AlstraNet valuable and would like to support our project, you can make donations in Bitcoin (BTC) and Ethereum (ETH) to the following wallet addresses:

- Bitcoin (BTC):
  - Wallet Address: `bc1qe5apr7222ksw03pdd42kf2588aaewxlukyg5sv`

- Ethereum (ETH):
  - Wallet Address: `0xDEf84737126AECBE617634f0009d2827b3860a62`

## License

AlstraNet is open-source software licensed under the [MIT License](LICENSE.md). We encourage collaboration and contributions from the community.

Thank you for joining us on this journey to enhance Ethereum's scalability and security through AlstraNet!
