# Shared validation

## Svrha

Deljeni skelet za validaciona pravila, greške i kontrolne klase koje koristi više domena.

## Sadržaj paketa

- zajedničke validacije obaveznih polja i korelacionih pravila
- klase grešaka i razlog odbijanja
- kontrolna pravila za regulatorne i pristupne blokade

## Povezani artefakti

- `packages/shared-statuses/`
- `specs/api/README.md`
- `tests/contract/README.md`

## Centralna governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/error-taxonomy.md`, `docs/06-developer/create-domain-ownership-map.md`, `docs/06-developer/traceability-matrix.md`
- ownership: `docs/06-developer/create-domain-ownership-map.md`
- traceability: `docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: vlasnici odluke svih pogođenih domena
- vlasnik isporuke: tehnički vlasnik implementacije shared sloja
- vlasnik kontrole: najstroži relevantni vlasnik kontrole iz pogođenih domena
- traceability signal: paket pokriva višedomenski red Deljeni statusi i validacije i mora ostati usklađen sa centralnom taksonomijom grešaka

## Readiness i release

- paket se otvara zajedno sa ugovornim slojem pre izvršnih servisa i aplikacija
- paket ne uvodi lokalna pravila bez dopune source-of-truth i ownership dokumenata
- završna spremnost proverava se kroz `docs/06-developer/definition-of-ready.md`, `docs/06-developer/definition-of-done.md` i `docs/06-developer/release-gates.md`
