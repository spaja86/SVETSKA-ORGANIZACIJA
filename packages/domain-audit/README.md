# Domain audit

## Svrha

Početni skelet za audit događaje, korelaciju i KPI modele.

## Sadržaj paketa

- entiteti: audit događaj, korelacioni trag, KPI agregat
- statusi: `captured`, `correlated`, `flagged`, `closed`
- validacije: neizmenjivost, kompletiranost korelacije, KPI signal

## Povezani artefakti

- `specs/api/v1/audit-event-contract.md`
- `services/audit-reporting-service/`
- `tests/audit/README.md`

## Centralna governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/observability-plan.md`, `docs/06-developer/event-naming-standard.md`, `docs/06-developer/traceability-matrix.md`
- ownership: `docs/06-developer/create-domain-ownership-map.md`
- traceability: `docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: operativni + policy + tehnički vlasnik
- vlasnik isporuke: tehnički vlasnik implementacije
- vlasnik kontrole: observability vlasnik domena uz audit i policy podršku
- traceability signal: paket pokriva red Audit i KPI i mora ostati usklađen sa audit tragom i KPI signalom

## Readiness i release

- paket se otvara zajedno sa ugovornim slojem pre izvršnih servisa i aplikacija
- paket ne uvodi lokalna pravila bez dopune source-of-truth i ownership dokumenata
- završna spremnost proverava se kroz `docs/06-developer/definition-of-ready.md`, `docs/06-developer/definition-of-done.md` i `docs/06-developer/release-gates.md`
