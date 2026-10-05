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