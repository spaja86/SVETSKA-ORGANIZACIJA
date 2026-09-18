# Domain audit

## Svrha

Početni skelet za audit događaje, korelaciju, KPI signale i incidentne izuzetke.

## Sadržaj paketa

- entiteti: audit događaj, korelacioni zapis, KPI signal, incident zastavica
- statusi: `recorded`, `correlated`, `flagged`, `exported`
- validacije: neizmenjivost, potpuna metadata, veza sa create korakom

## Povezani artefakti

- `specs/api/v1/audit-event-contract.md`
- `services/audit-reporting-service/`
- `docs/06-developer/event-naming-standard.md`
- `tests/audit/README.md`
