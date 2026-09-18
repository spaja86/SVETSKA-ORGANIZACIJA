# Audit reporting service

## Svrha

Servis za audit događaje, korelaciju create traga, KPI agregaciju i incident signal.

## Ulazi i izlazi

- ulazi: događaji iz svih create domena
- izlazi: korelisani audit trag, KPI metrički ulazi, označeni izuzeci i incidenti

## Granice odgovornosti

- čuva i koreliše događaje
- ne menja poslovne odluke iz drugih domena
- signalizira neusaglašenost, ali ne rešava je bez odgovornog domena

## Povezani artefakti

- `packages/domain-audit/`
- `specs/api/v1/audit-event-contract.md`
- `docs/06-developer/event-naming-standard.md`
- `tests/audit/README.md`
