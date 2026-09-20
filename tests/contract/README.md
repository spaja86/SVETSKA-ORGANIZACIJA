# Contract tests

## Svrha

Validacija API ugovora, kompatibilnosti statusa, grešaka i ownership očekivanja.

## Fokus

- doslednost v1 ugovora
- kompatibilnost sa statusima i događajima
- negativni scenariji za validacije, blokade i dozvole

## Povezani artefakti

- `specs/api/README.md`
- `specs/api/v1/README.md`
- `packages/shared-statuses/`
- `packages/shared-validation/`

## Centralna governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/source-of-truth-map.md`, `docs/06-developer/release-gates.md`, `docs/06-developer/traceability-matrix.md`
- ownership: `docs/06-developer/create-domain-ownership-map.md`
- traceability: `docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: vlasnici odluke pogođenih API domena
- vlasnik isporuke: tehnički vlasnik isporuke ugovornog sloja
- vlasnik kontrole: najstroži relevantni vlasnik kontrole iz pogođenih domena
- traceability signal: ovaj sloj proverava traceability između ugovora, shared paketa i domena pre otvaranja servisa i aplikacija

## Readiness i release

- test sloj se širi paralelno sa svakim novim ugovorom, statusom, događajem i kontrolom
- ovaj README ne uvodi lokalna pravila mimo source-of-truth i release dokumentacije
- završna spremnost proverava se kroz `docs/06-developer/definition-of-ready.md`, `docs/06-developer/definition-of-done.md` i `docs/06-developer/release-gates.md`
