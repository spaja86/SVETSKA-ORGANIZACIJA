# Audit reporting service

## Svrha

Servis za audit događaje, korelaciju, KPI agregaciju i incidentne operativne signale.

## Ulazi i izlazi

- ulazi: događaji iz create servisa, korelacioni ID-jevi, KPI signal
- izlazi: audit trag, KPI agregat, signal neuspele korelacije ili incidenta

## Granice odgovornosti

- upravlja audit tragom i KPI izlazima
- ne menja domenske odluke drugih servisa
- ne redefiniše event naming i data handling bez centralne promene

## Povezani artefakti

- `../../specs/api/v1/audit-event-contract.md`
- `../../packages/domain-audit/`
- `../../docs/06-developer/event-naming-standard.md`
- `../../tests/audit/README.md`

## Centralna governance veza

- centralni ulaz: `../../docs/06-developer/README.md`
- source-of-truth: `../../docs/06-developer/observability-plan.md`, `../../docs/06-developer/event-naming-standard.md`, `../../docs/06-developer/traceability-matrix.md`
- ownership: `../../docs/06-developer/create-domain-ownership-map.md`
- traceability: `../../docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: operativni + policy + tehnički vlasnik
- vlasnik isporuke: tehnički vlasnik implementacije
- vlasnik kontrole: observability vlasnik domena uz audit i policy podršku
- traceability signal: servis pokriva red Audit i KPI i mora da održi neizmenjiv trag i KPI signal za celo create jezgro

## Readiness i release

- servis se otvara tek nakon potvrđenih ugovora i shared paketa
- servis mora dokumentovati audit, data-handling i manual-review posledice kada su relevantne
- završna spremnost proverava se kroz `../../docs/06-developer/definition-of-ready.md`, `../../docs/06-developer/definition-of-done.md` i `../../docs/06-developer/release-gates.md`
