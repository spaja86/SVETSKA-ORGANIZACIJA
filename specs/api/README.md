# API specifikacije

Ovde se nalaze verzionisane API specifikacije i ugovori razmene podataka. Repo-wide API governance ostaje u `../../docs/06-developer/`, a ovaj direktorijum služi kao downstream indeks i verzionisani skup ugovora.

## Aktivni skelet

- `v1/` — početni verzionisani ugovori za MVP create tok
- `mvp-create-flow-contracts.md` — pregled minimalnih ugovora i njihovih veza

## Prioritetni ugovori za MVP

- profil korisnika i status profila
- dokaz kompetencije i istorija dokaza
- zahtev za procenu, rezultat i ljudska revizija
- izdavanje licence, status licence i obnova
- partner pristup i potvrda angažmana
- audit događaj i KPI ulazi

## Centralna governance veza

- centralni ulaz: `../../docs/06-developer/README.md`
- source-of-truth: `../../docs/06-developer/source-of-truth-map.md`, `../../docs/06-developer/api-contract-governance.md`, `../../docs/06-developer/error-taxonomy.md`, `../../docs/06-developer/domain-status-and-events-catalog.md`, `../../docs/06-developer/program-equivalent-assembly-model.md`
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
- ugovorni sloj je prvi izvršno-prenosivi korak montaže i mora ostati usklađen sa centralnim modelom sklapanja create jezgra

## Izvedeni standardi za svaki ugovor

- pravila u ovom odeljku preuzimaju se iz `../../docs/06-developer/api-contract-governance.md` i prateće governance dokumentacije
- izvorni dokument i povezani domen
- vlasnik odluke, vlasnik isporuke i vlasnik kontrole ili dokaz nasleđenog ownership-a
- identifikatori resursa i pravilo statusa
- validacije, greške i regulatorne blokade
- audit metadata, korelacija i ručna revizija kada je potrebna
- test posledice i povezani slojevi u `../../tests/`

## Pravila verzionisanja

- ugovori se uvode tek kada imaju jasnu vezu sa domenom i izvorom zahteva
- svaka promena ugovora mora navesti posledice za aplikacije, servise, pakete i testove
- nekompatibilne promene zahtevaju novu verziju ugovora i plan prelaza
- regulatorna lokalizacija ne menja globalni osnovni ugovor bez eksplicitne odluke

## Readiness i release

- `../../specs/api/` se otvara pre `../../services/` i `../../apps/` sloja
- ugovor ne prelazi dalje dok nije povezan sa source-of-truth, ownership i traceability dokumentima
- završna spremnost ugovora proverava se kroz `../../docs/06-developer/definition-of-ready.md`, `../../docs/06-developer/definition-of-done.md` i `../../docs/06-developer/release-gates.md`
