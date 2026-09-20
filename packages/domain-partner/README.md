# Domain partner

## Svrha

Početni skelet za modele partnera, angažmana i potvrda.

## Sadržaj paketa

- entiteti: partner, angažman, potvrda učinka
- statusi: `draft`, `pending-approval`, `active`, `suspended`, `closed`
- validacije: partner prava, potvrda angažmana, sporni slučaj

## Povezani artefakti

- `specs/api/v1/partner-contract.md`
- `services/partner-engagement-service/`
- `docs/06-developer/role-permission-model.md`
- `tests/contract/README.md`
- `tests/integration/README.md`

## Centralna governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/external-integration-map.md`, `docs/06-developer/create-domain-ownership-map.md`, `docs/06-developer/traceability-matrix.md`
- ownership: `docs/06-developer/create-domain-ownership-map.md`
- traceability: `docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: operativni + tehnički vlasnik
- vlasnik isporuke: tehnički vlasnik implementacije
- vlasnik kontrole: operativni kontrolni vlasnik partnera uz audit i policy podršku
- traceability signal: paket pokriva red Partneri i angažmani i mora zadržati partner ownership granice

## Readiness i release

- paket se otvara zajedno sa ugovornim slojem pre izvršnih servisa i aplikacija
- paket ne uvodi lokalna pravila bez dopune source-of-truth i ownership dokumenata
- završna spremnost proverava se kroz `docs/06-developer/definition-of-ready.md`, `docs/06-developer/definition-of-done.md` i `docs/06-developer/release-gates.md`
