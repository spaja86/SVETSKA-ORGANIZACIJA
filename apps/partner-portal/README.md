# Partner portal

## Svrha

Partnerski portal za procenu, potvrdu rezultata, upravljanje angažmanima i pregled licenci u partner kontekstu.

## Izvorni dokumenti

- `../../docs/03-product/product-requirements.md`
- `../../docs/05-operations/operating-model.md`
- `../../docs/06-developer/mvp-create-implementation-plan.md`

## Minimalni ekrani

- pregled zahteva za procenu i partner zadataka
- potvrda rezultata, žalbi i korekcija
- pregled angažmana, licenci i partner statusa
- signal za ručnu reviziju i regulatorne blokade

## Uloge i događaji

- primarne uloge: partner evaluator, partner administrator
- ključni događaji: `assessment.requested`, `assessment.decision.confirmed`, `partner.engagement.confirmed`

## Centralna governance veza

- centralni ulaz: `../../docs/06-developer/README.md`
- source-of-truth: `../../docs/06-developer/mvp-create-implementation-plan.md`, `../../docs/06-developer/create-domain-ownership-map.md`, `../../docs/06-developer/manual-review-checkpoints.md`
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

- vlasnik odluke: produkt + policy + tehnički vlasnik za procenu, uz operativni + tehnički vlasnik za partner angažmane
- vlasnik isporuke: tehnički vlasnik implementacije
- vlasnik kontrole: AI governance vlasnik domena i operativni kontrolni vlasnik partnera uz audit podršku
- traceability signal: portal pokriva redove Procena i validacija, Licence i Partneri i angažmani iz traceability matrice

## Readiness i release

- zavisni moduli: `../../services/assessment-validation-service/`, `../../services/partner-engagement-service/`, `../../services/license-service/`, `../../packages/domain-assessment/`, `../../packages/domain-partner/`, `../../packages/domain-license/`, `../../specs/api/v1/assessment-contract.md`, `../../specs/api/v1/partner-contract.md`, `../../specs/api/v1/license-contract.md`
- portal se otvara tek nakon potvrđenih ugovora, shared paketa i zavisnih servisa
- završna spremnost proverava se kroz `../../docs/06-developer/definition-of-ready.md`, `../../docs/06-developer/definition-of-done.md` i `../../docs/06-developer/release-gates.md`
