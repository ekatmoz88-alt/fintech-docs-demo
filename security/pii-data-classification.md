# PII Data Classification (Demo)
## Level 1 (Public)
- Public wallet address (displayed on screen)

## Level 2 (Internal)
- Operator ID, Session ID

## Level 3 (Restricted PII)
- User Full Name, Scan of ID doc (masked in UI: **F*** **Name**)
- Source of funds details

## Rules
- Do not log Level 3 data in plain text.
- Auto-mask PII in operator ARM console screens.
## PII Handling Matrix (Demo)

| Data Element | Class | Where shown | Masking rule | Who can view full value |
|--------------|-------|-------------|--------------|--------------------------|
| Wallet alias | Public | All screens | None | Anyone (UI only) |
| Operator ID | Internal | Audit log | Last 2 chars: `op***07` | L2 + Auditor |
| Full name | PII-2 | KYC review | `F*** N***` | L2 only |
| ID document number | PII-2 | KYC review | `**** **** 1234` | L2 only, never in logs |
| Biometric vector | PII-3 | Manual review modal | Never rendered as text | L2 + secure enclave |
| Source-of-funds note | PII-3 | Escalation view | Redacted by default | L2 + Compliance |

### Retention rules (demo)
- PII-2: retained 30 days post-decision, then hashed.
- PII-3: never stored at rest in the operator console.
- Audit log: append-only, PII never written in plain text.