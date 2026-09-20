# API contract governance / Upravljanje API ugovorima

## Svrha

Ovaj dokument zaključava repo-wide pravila za API resurse, operacije, interoperabilnost i odnos između governance sloja i `specs/api/` artefakata.

## Centralna pravila

- `docs/06-developer/` zadržava source-of-truth za značenje API sloja; `specs/api/` prikazuje i verzioniše ugovore, ali ne postaje primarni vlasnik centralnih pravila
- svaki API resurs i operacija moraju imati vezu sa izvornim zahtevom, ownership-om, statusnim jezikom, greškama, audit posledicama i test slojevima
- `specs/api/README.md` i `specs/api/v1/*.md` ostaju downstream artefakti usklađeni sa ovim dokumentom, `source-of-truth-map.md`, `error-taxonomy.md` i `traceability-matrix.md`
- nekompatibilne promene zahtevaju novu verziju ugovora i plan prelaza pre otvaranja servisnog ili aplikativnog sloja

## Minimalni elementi svakog ugovora

- resurs, operacija i opseg upotrebe
- statusi, događaji i razlozi kada su relevantni
- validacije, greške i regulatorne blokade
- ownership signal i kontrolne tačke pristupa
- audit metadata, korelacija i manual-review posledice kada su relevantne
- traceability veza ka test slojevima i release kontroli

## Pravilo održavanja

- prvo se menja ovaj dokument ili drugi odgovarajući governance artefakt u `docs/06-developer/`, zatim `specs/api/` izvedeni sadržaj
- kada se uvede nova API oblast, mora biti dodata u `traceability-matrix.md` i usklađena sa `create-domain-ownership-map.md`
- `specs/api/` ne uvodi samostalna release, ownership ili status pravila van ovde zaključenih smernica
