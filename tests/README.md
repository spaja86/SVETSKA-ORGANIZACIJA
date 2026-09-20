# Testovi

Ovde se nalaze test strategija, scenariji validacije, integracioni tokovi i referentni paketi za create tok.

## Aktivni skelet

- `documentation/` — validacija dokumentacije, navigacije i traceability-ja
- `contract/` — ugovorna validacija i kompatibilnost statusa
- `domain/` — domenska pravila i negativni scenariji
- `integration/` — krajnji create tok između aplikacija i servisa
- `audit/` — audit korelacija, KPI signali i regulatorne blokade

## Centralna governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/source-of-truth-map.md`, `docs/06-developer/release-gates.md`, `docs/06-developer/reference-test-packages.md`
- ownership: `docs/06-developer/create-domain-ownership-map.md`
- traceability: `docs/06-developer/traceability-matrix.md`

## Nivoi validacije

- dokumentaciona validacija za konzistentnost zahteva i navigacije
- ugovorna validacija za API specifikacije i statuse
- domenska validacija za pravila profila, procene i licenci
- integraciona validacija za create tok između aplikacija i servisa
- audit validacija za događaje, trag odluke i KPI ulaze

## Pravilo pokrivenosti

- svaki novi ugovor, status ili događaj mora imati test posledicu u odgovarajućem sloju
- negativni scenariji, autorizacija i regulatorne blokade imaju prioritet u ranim talasima
- centralna pravila sledljivosti i release kontrole vode se kroz `docs/06-developer/README.md`
- test sloj pokazuje ownership i audit posledice kroz povezane domene i ugovore

## Ownership i kontrola

- vlasnici odluke: vlasnici domena i ugovora koje test sloj proverava
- vlasnik isporuke: tehnički vlasnik isporuke test sloja
- vlasnik kontrole: najstroži relevantni vlasnik kontrole iz pogođenih domena
- traceability signal: svaki test sloj mora odražavati relevantne redove iz `docs/06-developer/traceability-matrix.md`

## Readiness i release

- `tests/` se šire paralelno sa svakim novim ugovorom, statusom, događajem i kontrolom
- nijedan test README ne uvodi lokalna pravila mimo source-of-truth i traceability dokumentacije
- završna spremnost test sloja proverava se kroz `docs/06-developer/definition-of-ready.md`, `docs/06-developer/definition-of-done.md` i `docs/06-developer/release-gates.md`
