# Audit Log Specification (Demo)

## Logged fields (always)
| Field | Example (masked) | Notes |
|-------|------------------|-------|
| actor_id | `op***07` | Operator, never full name |
| action | `kyc.approve` | Verb + object |
| subject_ref | `sub#8821` | Obfuscated subject id |
| prev_state | `pending` | No PII values |
| new_state | `verified` | No PII values |
| ts_utc | `2026-10-05T09:12:04Z` | UTC only |

## Never logged
- Full name, ID number, biometric vector, source-of-funds text.
- Raw RFID UID (only hashed suffix).

## Retention
- Append-only. 180 days hot storage, then archived (hashed).
- No edit / no delete API exposed to L1/L2.
