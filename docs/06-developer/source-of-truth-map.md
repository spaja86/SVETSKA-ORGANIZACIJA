# Source-of-truth mapa

## Svrha

Ovaj dokument određuje koji artefakt zaključava koju oblast kako bi se izbeglo dupliranje pravila i kontradiktorna značenja.

## Primarna mapa

| Oblast | Source-of-truth artefakt | Sekundarni artefakti koji se usklađuju |
| --- | --- | --- |
| Razvojni lifecycle | `docs/06-developer/developer-guide.md` | `change-management.md`, `definition-of-ready.md`, `definition-of-done.md` |
| Create opseg i faze | `docs/06-developer/mvp-create-implementation-plan.md` | `traceability-matrix.md`, `module-readiness-overview.md`, `specs/api/mvp-create-flow-contracts.md` |
| Ownership i granice | `docs/06-developer/create-domain-ownership-map.md` | `repository-structure.md`, README skeleti modula |
| Statusi i događaji | `docs/06-developer/domain-status-and-events-catalog.md` | `event-naming-standard.md`, v1 ugovori, `tests/domain/README.md` |
| Release kontrole | `docs/06-developer/release-gates.md` | `definition-of-ready.md`, `definition-of-done.md`, `release-tier-model.md` |
| API standardi | `docs/06-developer/error-taxonomy.md` + `specs/api/README.md` | `specs/api/v1/*.md`, `tests/contract/README.md` |
| Ručna revizija | `docs/06-developer/manual-review-checkpoints.md` | `ai-governance-plan.md`, `specs/api/v1/assessment-contract.md`, `apps/admin-portal/README.md` |
| Klasifikacija podataka | `docs/06-developer/data-classification-and-handling.md` | `create-data-governance-plan.md`, `specs/api/v1/evidence-contract.md`, `specs/api/v1/profile-contract.md` |

## Pravilo izmene

- menja se prvo source-of-truth artefakt, zatim svi zavisni dokumenti
- ako nije jasno gde je izvor istine, promena ne prelazi Gate 1
- kada se uvede novi source-of-truth, mora biti dodat u developer indeks i traceability matricu kada je relevantno
