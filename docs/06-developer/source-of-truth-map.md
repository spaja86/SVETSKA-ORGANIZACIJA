# Source-of-truth mapa

## Svrha

Ovaj dokument određuje koji artefakt zaključava koju oblast kako bi se izbeglo dupliranje pravila i kontradiktorna značenja.

## Primarna mapa

| Oblast | Source-of-truth artefakt | Sekundarni artefakti koji se usklađuju |
| --- | --- | --- |
| Repo-wide create governance ulaz | `docs/06-developer/README.md` | svi tehnički README, `CONTRIBUTING.md`, `docs/README.md` |
| Razvojni lifecycle | `docs/06-developer/developer-guide.md` | `change-management.md`, `definition-of-ready.md`, `definition-of-done.md` |
| Create opseg i faze | `docs/06-developer/mvp-create-implementation-plan.md` | `traceability-matrix.md`, `module-readiness-overview.md`, `specs/api/mvp-create-flow-contracts.md` |
| Ownership i granice | `docs/06-developer/create-domain-ownership-map.md` | `repository-structure.md`, README skeleti modula |
| Klasifikacija release nivoa promene | `docs/06-developer/release-tier-model.md` | `release-gates.md`, `definition-of-ready.md`, `definition-of-done.md` |
| Statusi i događaji | `docs/06-developer/domain-status-and-events-catalog.md` | `event-naming-standard.md`, v1 ugovori, `tests/domain/README.md`, `packages/shared-statuses/README.md` |
| Release gate kontrole po fazi | `docs/06-developer/release-gates.md` | `definition-of-ready.md`, `definition-of-done.md`, `release-tier-model.md`, svi tehnički README |
| API greške i klase odgovora | `docs/06-developer/error-taxonomy.md` | error sekcije u `specs/api/v1/*.md`, `tests/contract/README.md`, `packages/shared-validation/README.md` |
| API resursi, operacije i interoperabilnost | `docs/06-developer/api-contract-governance.md` | `specs/api/README.md`, `specs/api/v1/*.md`, `tests/contract/README.md` |
| Ručna revizija | `docs/06-developer/manual-review-checkpoints.md` | `ai-governance-plan.md`, `specs/api/v1/assessment-contract.md`, `apps/admin-portal/README.md` |
| Klasifikacija podataka | `docs/06-developer/data-classification-and-handling.md` | `create-data-governance-plan.md`, `specs/api/v1/evidence-contract.md`, `specs/api/v1/profile-contract.md` |
| Međudomenske zavisnosti | `docs/06-developer/cross-domain-dependency-map.md` | `traceability-matrix.md`, `mvp-create-implementation-plan.md`, `specs/api/mvp-create-flow-contracts.md` |
| Readiness dokazi po slojevima | `docs/06-developer/module-readiness-overview.md` | README skeleti modula, `definition-of-ready.md`, `release-gates.md` |
| Otvorene odluke i blokatori | `docs/06-developer/decision-backlog.md` | `adrs/README.md`, `repository-evolution-migration-plan.md`, `module-readiness-overview.md` |
| Lokalizacija i jurisdikcija | `docs/06-developer/localization-and-jurisdiction-plan.md` | `create-data-governance-plan.md`, `release-gates.md`, `services/regulatory-rules-service/README.md` |
| Observability i KPI signal | `docs/06-developer/observability-plan.md` | `traceability-matrix.md`, `services/audit-reporting-service/README.md`, `tests/audit/README.md` |
| Traceability između zahteva, ugovora i testova | `docs/06-developer/traceability-matrix.md` | svi tehnički README, `specs/api/README.md`, `tests/README.md` |

## Pravilo izmene

- menja se prvo source-of-truth artefakt, zatim svi zavisni dokumenti i skeleti
- ako nije jasno gde je izvor istine, promena ne prelazi Gate 1
- kada se uvede novi source-of-truth, mora biti dodat u developer indeks i traceability matricu kada je relevantno
- nijedan sloj van `docs/06-developer/` ne otvara novo značenje dok njegov source-of-truth red nije eksplicitno pokriven ovom mapom
- deljeni i višedomenski artefakti ne mogu postati source-of-truth za ownership, status, greške ili release pravila; oni samo nasleđuju i prikazuju centralne odluke
