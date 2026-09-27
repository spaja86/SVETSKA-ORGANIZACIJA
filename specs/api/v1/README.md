# API v1

Početna verzija MVP create ugovora ostaje minimalna, stabilna i povezana sa traceability matricom.

## Ugovori

- `profile-contract.md`
- `evidence-contract.md`
- `assessment-contract.md`
- `license-contract.md`
- `partner-contract.md`
- `audit-event-contract.md`

## Centralna governance veza

- centralni ulaz: `../../../docs/06-developer/README.md`
- source-of-truth: `../../../docs/06-developer/source-of-truth-map.md`, `../../../docs/06-developer/api-contract-governance.md`, `../../../docs/06-developer/error-taxonomy.md`, `../../../docs/06-developer/event-naming-standard.md`, `../../../docs/06-developer/program-equivalent-assembly-model.md`
- ownership: `../../../docs/06-developer/create-domain-ownership-map.md`
- traceability: `../../../docs/06-developer/traceability-matrix.md`

## Repo-wide radni takt

- obavezni redosled ostaje: zahtev → domen → odluka → ugovor i deljeni modeli → test posledice → audit i usklađenost → implementacija → verifikacija i release odluka
- ovaj artefakt se ne otvara ako prethodni koraci nisu potvrđeni kroz `../../../docs/06-developer/README.md`, `../../../docs/06-developer/definition-of-ready.md` i `../../../docs/06-developer/release-gates.md`
- otvorena pitanja, izuzeci i tehnološke odluke vode se kroz `../../../docs/06-developer/decision-backlog.md` i `../../../docs/06-developer/adrs/README.md`, ne lokalno

## Kontrolni stubovi

- bezbednost, privatnost i role-based pristup ulaze u dizajn od početka
- audit trag, manual-review signal, regulatorna blokada i korektivni tok moraju biti vidljivi kada su relevantni
- create jezgro `profil → dokazi → procena → odluka → licenca → audit` ima prioritet nad sekundarnim tokovima
- traceability od izvornog zahteva do ugovora, testova i release odluke ostaje obavezna
- v1 ugovori predstavljaju prvi konkretan izvršno-prenosivi sloj programa i moraju ostati u skladu sa centralnim modelom montaže create jezgra

## Zajednički standardi v1

- svi resursi imaju jedinstveni identifikator i status ili razlog kada status nije primenljiv
- greške koriste klase iz `../../../docs/06-developer/error-taxonomy.md`
- audit događaji koriste standard iz `../../../docs/06-developer/event-naming-standard.md`
- osetljivi tokovi navode ručnu reviziju kada postoji visoki rizik ili regulatorna blokada
- test posledice moraju upućivati na `../../../tests/contract/`, `../../../tests/domain/`, `../../../tests/integration/` ili `../../../tests/audit/`

## Readiness i release

- v1 ugovori ne uvode lokalne varijante statusa, događaja, grešaka ili ownership-a
- svaka promena v1 ugovora mora pokazati posledice po pakete, servise, aplikacije i testove
- završna spremnost v1 sloja proverava se kroz `../../../docs/06-developer/definition-of-ready.md`, `../../../docs/06-developer/definition-of-done.md` i `../../../docs/06-developer/release-gates.md`
