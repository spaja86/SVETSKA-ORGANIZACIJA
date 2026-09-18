# Assessment validation service

## Svrha

Servis za procenu, rezultat, ljudsku reviziju i žalbeni tok.

## Ulazi i izlazi

- ulazi: validan profil, dokazi, kriterijumi procene, partner/evaluator kontekst
- izlazi: preliminarni rezultat, konačna odluka, zahtev za ručnu reviziju, žalbeni status

## Granice odgovornosti

- vodi procenu i odluku nad kriterijumima
- ne izdaje licencu bez saradnje sa `license-service`
- ne upravlja partner akreditacijom bez `partner-engagement-service`

## Povezani artefakti

- `packages/domain-assessment/`
- `packages/shared-statuses/`
- `specs/api/v1/assessment-contract.md`
- `docs/06-developer/manual-review-checkpoints.md`
- `tests/integration/README.md`
