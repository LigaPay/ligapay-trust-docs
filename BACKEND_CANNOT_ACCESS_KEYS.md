# LigaPay™ Backend Key Access Limitations

**Product:** LigaPay™  
**Operating Entity:** Liga Techs, Inc. (doing business as LigaPay™)  
**Last Updated:** January 2026

---

## Purpose

This document explains why LigaPay™ backend systems **cannot access, control, or recover user private keys** under any circumstances. It is intended to clarify architectural boundaries for security, compliance, and risk assessment purposes.

---

## 1. Architectural Separation

LigaPay™ is architected with a strict separation between:
- client-side cryptographic operations, and
- backend infrastructure services.

All private key–related functions occur exclusively on the client device. Backend systems are deliberately excluded from all cryptographic workflows.

---

## 2. No Key Material Transmission

LigaPay™ backend services:
- do not receive private keys,
- do not store encrypted private keys,
- do not receive seed phrases or recovery material,
- do not participate in key generation or reconstruction.

Only public blockchain addresses and non-sensitive metadata are transmitted to backend services.

---

## 3. No Signing Capability

Backend systems:
- do not possess signing libraries configured for user transactions,
- do not hold credentials capable of authorizing blockchain operations,
- cannot initiate or approve asset transfers.

All signing is performed locally by the user.

---

## 4. Infrastructure & Access Controls

LigaPay™ backend environments are configured such that:
- no private key storage paths exist,
- no administrative override can introduce key access,
- no operational process allows manual intervention in user wallets.

This ensures that even privileged backend access cannot compromise user assets.

---

## 5. Failure & Incident Scenarios

In the event of:
- server compromise,
- data breach,
- service outage,
- insider threat,

LigaPay™ backend systems remain incapable of accessing or moving user funds, as no cryptographic authority is present server-side.

---

## 6. Design Intent & Risk Mitigation

This design intentionally:
- removes custodial risk,
- limits blast radius in security incidents,
- prevents backend compromise from affecting user funds,
- maintains clear non-custodial regulatory boundaries.

---

## Conclusion

LigaPay™ backend systems are structurally and operationally incapable of accessing user private keys or controlling user assets. Custody and control remain exclusively with the user at all times.

---
