# Traceability matrica

Ova matrica povezuje izvorne dokumente sa domenima, odlukama, interfejsima, testovima i audit zahtevima.

| Oblast | Izvorni dokumenti | Domen | Odluka / kontrolni dokument | Budući API ugovori | Budući testovi | Audit fokus |
| --- | --- | --- | --- | --- | --- | --- |
| Identitet i profil | `docs/03-product/product-requirements.md`, `docs/02-platform/domain-model.md` | osoba, kompetencija | `definition-of-ready.md`, `create-domain-ownership-map.md`, `source-of-truth-map.md` | profil, dokaz, status profila | validacija kreiranja profila, kontrola pristupa, istorija promena | otvaranje profila, promena statusa, odbijen dokaz |
| Procena i validacija | `docs/03-product/use-cases-and-user-journeys.md`, `docs/04-policies/security-ethics-and-compliance.md` | procena, rezultat, evaluator | `ai-governance-plan.md`, `release-gates.md`, `manual-review-checkpoints.md` | zahtev za procenu, odluka, ljudska revizija | pozitivni i negativni scenariji procene, žalbe, override | trag odluke, žalba, ručna supervizija |
| Licence | `docs/02-platform/global-work-licenses.md`, `docs/03-product/product-requirements.md` | licenca, obnova licence | `definition-of-done.md`, `role-permission-model.md`, `error-taxonomy.md` | izdavanje licence, pregled statusa, obnova | statusi licence, zabrana nevažećih prelaza, autorizacija | izdavanje, obnova, suspenzija |
| Partneri i angažmani | `docs/02-platform/domain-model.md`, `docs/05-operations/operating-model.md` | partner, posao, projekat, angažman | `create-domain-ownership-map.md`, `external-integration-map.md` | dodela partnera, potvrda angažmana | partner pristup, potvrda učinka, sporni angažman | partner akcije, potvrde |
| Audit i KPI | `docs/05-operations/kpi-framework.md`, `docs/04-policies/data-governance.md` | audit, izveštavanje | `observability-plan.md`, `create-data-governance-plan.md`, `event-naming-standard.md` | audit događaj, KPI agregat | kompletiranje događaja, integritet metrika, korelacija | neizmenjiv trag, praćenje učinka |
| Regulatorna pravila | `docs/04-policies/legal-and-regulatory-framework.md`, `docs/04-policies/data-governance.md` | regulator, jurisdikcija, region | `localization-and-jurisdiction-plan.md`, `release-gates.md`, `data-classification-and-handling.md` | pravilo jurisdikcije, izuzetak, ograničenje | lokalna pravila, blokade tokova, override evidencija | osnov odluke, lokalno pravilo |

## Pravilo održavanja

- svaka nova funkcionalnost mora proširiti najmanje jedan red ili dodati novi red
- nijedan API ugovor ne ulazi u finalizaciju bez reference na izvorni dokument, kontrolni dokument i test posledice
- osetljivi tokovi moraju imati eksplicitno naveden audit fokus i model dozvola kada je relevantno
- kada dokument postane source-of-truth za oblast, mora biti dodat i u `source-of-truth-map.md`
