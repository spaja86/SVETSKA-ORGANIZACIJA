# Struktura repozitorijuma

## Pravilo rasporeda

- `docs/` sadrži izvor istine za strategiju, operacije i tehničku osnovu
- `apps/` sadrži skelet korisničkih i administrativnih interfejsa
- `services/` sadrži skelet servisnih granica i integracija
- `packages/` sadrži skelet deljenih modela, pravila i biblioteka
- `specs/api/` sadrži verzionisane API specifikacije, ugovore razmene podataka i pravila interoperabilnosti
- `tests/` sadrži test strategiju, scenarije validacije i referentne test pakete

## Aktivni skelet po direktorijumima

- `apps/` — `apps/public-portal/`, `apps/user-portal/`, `apps/partner-portal/`, `apps/admin-portal/`
- `services/` — `services/profile-identity-service/`, `services/assessment-validation-service/`, `services/license-service/`, `services/partner-engagement-service/`, `services/audit-reporting-service/`, `services/regulatory-rules-service/`
- `packages/` — `packages/domain-profile/`, `packages/domain-assessment/`, `packages/domain-license/`, `packages/domain-partner/`, `packages/domain-audit/`, `packages/domain-regulatory/`, `packages/shared-statuses/`, `packages/shared-validation/`
- `specs/api/` — `specs/api/v1/`, `specs/api/mvp-create-flow-contracts.md`
- `tests/` — `tests/documentation/`, `tests/contract/`, `tests/domain/`, `tests/integration/`, `tests/audit/`

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

## Pravilo readiness-a po sloju

- `docs/` zaključava značenje, source-of-truth i otvorene odluke
- `apps/` dokumentuju minimalne ekrane, uloge, događaje i izlaze
- `services/` dokumentuju ulaze, izlaze, zabrane preklapanja i audit posledice
- `packages/` dokumentuju entitete, statuse, validacije i zavisne ugovore
- `specs/api/` dokumentuju resurse, operacije, greške, paginaciju i audit metadata
- `tests/` dokumentuju šta proveravaju, kada se proširuju i na koje ugovore ili događaje se oslanjaju

## Pravilo centralnog povezivanja

- svaka create referenca iz skeleta vodi ka `docs/06-developer/README.md`
- svaka servisna ili aplikaciona referenca mora pokazati povezani paket, ugovor i test sloj
- svaka promena statusa ili događaja mora ostati usklađena sa `domain-status-and-events-catalog.md`
