# Shared statuses

## Svrha

Deljeni skelet za zajedničke statuse, razloge promene i pravila prelaza između domena.

## Sadržaj paketa

- zajednički statusni tipovi i razlozi
- pravila prelaza koja povezuju više create domena
- usaglašavanje događaja koji zavise od statusnih promena

## Povezani artefakti

- `packages/domain-profile/`
- `packages/domain-assessment/`
- `packages/domain-license/`
- `specs/api/v1/README.md`

## Centralna governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/domain-status-and-events-catalog.md`, `docs/06-developer/create-domain-ownership-map.md`, `docs/06-developer/traceability-matrix.md`
- ownership: `docs/06-developer/create-domain-ownership-map.md`
- traceability: `docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: vlasnici odluke svih pogođenih domena
- vlasnik isporuke: tehnički vlasnik implementacije shared sloja
- vlasnik kontrole: najstroži relevantni vlasnik kontrole iz pogođenih domena
- traceability signal: paket pokriva višedomenski red Deljeni statusi i validacije i ne sme postati lokalni izvor istine

## Readiness i release

- paket se otvara zajedno sa ugovornim slojem pre izvršnih servisa i aplikacija
- paket ne uvodi lokalna pravila bez dopune source-of-truth i ownership dokumenata
- završna spremnost proverava se kroz `docs/06-developer/definition-of-ready.md`, `docs/06-developer/definition-of-done.md` i `docs/06-developer/release-gates.md`
