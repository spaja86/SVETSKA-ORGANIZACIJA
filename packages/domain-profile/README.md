# Domain profile

## Svrha

Početni skelet za modele profila, identiteta i dokaza.

## Sadržaj paketa

- entiteti: profil, identitet, dokaz
- statusi: `draft`, `active`, `pending-review`, `suspended`, `archived`
- validacije: obavezna polja, poreklo dokaza, veza sa korisnikom

## Povezani artefakti

- `specs/api/v1/profile-contract.md`
- `specs/api/v1/evidence-contract.md`
- `services/profile-identity-service/`
- `tests/domain/README.md`

## Centralna governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/domain-status-and-events-catalog.md`, `docs/06-developer/create-domain-ownership-map.md`, `docs/06-developer/traceability-matrix.md`
- ownership: `docs/06-developer/create-domain-ownership-map.md`
- traceability: `docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: produkt + tehnički vlasnik domena
- vlasnik isporuke: tehnički vlasnik implementacije
- vlasnik kontrole: bezbednosni vlasnik domena uz privatnost i audit podršku
- traceability signal: paket pokriva red Identitet i profil i ne uvodi lokalne varijante statusa ili validacija

## Readiness i release

- paket se otvara zajedno sa ugovornim slojem pre izvršnih servisa i aplikacija
- paket ne uvodi lokalna pravila bez dopune source-of-truth i ownership dokumenata
- završna spremnost proverava se kroz `docs/06-developer/definition-of-ready.md`, `docs/06-developer/definition-of-done.md` i `docs/06-developer/release-gates.md`
