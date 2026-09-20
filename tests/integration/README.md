# Integration tests

## Svrha

Validacija krajnjeg create toka između aplikacija, servisa, shared paketa i ugovora.

## Fokus

- prolaz kroz profil, dokaze, procenu, odluku i licencu
- kontrola korelacije događaja i statusnih promena između slojeva
- regulatorne blokade i partner potvrde u višeslojnom toku

## Povezani artefakti

- `apps/user-portal/README.md`
- `services/README.md`
- `specs/api/v1/README.md`

## Centralna governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/source-of-truth-map.md`, `docs/06-developer/release-gates.md`, `docs/06-developer/traceability-matrix.md`
- ownership: `docs/06-developer/create-domain-ownership-map.md`
- traceability: `docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: vlasnici odluke pogođenih create domena
- vlasnik isporuke: tehnički vlasnik isporuke integracionog sloja
- vlasnik kontrole: najstroži relevantni vlasnik kontrole iz pogođenih domena
- traceability signal: ovaj sloj proverava fazno otvoren create tok preko svih zavisnih modula

## Readiness i release

- test sloj se širi paralelno sa svakim novim ugovorom, statusom, događajem i kontrolom
- ovaj README ne uvodi lokalna pravila mimo source-of-truth i release dokumentacije
- završna spremnost proverava se kroz `docs/06-developer/definition-of-ready.md`, `docs/06-developer/definition-of-done.md` i `docs/06-developer/release-gates.md`
