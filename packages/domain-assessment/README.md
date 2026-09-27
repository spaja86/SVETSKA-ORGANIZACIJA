# Domain assessment

## Svrha

Početni skelet za modele procene, rezultata, žalbe i ručne revizije.

## Sadržaj paketa

- entiteti: procena, rezultat, odluka, žalba
- statusi: `requested`, `in-review`, `manual-review`, `appealed`, `approved`, `rejected`
- validacije: kriterijumi procene, override pravila, signal za žalbu

## Povezani artefakti

- `../../specs/api/v1/assessment-contract.md`
- `../../services/assessment-validation-service/`
- `../../docs/06-developer/manual-review-checkpoints.md`
- `../../tests/domain/README.md`

## Centralna governance veza

- centralni ulaz: `../../docs/06-developer/README.md`
- source-of-truth: `../../docs/06-developer/manual-review-checkpoints.md`, `../../docs/06-developer/domain-status-and-events-catalog.md`, `../../docs/06-developer/create-domain-ownership-map.md`, `../../docs/06-developer/traceability-matrix.md`
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

- vlasnik odluke: produkt + policy + tehnički vlasnik
- vlasnik isporuke: tehnički vlasnik implementacije
- vlasnik kontrole: AI governance vlasnik domena uz policy i audit podršku
- traceability signal: paket pokriva red Procena i validacija i mora ostati usklađen sa manual-review i žalbenim pravilima

## Readiness i release

- paket se otvara zajedno sa ugovornim slojem pre izvršnih servisa i aplikacija
- paket ne uvodi lokalna pravila bez dopune source-of-truth i ownership dokumenata
- završna spremnost proverava se kroz `../../docs/06-developer/definition-of-ready.md`, `../../docs/06-developer/definition-of-done.md` i `../../docs/06-developer/release-gates.md`
