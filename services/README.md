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
- source-of-truth: `../docs/06-developer/source-of-truth-map.md`, `../docs/06-developer/module-readiness-overview.md`, `../docs/06-developer/domain-status-and-events-catalog.md`, `../docs/06-developer/program-equivalent-assembly-model.md`
- ownership: `../docs/06-developer/create-domain-ownership-map.md`
- traceability: `../docs/06-developer/traceability-matrix.md`

## Pravilo granica

- servisi nose izvršavanje domena i integracija, ali ne redefinišu deljene modele van `../packages/`
- svaki servis mora imati eksplicitne ulaze, izlaze, statuse, ownership i audit događaje
- regulatorna pravila i kontrole pristupa moraju biti ugrađeni u dizajn servisa od početka
- ownership granice, source-of-truth i release kontrole vode se kroz `../docs/06-developer/README.md`

## Repo-wide radni takt

- obavezni redosled ostaje: zahtev → domen → odluka → ugovor i deljeni modeli → test posledice → audit i usklađenost → implementacija → verifikacija i release odluka
- ovaj artefakt se ne otvara ako prethodni koraci nisu potvrđeni kroz `../docs/06-developer/README.md`, `../docs/06-developer/definition-of-ready.md` i `../docs/06-developer/release-gates.md`
- otvorena pitanja, izuzeci i tehnološke odluke vode se kroz `../docs/06-developer/decision-backlog.md` i `../docs/06-developer/adrs/README.md`, ne lokalno

## Kontrolni stubovi

- bezbednost, privatnost i role-based pristup ulaze u dizajn od početka
- audit trag, manual-review signal, regulatorna blokada i korektivni tok moraju biti vidljivi kada su relevantni
- create jezgro `profil → dokazi → procena → odluka → licenca → audit` ima prioritet nad sekundarnim tokovima
- traceability od izvornog zahteva do ugovora, testova i release odluke ostaje obavezna
- servisni sloj se sklapa tek nakon potvrđenog ugovornog i shared sloja za ciljni create korak

## Ownership i kontrola

- vlasnici odluke: odgovarajući domenski vlasnici iz `../docs/06-developer/create-domain-ownership-map.md`
- vlasnik isporuke: tehnički vlasnik implementacije servisa
- vlasnik kontrole: domenom određeni kontrolni vlasnik sa najstrožim relevantnim pravilima
- traceability signal: svaki servis mora odražavati relevantne redove iz `../docs/06-developer/traceability-matrix.md`

## Readiness i release

- `../services/` se otvara tek nakon potvrđenih `../specs/api/` i `../packages/` artefakata
- svaki servis mora pokazati data-handling, audit i manual-review posledice kada ih domen zahteva
- završna spremnost servisa proverava se kroz `../docs/06-developer/definition-of-ready.md`, `../docs/06-developer/definition-of-done.md` i `../docs/06-developer/release-gates.md`
