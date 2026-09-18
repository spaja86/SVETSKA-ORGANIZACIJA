# API v1

Početna verzija MVP create ugovora ostaje minimalna, stabilna i povezana sa traceability matricom.

## Ugovori

- `profile-contract.md`
- `evidence-contract.md`
- `assessment-contract.md`
- `license-contract.md`
- `partner-contract.md`
- `audit-event-contract.md`

## Zajednički standardi v1

- svi resursi imaju jedinstveni identifikator i status ili razlog kada status nije primenljiv
- greške koriste klase iz `docs/06-developer/error-taxonomy.md`
- audit događaji koriste standard iz `docs/06-developer/event-naming-standard.md`
- osetljivi tokovi navode ručnu reviziju kada postoji visoki rizik ili regulatorna blokada
- test posledice moraju upućivati na `tests/contract/`, `tests/domain/`, `tests/integration/` ili `tests/audit/`
