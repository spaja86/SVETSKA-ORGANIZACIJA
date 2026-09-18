# Partner portal

## Svrha

Partnerski portal za procenu, potvrdu rezultata, angažmane i rad nad predmetima povezanim sa create tokom.

## Izvorni dokumenti

- `docs/05-operations/operating-model.md`
- `docs/06-developer/mvp-create-implementation-plan.md`
- `docs/06-developer/manual-review-checkpoints.md`

## Minimalni ekrani

- radna lista zahteva za procenu
- pregled dokaza i kriterijuma procene
- potvrda rezultata, angažmana i eventualnih sporova
- status partner akreditacije i dodela evaluatora

## Uloge i događaji

- primarne uloge: partner, evaluator
- ključni događaji: `assessment.started`, `assessment.decision.confirmed`, `partner.assigned`, `engagement.confirmed`

## Zavisni moduli

- `services/assessment-validation-service/`
- `services/partner-engagement-service/`
- `packages/domain-assessment/`
- `packages/domain-partner/`
- `specs/api/v1/assessment-contract.md`
- `specs/api/v1/partner-contract.md`
