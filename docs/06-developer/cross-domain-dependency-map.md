# Mapa međudomenskih zavisnosti

## Svrha

Create tok prelazi kroz više domena; ova mapa sprečava da jedan domen uvede pravilo bez posledica po ostale zavisne oblasti.

## Primarne zavisnosti

| Izvorni domen | Zavisni domen | Zašto postoji zavisnost | Kontrolni dokument |
| --- | --- | --- | --- |
| Identitet i profil | Procena i validacija | procena ne može početi bez validnog profila i povezanih dokaza | `mvp-create-implementation-plan.md`, `profile-contract.md`, `evidence-contract.md` |
| Procena i validacija | Licence | licenca zavisi od potvrđene odluke procene | `assessment-contract.md`, `license-contract.md` |
| Licence | Audit i KPI | svaka promena statusa licence mora emitovati audit i KPI signal | `audit-event-contract.md`, `observability-plan.md` |
| Regulatorna pravila | Identitet i profil | lokalna pravila mogu ograničiti prihvatljive dokaze ili identitet | `create-data-governance-plan.md`, `data-classification-and-handling.md` |
| Regulatorna pravila | Procena i validacija | pravila mogu zahtevati ručnu reviziju ili zabraniti automatsku odluku | `manual-review-checkpoints.md`, `ai-governance-plan.md` |
| Partneri i angažmani | Procena i validacija | partner ili evaluator mora biti akreditovan pre donošenja odluke | `partner-contract.md`, `role-permission-model.md` |
| Audit i KPI | Svi domeni | svi create koraci ostavljaju trag i signal za kasniju proveru | `event-naming-standard.md`, `traceability-matrix.md` |

## Pravilo izmene zavisnosti

- nova zavisnost mora biti uvedena pre nego što se menja ugovor ili status
- kada se promeni zavisnost, moraju se proveriti test, audit i release posledice
- zavisnosti koje uvode ručni override moraju imati eksplicitnu ulogu i evidenciju razloga
