# Domain license

## Svrha

Početni skelet za modele licenci, statusa, obnove i suspenzije.

## Sadržaj paketa

- entiteti: licenca, obnova, suspenzija, istorija statusa
- statusi: `pending`, `active`, `renewal-due`, `expired`, `suspended`, `revoked`
- validacije: uslovi izdavanja, obnova, zabrana nevažećih prelaza

## Povezani artefakti

- `../../specs/api/v1/license-contract.md`
- `../../services/license-service/`
- `../../tests/domain/README.md`
- `../../tests/audit/README.md`

## Centralna governance veza

- centralni ulaz: `../../docs/06-developer/README.md`
- source-of-truth: `../../docs/06-developer/domain-status-and-events-catalog.md`, `../../docs/06-developer/error-taxonomy.md`, `../../docs/06-developer/create-domain-ownership-map.md`, `../../docs/06-developer/traceability-matrix.md`
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
- vlasnik kontrole: policy vlasnik licence uz audit i regulatornu podršku
- traceability signal: paket pokriva red Licence i mora koristiti centralni statusni jezik i greške

## Readiness i release

- paket se otvara zajedno sa ugovornim slojem pre izvršnih servisa i aplikacija
- paket ne uvodi lokalna pravila bez dopune source-of-truth i ownership dokumenata
- završna spremnost proverava se kroz `../../docs/06-developer/definition-of-ready.md`, `../../docs/06-developer/definition-of-done.md` i `../../docs/06-developer/release-gates.md`
