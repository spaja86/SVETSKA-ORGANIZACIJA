# Checkpoint-i ručne revizije

## Svrha

Ovaj dokument određuje kada automatizovani ili poluautomatizovani create tok mora stati i sačekati ljudsku odluku.

## Obavezni checkpoint-i

| Korak | Okidač ručne revizije | Očekivani izlaz | Povezani artefakti |
| --- | --- | --- | --- |
| Unos dokaza | sumnjivo poreklo, nepotpun dokaz ili konflikt sa profilom | prihvati, odbij ili vrati na dopunu | `specs/api/v1/evidence-contract.md`, `packages/domain-profile/README.md` |
| Procena | AI preporuka visokog rizika ili kontradikcija kriterijuma | potvrđen rezultat ili eskalacija | `specs/api/v1/assessment-contract.md`, `ai-governance-plan.md` |
| Odluka o licenci | regulatorna blokada ili sporni rezultat procene | izdavanje, odbijanje ili dodatna provera | `specs/api/v1/license-contract.md`, `role-permission-model.md` |
| Partner angažman | neusklađena akreditacija ili sporni angažman | potvrdi, ograniči ili deaktiviraj partnera | `specs/api/v1/partner-contract.md`, `packages/domain-partner/README.md` |
| Audit korelacija | nedostajući ili neusaglašen događaji | incident, korekcija ili ponovna korelacija | `specs/api/v1/audit-event-contract.md`, `tests/audit/README.md` |

## Pravilo evidencije

- ručna revizija mora imati razlog, ulogu aktera i vremensku oznaku
- odluka ručne revizije mora imati jasan uticaj na status i audit trag
- slučaj bez definisanog izlaza ne može preći u implementaciju
