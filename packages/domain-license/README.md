# Domain license

## Svrha

Početni skelet za modele licenci, statusa, obnove i suspenzije.

## Sadržaj paketa

- entiteti: licenca, status licence, istorija statusa
- statusi: `pending-issuance`, `active`, `rejected`, `suspended`, `expired`, `renewal-pending`
- validacije: dozvoljeni prelazi, regulatorna blokada, autorizacija promene

## Povezani artefakti

- `specs/api/v1/license-contract.md`
- `services/license-service/`
- `tests/domain/README.md`
- `tests/audit/README.md`
