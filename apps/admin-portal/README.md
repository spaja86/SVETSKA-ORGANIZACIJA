# Admin portal

## Svrha

Administrativni portal za audit, KPI, regulatorne blokade, override odluke i operativni nadzor.

## Izvorni dokumenti

- `docs/04-policies/legal-and-regulatory-framework.md`
- `docs/05-operations/kpi-framework.md`
- `docs/06-developer/observability-plan.md`

## Minimalni ekrani

- pregled audit događaja i korelacija
- regulatorne blokade i ručne revizije
- KPI signal i osnovni dashboard za create tok
- pregled izuzetaka, incidenata i neuspelih korelacija

## Uloge i događaji

- primarne uloge: administrator, compliance, operativni nadzor
- ključni događaji: `audit.trace.correlated`, `audit.exception.flagged`, `jurisdiction.blocked`, `assessment.human-review.requested`

## Zavisni moduli

- `services/audit-reporting-service/`
- `services/regulatory-rules-service/`
- `services/assessment-validation-service/`
- `packages/domain-audit/`
- `packages/domain-regulatory/`
- `specs/api/v1/audit-event-contract.md`
- `specs/api/v1/assessment-contract.md`
