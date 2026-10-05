# Fintech Docs Demo
Technical Writing portfolio piece. 
Documentation structure for a fictional crypto-onramp operator console.

## Scope
- **ARM Console:** L1/L2 operator UX flows (`/arm`)
- **User Flows:** Crypto onramp scenario (`/flows`)
- **Security:** PII classification, RFID threat matrix (`/security`)
## Diagrams
- [`diagrams/flow-kyc-onramp.txt`](diagrams/flow-kyc-onramp.txt) — ASCII flow: KYC → L1/L2 → QR token

`security/audit-log-spec.md` 
  append-only audit log schema
  
## Structure (final)
- `arm/` — operator console UX (L1/L2)
- `flows/` — crypto onramp scenario
- `security/` — PII classification 
 leak prevention · RFID threats · audit-log spec
- `diagrams/` — ASCII KYC→onramp flow
*Demo-only. No real data included.*