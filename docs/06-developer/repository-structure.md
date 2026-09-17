# Struktura repozitorijuma

## Pravilo rasporeda

- `docs/` sadrži izvor istine za strategiju, operacije i tehničku osnovu
- `apps/` će sadržati korisničke i administrativne interfejse
- `services/` će sadržati servisne granice i integracije
- `packages/` će sadržati deljene modele, pravila i biblioteke
- `specs/api/` će sadržati API specifikacije, ugovore razmene podataka, verzioniranje interfejsa i pravila interoperabilnosti
- `tests/` će sadržati test strategiju i buduće scenarije validacije

## Pravilo širenja

Novi sadržaj se dodaje u postojeći sloj kada je moguće. Novi direktorijum se uvodi tek kada postoji jasan domenski razlog i održiva količina sadržaja.
