# Struktura repozitorijuma

## Pravilo rasporeda

- `docs/` sadrži izvor istine za strategiju, operacije i tehničku osnovu
- `apps/` će sadržati korisničke i administrativne interfejse
- `services/` će sadržati servisne granice i integracije
- `packages/` će sadržati deljene modele, pravila i biblioteke
- `specs/api/` će sadržati API specifikacije, ugovore razmene podataka, verzioniranje interfejsa i pravila interoperabilnosti
- `tests/` će sadržati test strategiju i buduće scenarije validacije

## Prvi kandidati po direktorijumima

- `apps/` — javni portal, portal korisnika, portal partnera, administrativni portal
- `services/` — servis profila, servis procene, servis licenci, audit servis, regulatorni servis
- `packages/` — deljeni domenski modeli, statusi, validaciona pravila, audit tipovi događaja
- `specs/api/` — ugovori za profil, dokaze, procenu, licencu, partnere i audit događaje
- `tests/` — dokumentaciona validacija, ugovorni scenariji, domenski tokovi, integracioni i audit testovi

## Pravilo širenja

Novi sadržaj se dodaje u postojeći sloj kada je moguće. Novi direktorijum se uvodi tek kada postoji jasan domenski razlog i održiva količina sadržaja.

## Pravilo novog artefakta

Svaki novi artefakt mora da navede:

- vlasnika
- svrhu
- granice odgovornosti
- referencu na izvorni dokument
- očekivanu vezu sa API-jem, testovima i auditom kada je relevantno
