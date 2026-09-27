# Regulatory rules service

## Svrha

Servis za lokalna pravila, blokade, izuzetke i mapiranje jurisdikcija.

## Ulazi i izlazi

- ulazi: jurisdikcija, pravilo, izuzetak, zahtev koji može biti blokiran
- izlazi: odluka o blokadi, izuzetak, audit osnov i signal za ručnu intervenciju

## Granice odgovornosti

- upravlja pravilima i izuzecima po jurisdikciji
- ne izdaje licencu niti menja profile samostalno
- ne redefiniše klasifikaciju podataka ili regulatorna pravila bez centralne promene

## Povezani artefakti

- `../../packages/domain-regulatory/`
- `../../docs/06-developer/localization-and-jurisdiction-plan.md`
- `../../docs/06-developer/data-classification-and-handling.md`
- `../../tests/audit/README.md`
- `../../tests/integration/README.md`

## Centralna governance veza

- centralni ulaz: `../../docs/06-developer/README.md`
- source-of-truth: `../../docs/06-developer/localization-and-jurisdiction-plan.md`, `../../docs/06-developer/data-classification-and-handling.md`, `../../docs/06-developer/traceability-matrix.md`
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

- vlasnik odluke: policy + operativni + tehnički vlasnik
- vlasnik isporuke: tehnički vlasnik implementacije
- vlasnik kontrole: regulatorni vlasnik domena uz privatnost i audit podršku
- traceability signal: servis pokriva red Regulatorna pravila i mora pružiti dokumentovan osnov za blokade i izuzetke

## Readiness i release

- servis se otvara tek nakon potvrđenih ugovora i shared paketa
- servis mora dokumentovati audit, data-handling i manual-review posledice kada su relevantne
- završna spremnost proverava se kroz `../../docs/06-developer/definition-of-ready.md`, `../../docs/06-developer/definition-of-done.md` i `../../docs/06-developer/release-gates.md`
