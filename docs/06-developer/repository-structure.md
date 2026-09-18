# Struktura repozitorijuma

## Pravilo rasporeda

- `docs/` sadrži izvor istine za strategiju, operacije i tehničku osnovu
- `apps/` sadrži skelet korisničkih i administrativnih interfejsa
- `services/` sadrži skelet servisnih granica i integracija
- `packages/` sadrži skelet deljenih modela, pravila i biblioteka
- `specs/api/` sadrži verzionisane API specifikacije, ugovore razmene podataka i pravila interoperabilnosti
- `tests/` sadrži test strategiju, scenarije validacije i referentne test pakete

## Aktivni skelet po direktorijumima

- `apps/` — `public-portal/`, `user-portal/`, `partner-portal/`, `admin-portal/`
- `services/` — `profile-identity-service/`, `assessment-validation-service/`, `license-service/`, `partner-engagement-service/`, `audit-reporting-service/`, `regulatory-rules-service/`
- `packages/` — `domain-profile/`, `domain-assessment/`, `domain-license/`, `domain-partner/`, `domain-audit/`, `domain-regulatory/`, `shared-statuses/`, `shared-validation/`
- `specs/api/` — `v1/`, `mvp-create-flow-contracts.md`
- `tests/` — `documentation/`, `contract/`, `domain/`, `integration/`, `audit/`

## Pravilo širenja

Novi sadržaj se dodaje u postojeći sloj kada je moguće. Novi direktorijum se uvodi tek kada postoji jasan domenski razlog, potvrđeno vlasništvo i održiva količina sadržaja.

## Pravilo novog artefakta

Svaki novi artefakt mora da navede:

- vlasnika odluke
- vlasnika isporuke
- svrhu
- granice odgovornosti
- referencu na izvorni dokument
- očekivanu vezu sa API-jem, testovima i auditom kada je relevantno
