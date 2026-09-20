# Domain tests

## Svrha

Validacija domenskih pravila, negativnih scenarija i dozvoljenih prelaza statusa po create jezgru.

## Fokus

- pravila profila, dokaza, procene i licenci
- negativni scenariji i zabranjeni prelazi stanja
- manual-review i žalbeni tok kada je relevantan

## Povezani artefakti

- `../../packages/domain-profile/`
- `../../packages/domain-assessment/`
- `../../packages/domain-license/`
- `../../docs/06-developer/domain-status-and-events-catalog.md`

## Centralna governance veza

- centralni ulaz: `../../docs/06-developer/README.md`
- source-of-truth: `../../docs/06-developer/source-of-truth-map.md`, `../../docs/06-developer/release-gates.md`, `../../docs/06-developer/traceability-matrix.md`
- ownership: `../../docs/06-developer/create-domain-ownership-map.md`
- traceability: `../../docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: vlasnici odluke pogođenih create domena
- vlasnik isporuke: tehnički vlasnik isporuke domenskog sloja
- vlasnik kontrole: najstroži relevantni vlasnik kontrole iz pogođenih domena
- traceability signal: ovaj sloj proverava jezgro MVP create toka i mora pratiti centralni statusni jezik

## Readiness i release

- test sloj se širi paralelno sa svakim novim ugovorom, statusom, događajem i kontrolom
- ovaj README ne uvodi lokalna pravila mimo source-of-truth i release dokumentacije
- završna spremnost proverava se kroz `../../docs/06-developer/definition-of-ready.md`, `../../docs/06-developer/definition-of-done.md` i `../../docs/06-developer/release-gates.md`
