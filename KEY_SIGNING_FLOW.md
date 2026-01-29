# LigaPay™ Key Generation & Signing Flow

**Product:** LigaPay™  
**Operating Entity:** Liga Techs, Inc. (doing business as LigaPay™)  
**Last Updated:** January 2026

---

## Overview

This document describes the high-level key generation and transaction signing flow used by LigaPay™.  
The purpose is to clearly demonstrate that **all cryptographic operations occur client-side**, and that LigaPay™ backend systems **never access or control private keys**.

---

## 1. Client-Side Key Generation

- Cryptographic key pairs are generated **locally on the user’s device**.
- Key generation uses industry-standard cryptographic libraries supported by the client platform.
- No private key material is transmitted off the device at any point during generation.

**Result:** Private keys exist only within the user’s local environment.

---

## 2. Local Key Storage

- Private keys are stored using secure, platform-appropriate storage mechanisms available on the client device.
- LigaPay™ backend services have **no read, write, or recovery access** to locally stored keys.
- Key material is never logged, cached, or mirrored by server infrastructure.

---

## 3. Transaction Construction

When a user initiates an action (send, swap, interact with a protocol):

1. The client constructs an unsigned transaction locally.
2. Transaction parameters are displayed to the user for review.
3. No transaction is finalized without explicit user confirmation.

---

## 4. Client-Side Signing

- Transactions are signed **locally** using the user’s private key.
- Signing occurs entirely within the client environment.
- LigaPay™ servers do not participate in signing, co-signing, or approval.

---

## 5. Network Broadcast

- Once signed, the transaction is broadcast to the relevant blockchain network.
- Backend services may assist with routing or relaying, but **never with authorization**.
- The backend cannot modify, replace, or re-sign transactions.

---

## 6. Backend Role Clarification

LigaPay™ backend infrastructure is limited to:
- blockchain data retrieval,
- transaction status tracking,
- user interface support,
- decentralized protocol connectivity.

Backend systems **cannot**:
- generate keys,
- sign transactions,
- move funds,
- override user intent.

---

## 7. Security Boundary Summary

| Component | Capability |
|---------|------------|
| Client Device | Key generation, storage, signing |
| LigaPay™ Backend | Read-only data access, routing |
| Third-Party Protocols | Direct interaction with user wallet |

At no point does custody or control of user assets leave the user.

---

## 8. Design Intent

This architecture is intentionally designed to:
- eliminate custodial risk,
- prevent server-side compromise from affecting user funds,
- align with non-custodial best practices,
- maintain clear regulatory boundaries.

---
