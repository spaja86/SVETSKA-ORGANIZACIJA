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

- `packages/domain-regulatory/`
- `tests/audit/README.md`
- `tests/integration/README.md`

## Centralna governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/localization-and-jurisdiction-plan.md`, `docs/06-developer/data-classification-and-handling.md`, `docs/06-developer/traceability-matrix.md`
- ownership: `docs/06-developer/create-domain-ownership-map.md`
- traceability: `docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: policy + operativni + tehnički vlasnik
- vlasnik isporuke: tehnički vlasnik implementacije
- vlasnik kontrole: regulatorni vlasnik domena uz privatnost i audit podršku
- traceability signal: servis pokriva red Regulatorna pravila i mora pružiti dokumentovan osnov za blokade i izuzetke

## Readiness i release

- servis se otvara tek nakon potvrđenih ugovora i shared paketa
- servis mora dokumentovati audit, data-handling i manual-review posledice kada su relevantne
- završna spremnost proverava se kroz `docs/06-developer/definition-of-ready.md`, `docs/06-developer/definition-of-done.md` i `docs/06-developer/release-gates.md`
