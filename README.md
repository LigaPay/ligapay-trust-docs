# LigaPay™ Trust & Transparency Documentation

Public documentation describing the strictly non-custodial architecture of LigaPay™.

These documents are provided to support transparency, security reviews, and regulatory or partner due diligence.

## Core Architecture Documents

### Non-Custodial Guarantee
**[NON_CUSTODIAL_GUARANTEE.md](./NON_CUSTODIAL_GUARANTEE.md)**  
Defines LigaPay™’s non-custodial design commitments and user ownership guarantees.

### Key Generation & Transaction Signing Flow
**[KEY_SIGNING_FLOW.md](./KEY_SIGNING_FLOW.md)**  
Explains client-side key generation, encryption, storage, and local transaction signing.

### Backend Key Access Limitations
**[BACKEND_CANNOT_ACCESS_KEYS.md](./BACKEND_CANNOT_ACCESS_KEYS.md)**  
Explains why LigaPay™ backend systems cannot access, control, reconstruct, or recover user private keys.

## Design Principles

- Client-side cryptography only  
- No server-side private key handling  
- No custodial authority  
- No backend signing capability  
- User-controlled assets at all times
