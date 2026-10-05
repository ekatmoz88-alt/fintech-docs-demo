## RFID Threat & Control Matrix (Demo)

| # | Threat | Attack vector | Likelihood | Control | Operator action |
|---|--------|---------------|------------|---------|-----------------|
| T-01 | UID skimming | Proximity reader (<5cm) | Medium | Distance limiter + rate cap | Flag if 2 reads <1s |
| T-02 | UID cloning | Dumped UID replay | Medium | One-time dynamic code per session | Block card, escalate L2 |
| T-03 | Relay attack | Extended-range relay | Low | Challenge-response token | Force re-auth |
| T-04 | Holder substitution | Photo vs live face | Low/Med | 2FA + liveness check | Manual L2 review |
| T-05 | Log leakage | UID in audit export | Low | UID hashed in all logs | Export blocked if raw UID present |

### Operator UX notes (for TW)
- Never display full UID on L1 screen → show `UID: ****A3F1`.
- "Suspicious read" badge appears in red; L1 cannot dismiss it.
- Glossary entry: **Dynamic UID** = single-use session identifier.
