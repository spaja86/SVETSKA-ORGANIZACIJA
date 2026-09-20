# API v1

Početna verzija MVP create ugovora ostaje minimalna, stabilna i povezana sa traceability matricom.

## Ugovori

- `profile-contract.md`
- `evidence-contract.md`
- `assessment-contract.md`
- `license-contract.md`
- `partner-contract.md`
- `audit-event-contract.md`

## Centralna governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/source-of-truth-map.md`, `docs/06-developer/error-taxonomy.md`, `docs/06-developer/event-naming-standard.md`
- ownership: `docs/06-developer/create-domain-ownership-map.md`
- traceability: `docs/06-developer/traceability-matrix.md`

## Zajednički standardi v1

- svi resursi imaju jedinstveni identifikator i status ili razlog kada status nije primenljiv
- greške koriste klase iz `docs/06-developer/error-taxonomy.md`
- audit događaji koriste standard iz `docs/06-developer/event-naming-standard.md`
- osetljivi tokovi navode ručnu reviziju kada postoji visoki rizik ili regulatorna blokada
- test posledice moraju upućivati na `tests/contract/`, `tests/domain/`, `tests/integration/` ili `tests/audit/`

## Readiness i release

- v1 ugovori ne uvode lokalne varijante statusa, događaja, grešaka ili ownership-a
- svaka promena v1 ugovora mora pokazati posledice po pakete, servise, aplikacije i testove
- završna spremnost v1 sloja proverava se kroz `docs/06-developer/definition-of-ready.md`, `docs/06-developer/definition-of-done.md` i `docs/06-developer/release-gates.md`
