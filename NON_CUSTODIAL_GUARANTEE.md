# LigaPay™ Non-Custodial Guarantee

**Product:** LigaPay™  
**Operating Entity:** Liga Techs, Inc. (doing business as LigaPay™)  
**Last Updated:** January 2026

---

## 1. Statement of Non-Custodial Design

LigaPay™ is designed and operated as a **strictly non-custodial** digital wallet and Web3 interface.

At no point does LigaPay™:
- custody user funds,
- control user private keys,
- have unilateral signing authority over user transactions, or
- possess the ability to move user assets.

All cryptographic keys remain under the exclusive control of the user.

---

## 2. Private Key Ownership & Control

- Private keys are generated **client-side** on the user’s device.
- Private keys are never transmitted to, stored by, or accessible to LigaPay™ servers.
- LigaPay™ infrastructure cannot reconstruct, access, or derive user private keys.

Users retain full ownership and responsibility for their cryptographic credentials.

---

## 3. Transaction Authorization Model

All blockchain transactions initiated through LigaPay™:
- are created and signed locally by the user,
- require explicit user authorization, and
- are broadcast to the network without server-side key involvement.

LigaPay™ does not act as a transaction signer, co-signer, or intermediary custodian.

---

## 4. Backend & Infrastructure Limitations

LigaPay™ backend services are architecturally restricted to:
- transaction routing,
- blockchain data indexing,
- balance visualization,
- decentralized protocol interfacing.

Backend systems **cannot**:
- sign transactions,
- initiate asset transfers,
- override user intent, or
- access cryptographic secrets.

---

## 5. Third-Party Protocol Interactions

When users interact with decentralized exchanges, token swap protocols, or other Web3 services via LigaPay™:
- interactions occur directly between the user wallet and the protocol,
- LigaPay™ functions solely as a user interface and transaction facilitator,
- custody remains entirely with the user at all times.

---

## 6. Regulatory & Risk Disclosure

LigaPay™ does not qualify as:
- a custodian,
- a money transmitter holding customer funds,
- a broker-dealer,
- or a financial institution holding user assets.

Users assume responsibility for:
- safeguarding their private keys,
- transaction verification,
- compliance with applicable laws in their jurisdiction.

---

## 7. Transparency Commitment

LigaPay™ is committed to transparency by:
- publishing architectural documentation,
- clearly describing key ownership boundaries,
- avoiding opaque custody models,
- maintaining a verifiable non-custodial posture.

Additional technical documentation is provided in this repository.

---

## 8. No Implied Custody

Nothing in LigaPay™’s design, documentation, or operation should be interpreted as implying custody, control, or possession of user assets by LigaPay™ or its operators.

---
