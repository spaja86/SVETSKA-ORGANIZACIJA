# Servisi

Ovde se nalaze planirane servisne granice, integracioni slojevi i kontrolni servisi.

## Aktivni skelet

- `profile-identity-service/` — profil, identitet i dokazi
- `assessment-validation-service/` — procena, rezultat i ljudska revizija
- `license-service/` — izdavanje, status i obnova licence
- `partner-engagement-service/` — partneri, angažmani i potvrde
- `audit-reporting-service/` — audit događaji, korelacija i KPI ulazi
- `regulatory-rules-service/` — lokalna pravila, blokade i izuzeci

## Centralna governance veza

- centralni ulaz: `../docs/06-developer/README.md`
- source-of-truth: `../docs/06-developer/source-of-truth-map.md`, `../docs/06-developer/module-readiness-overview.md`, `../docs/06-developer/domain-status-and-events-catalog.md`
- ownership: `../docs/06-developer/create-domain-ownership-map.md`
- traceability: `../docs/06-developer/traceability-matrix.md`

## Pravilo granica

- servisi nose izvršavanje domena i integracija, ali ne redefinišu deljene modele van `../packages/`
- svaki servis mora imati eksplicitne ulaze, izlaze, statuse, ownership i audit događaje
- regulatorna pravila i kontrole pristupa moraju biti ugrađeni u dizajn servisa od početka
- ownership granice, source-of-truth i release kontrole vode se kroz `../docs/06-developer/README.md`

## Ownership i kontrola

- vlasnici odluke: odgovarajući domenski vlasnici iz `../docs/06-developer/create-domain-ownership-map.md`
- vlasnik isporuke: tehnički vlasnik implementacije servisa
- vlasnik kontrole: domenom određeni kontrolni vlasnik sa najstrožim relevantnim pravilima
- traceability signal: svaki servis mora odražavati relevantne redove iz `../docs/06-developer/traceability-matrix.md`

## Readiness i release

- `../services/` se otvara tek nakon potvrđenih `../specs/api/` i `../packages/` artefakata
- svaki servis mora pokazati data-handling, audit i manual-review posledice kada ih domen zahteva
- završna spremnost servisa proverava se kroz `../docs/06-developer/definition-of-ready.md`, `../docs/06-developer/definition-of-done.md` i `../docs/06-developer/release-gates.md`
