# Domain regulatory

## Svrha

Početni skelet za modele jurisdikcije, pravila, ograničenja i izuzetaka.

## Sadržaj paketa

- entiteti: jurisdikcija, pravilo, ograničenje, izuzetak
- statusi: `active`, `blocked`, `overridden`, `expired`
- validacije: lokalna primenljivost, osnov blokade, pravilo izuzetka

## Povezani artefakti

- `services/regulatory-rules-service/`
- `docs/06-developer/localization-and-jurisdiction-plan.md`
- `docs/06-developer/data-classification-and-handling.md`
- `tests/audit/README.md`
- `tests/integration/README.md`

## Centralna governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/localization-and-jurisdiction-plan.md`, `docs/06-developer/create-domain-ownership-map.md`, `docs/06-developer/traceability-matrix.md`
- ownership: `docs/06-developer/create-domain-ownership-map.md`
- traceability: `docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: policy + operativni + tehnički vlasnik
- vlasnik isporuke: tehnički vlasnik implementacije
- vlasnik kontrole: regulatorni vlasnik domena uz privatnost i audit podršku
- traceability signal: paket pokriva red Regulatorna pravila i mora zadržati dokumentovan osnov za blokade i izuzetke

## Readiness i release

- paket se otvara zajedno sa ugovornim slojem pre izvršnih servisa i aplikacija
- paket ne uvodi lokalna pravila bez dopune source-of-truth i ownership dokumenata
- završna spremnost proverava se kroz `docs/06-developer/definition-of-ready.md`, `docs/06-developer/definition-of-done.md` i `docs/06-developer/release-gates.md`
