# Audit tests

## Svrha

Validacija audit korelacije, KPI signala, regulatornih blokada i manual-review traga.

## Fokus

- kompletiranost audit događaja i korelacije
- KPI signali i neuspele korelacije
- regulatorne blokade, izuzeci i ručna revizija

## Povezani artefakti

- `../../services/audit-reporting-service/`
- `../../services/regulatory-rules-service/`
- `../../docs/06-developer/observability-plan.md`

## Centralna governance veza

- centralni ulaz: `../../docs/06-developer/README.md`
- source-of-truth: `../../docs/06-developer/source-of-truth-map.md`, `../../docs/06-developer/release-gates.md`, `../../docs/06-developer/traceability-matrix.md`
- ownership: `../../docs/06-developer/create-domain-ownership-map.md`
- traceability: `../../docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: vlasnici odluke domena Audit i KPI i Regulatorna pravila
- vlasnik isporuke: tehnički vlasnik isporuke audit sloja
- vlasnik kontrole: observability i regulatorni vlasnik kontrole uz audit podršku
- traceability signal: ovaj sloj proverava neizmenjiv trag odluke i kontrolni signal za osetljive tokove

## Readiness i release

- test sloj se širi paralelno sa svakim novim ugovorom, statusom, događajem i kontrolom
- ovaj README ne uvodi lokalna pravila mimo source-of-truth i release dokumentacije
- završna spremnost proverava se kroz `../../docs/06-developer/definition-of-ready.md`, `../../docs/06-developer/definition-of-done.md` i `../../docs/06-developer/release-gates.md`
