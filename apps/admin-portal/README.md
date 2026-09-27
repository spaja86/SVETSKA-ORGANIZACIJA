# Admin portal

## Svrha

Administrativni portal za audit, KPI, regulatorne blokade, override odluke i operativni nadzor.

## Izvorni dokumenti

- `../../docs/04-policies/legal-and-regulatory-framework.md`
- `../../docs/05-operations/kpi-framework.md`
- `../../docs/06-developer/observability-plan.md`

## Minimalni ekrani

- pregled audit događaja i korelacija
- regulatorne blokade i ručne revizije
- KPI signal i osnovni dashboard za create tok
- pregled izuzetaka, incidenata i neuspelih korelacija

## Uloge i događaji

- primarne uloge: administrator, compliance, operativni nadzor
- ključni događaji: `audit.trace.correlated`, `audit.exception.flagged`, `jurisdiction.blocked`, `assessment.human-review.requested`

## Centralna governance veza

- centralni ulaz: `../../docs/06-developer/README.md`
- source-of-truth: `../../docs/06-developer/observability-plan.md`, `../../docs/06-developer/manual-review-checkpoints.md`, `../../docs/06-developer/create-domain-ownership-map.md`
- ownership: `../../docs/06-developer/create-domain-ownership-map.md`
- traceability: `../../docs/06-developer/traceability-matrix.md`

## Repo-wide radni takt

- obavezni redosled ostaje: zahtev → domen → odluka → ugovor i deljeni modeli → test posledice → audit i usklađenost → implementacija → verifikacija i release odluka
- ovaj artefakt se ne otvara ako prethodni koraci nisu potvrđeni kroz `../../docs/06-developer/README.md`, `../../docs/06-developer/definition-of-ready.md` i `../../docs/06-developer/release-gates.md`
- otvorena pitanja, izuzeci i tehnološke odluke vode se kroz `../../docs/06-developer/decision-backlog.md` i `../../docs/06-developer/adrs/README.md`, ne lokalno

## Kontrolni stubovi

- bezbednost, privatnost i role-based pristup ulaze u dizajn od početka
- audit trag, manual-review signal, regulatorna blokada i korektivni tok moraju biti vidljivi kada su relevantni
- create jezgro `profil → dokazi → procena → odluka → licenca → audit` ima prioritet nad sekundarnim tokovima
- traceability od izvornog zahteva do ugovora, testova i release odluke ostaje obavezna

## Ownership i kontrola

- vlasnik odluke: operativni + policy + tehnički vlasnik za audit i KPI, uz policy + operativni + tehnički vlasnik za regulatorna pravila
- vlasnik isporuke: tehnički vlasnik implementacije
- vlasnik kontrole: observability vlasnik domena i regulatorni vlasnik domena uz audit i privatnost podršku
- traceability signal: portal pokriva redove Procena i validacija, Audit i KPI i Regulatorna pravila iz traceability matrice

## Readiness i release

- zavisni moduli: `../../services/audit-reporting-service/`, `../../services/regulatory-rules-service/`, `../../services/assessment-validation-service/`, `../../packages/domain-audit/`, `../../packages/domain-regulatory/`, `../../specs/api/v1/audit-event-contract.md`, `../../specs/api/v1/assessment-contract.md`
- portal se otvara tek nakon potvrđenih ugovora, shared paketa i zavisnih servisa
- završna spremnost proverava se kroz `../../docs/06-developer/definition-of-ready.md`, `../../docs/06-developer/definition-of-done.md` i `../../docs/06-developer/release-gates.md`
