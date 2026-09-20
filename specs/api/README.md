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
- source-of-truth: `../../docs/06-developer/source-of-truth-map.md`, `../../docs/06-developer/api-contract-governance.md`, `../../docs/06-developer/error-taxonomy.md`, `../../docs/06-developer/domain-status-and-events-catalog.md`
- ownership: `../../docs/06-developer/create-domain-ownership-map.md`
- traceability: `../../docs/06-developer/traceability-matrix.md`

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
