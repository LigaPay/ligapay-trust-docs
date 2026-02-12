# LigaPay™ Key Generation & Signing Flow

**Product:** LigaPay™  
**Operating Entity:** Liga Techs, Inc. (doing business as LigaPay™)  
**Last Updated:** February 2026  

---

## Overview

This document describes the high-level key generation and transaction signing flow used by LigaPay™.

The purpose of this document is to clearly demonstrate that **all cryptographic operations occur client-side**, and that LigaPay™ backend systems **never access, store, or control private keys or user assets**.

---

## 1. Client-Side Key Generation

- Cryptographic key pairs are generated **locally on the user’s device**.
- Key generation uses industry-standard cryptographic libraries supported by the client platform.
- No private key material is transmitted off the device at any point during generation.

**Result:** Private keys exist only within the user’s local environment and are never accessible to LigaPay™ backend systems.

---

## 2. Local Key Storage

- Private keys are stored using secure, platform-appropriate storage mechanisms available on the client device.
- LigaPay™ backend services have **no read, write, backup, or recovery access** to locally stored keys.
- Key material is never logged, cached, mirrored, or transmitted to server infrastructure.

Private keys remain under the exclusive control of the user.

---

## 3. Transaction Construction

When a user initiates an action (such as sending assets, performing a token swap, or interacting with a decentralized protocol):

1. The client constructs an unsigned transaction locally.
2. Relevant transaction parameters are retrieved from the blockchain network or third-party protocol interfaces as needed.
3. All transaction details are displayed to the user for review.
4. No transaction is finalized without explicit user confirmation.

At this stage, the transaction remains unsigned and cannot be executed.

---

## 3A. Decentralized Exchange (DEX) Routing (When Applicable)

When a user initiates a token swap, LigaPay™ may connect to third-party decentralized exchange (DEX) aggregation protocols to obtain optimized routing data.

In such cases:

- Swap transaction parameters are generated via third-party routing infrastructure.
- The client receives unsigned transaction data for user review.
- All swap details (tokens, amounts, estimated network fees, smart contract addresses, and routing paths) are displayed prior to user confirmation.
- LigaPay™ does not custody assets, act as a counterparty, or perform exchange or brokerage services.
- LigaPay™ backend systems do not access, store, or control private keys or user assets during swap execution.

All swap transactions are executed directly on public blockchain networks at the user’s direction and are signed locally on the user’s device.

---

## 4. Client-Side Signing

- Transactions are signed **locally on the user’s device** using the user’s private key.
- Signing occurs entirely within the client environment.
- LigaPay™ servers do not participate in signing, co-signing, approval, or key management.
- No private key material is transmitted to backend systems during signing.

Only the user can authorize a transaction.

---

## 5. Network Broadcast

- Once signed, the transaction is broadcast to the relevant blockchain network.
- Backend services may assist with network routing or transaction relay functions, but **never with transaction authorization or signing**.
- Backend systems cannot modify, replace, intercept, or re-sign transactions.
- Execution occurs directly on decentralized public blockchain networks.

---

## 6. Backend Role Clarification

LigaPay™ backend infrastructure is limited to:

- Blockchain data retrieval  
- Transaction status tracking  
- User interface support  
- Connectivity to decentralized protocol infrastructure  

Backend systems **cannot**:

- Generate private keys  
- Access private keys  
- Reconstruct seed phrases  
- Sign transactions  
- Move funds  
- Override user intent  
- Act as a transaction counterparty  

The backend operates strictly as a non-custodial support layer.

---

## 7. Security Boundary Summary

| Component | Capability |
|------------|------------|
| Client Device | Key generation, encrypted storage, transaction signing |
| LigaPay™ Backend | Read-only blockchain data access, routing, relay assistance |
| Third-Party Protocols | Direct smart contract interaction with user-signed transactions |

At no point does custody or control of user assets transfer to LigaPay™.

---

## 8. Design Intent

This architecture is intentionally designed to:

- Eliminate custodial risk  
- Ensure private keys remain under exclusive user control  
- Prevent server-side compromise from affecting user assets  
- Maintain strict separation between cryptographic authority and backend services  
- Align with non-custodial best practices  
- Preserve clear regulatory and operational boundaries  

LigaPay™ is designed and operated exclusively as strictly non-custodial blockchain software infrastructure and does not take possession, custody, or control of user digital assets.

