# Testovi

Ovde se nalaze test strategija, scenariji validacije, integracioni tokovi i referentni paketi za create tok.

## Aktivni skelet

- `documentation/` — validacija dokumentacije, navigacije i traceability-ja
- `contract/` — ugovorna validacija i kompatibilnost statusa
- `domain/` — domenska pravila i negativni scenariji
- `integration/` — krajnji create tok između aplikacija i servisa
- `audit/` — audit korelacija, KPI signali i regulatorne blokade

## Centralna governance veza

- centralni ulaz: `../docs/06-developer/README.md`
- source-of-truth: `../docs/06-developer/source-of-truth-map.md`, `../docs/06-developer/release-gates.md`, `../docs/06-developer/module-readiness-overview.md`, `../docs/06-developer/program-equivalent-assembly-model.md`
- ownership: `../docs/06-developer/create-domain-ownership-map.md`
- traceability: `../docs/06-developer/traceability-matrix.md`

## Nivoi validacije

- dokumentaciona validacija za konzistentnost zahteva i navigacije
- ugovorna validacija za API specifikacije i statuse
- domenska validacija za pravila profila, procene i licenci
- integraciona validacija za create tok između aplikacija i servisa
- audit validacija za događaje, trag odluke i KPI ulaze

## Pravilo pokrivenosti

- svaki novi ugovor, status ili događaj mora imati test posledicu u odgovarajućem sloju
- negativni scenariji, autorizacija i regulatorne blokade imaju prioritet u ranim talasima
- centralna pravila sledljivosti i release kontrole vode se kroz `../docs/06-developer/README.md`
- test sloj pokazuje ownership i audit posledice kroz povezane domene i ugovore

## Repo-wide radni takt

- obavezni redosled ostaje: zahtev → domen → odluka → ugovor i deljeni modeli → test posledice → audit i usklađenost → implementacija → verifikacija i release odluka
- ovaj artefakt se ne otvara ako prethodni koraci nisu potvrđeni kroz `../docs/06-developer/README.md`, `../docs/06-developer/definition-of-ready.md` i `../docs/06-developer/release-gates.md`
- otvorena pitanja, izuzeci i tehnološke odluke vode se kroz `../docs/06-developer/decision-backlog.md` i `../docs/06-developer/adrs/README.md`, ne lokalno

## Kontrolni stubovi

- bezbednost, privatnost i role-based pristup ulaze u dizajn od početka
- audit trag, manual-review signal, regulatorna blokada i korektivni tok moraju biti vidljivi kada su relevantni
- create jezgro `profil → dokazi → procena → odluka → licenca → audit` ima prioritet nad sekundarnim tokovima
- traceability od izvornog zahteva do ugovora, testova i release odluke ostaje obavezna
- test sloj se montira paralelno sa svakim novim ugovorom, paketom, servisom i aplikativnim tokom iz create jezgra

## Ownership i kontrola

- vlasnici odluke: vlasnici domena i ugovora koje test sloj proverava
- vlasnik isporuke: tehnički vlasnik isporuke test sloja
- vlasnik kontrole: najstroži relevantni vlasnik kontrole iz pogođenih domena
- traceability signal: svaki test sloj mora odražavati relevantne redove iz `../docs/06-developer/traceability-matrix.md`

## Readiness i release

- `../tests/` se šire paralelno sa svakim novim ugovorom, statusom, događajem i kontrolom
- nijedan test README ne uvodi lokalna pravila mimo source-of-truth i traceability dokumentacije
- završna spremnost test sloja proverava se kroz `../docs/06-developer/definition-of-ready.md`, `../docs/06-developer/definition-of-done.md` i `../docs/06-developer/release-gates.md`
