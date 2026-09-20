# Domain assessment

## Svrha

Početni skelet za modele procene, rezultata, žalbe i ručne revizije.

## Sadržaj paketa

- entiteti: procena, rezultat, odluka, žalba
- statusi: `requested`, `in-review`, `manual-review`, `approved`, `rejected`
- validacije: kriterijumi procene, override pravila, signal za žalbu

## Povezani artefakti

- `specs/api/v1/assessment-contract.md`
- `services/assessment-validation-service/`
- `tests/domain/README.md`

## Centralna governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/manual-review-checkpoints.md`, `docs/06-developer/domain-status-and-events-catalog.md`, `docs/06-developer/create-domain-ownership-map.md`, `docs/06-developer/traceability-matrix.md`
- ownership: `docs/06-developer/create-domain-ownership-map.md`
- traceability: `docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: produkt + policy + tehnički vlasnik
- vlasnik isporuke: tehnički vlasnik implementacije
- vlasnik kontrole: AI governance vlasnik domena uz policy i audit podršku
- traceability signal: paket pokriva red Procena i validacija i mora ostati usklađen sa manual-review i žalbenim pravilima

## Readiness i release

- paket se otvara zajedno sa ugovornim slojem pre izvršnih servisa i aplikacija
- paket ne uvodi lokalna pravila bez dopune source-of-truth i ownership dokumenata
- završna spremnost proverava se kroz `docs/06-developer/definition-of-ready.md`, `docs/06-developer/definition-of-done.md` i `docs/06-developer/release-gates.md`
