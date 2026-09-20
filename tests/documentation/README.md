# Documentation tests

## Svrha

Validacija dokumentacije, navigacije, source-of-truth veza i traceability konzistentnosti.

## Fokus

- doslednost README i governance referenci
- poklapanje source-of-truth, ownership i traceability veza
- kontrola da nijedan tehnički sloj ne uvodi paralelna pravila

## Povezani artefakti

- `docs/06-developer/README.md`
- `docs/06-developer/source-of-truth-map.md`
- `docs/06-developer/traceability-matrix.md`

## Centralna governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/source-of-truth-map.md`, `docs/06-developer/release-gates.md`, `docs/06-developer/traceability-matrix.md`
- ownership: `docs/06-developer/create-domain-ownership-map.md`
- traceability: `docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: vlasnici odluke pogođenih governance dokumenata
- vlasnik isporuke: tehnički vlasnik isporuke dokumentacionog sloja
- vlasnik kontrole: najstroži relevantni vlasnik kontrole iz pogođenih domena
- traceability signal: ovaj sloj proverava repo-wide governance ritam i mora ostati usklađen sa release kontrolama dokumentacionog talasa

## Readiness i release

- test sloj se širi paralelno sa svakim novim ugovorom, statusom, događajem i kontrolom
- ovaj README ne uvodi lokalna pravila mimo source-of-truth i release dokumentacije
- završna spremnost proverava se kroz `docs/06-developer/definition-of-ready.md`, `docs/06-developer/definition-of-done.md` i `docs/06-developer/release-gates.md`
