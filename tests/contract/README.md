# Contract tests

## Svrha

Validacija API ugovora, kompatibilnosti statusa, grešaka i ownership očekivanja.

## Fokus

- doslednost v1 ugovora
- kompatibilnost sa statusima i događajima
- negativni scenariji za validacije, blokade i dozvole

## Povezani artefakti

- `../../specs/api/README.md`
- `../../specs/api/v1/README.md`
- `../../packages/shared-statuses/`
- `../../packages/shared-validation/`

## Centralna governance veza

- centralni ulaz: `../../docs/06-developer/README.md`
- source-of-truth: `../../docs/06-developer/source-of-truth-map.md`, `../../docs/06-developer/release-gates.md`, `../../docs/06-developer/traceability-matrix.md`
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

- vlasnik odluke: vlasnici odluke pogođenih API domena
- vlasnik isporuke: tehnički vlasnik isporuke ugovornog sloja
- vlasnik kontrole: najstroži relevantni vlasnik kontrole iz pogođenih domena
- traceability signal: ovaj sloj proverava traceability između ugovora, shared paketa i domena pre otvaranja servisa i aplikacija

## Readiness i release

- test sloj se širi paralelno sa svakim novim ugovorom, statusom, događajem i kontrolom
- ovaj README ne uvodi lokalna pravila mimo source-of-truth i release dokumentacije
- završna spremnost proverava se kroz `../../docs/06-developer/definition-of-ready.md`, `../../docs/06-developer/definition-of-done.md` i `../../docs/06-developer/release-gates.md`
