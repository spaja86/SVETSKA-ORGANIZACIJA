# Traceability matrica

Ova matrica povezuje izvorne dokumente sa domenima, odlukama, interfejsima, testovima i audit zahtevima.

| Oblast | Izvorni dokumenti | Domen | Odluka / kontrolni dokument | Ownership referenca | Budući API ugovori | Budući testovi | Audit fokus | Release odluka |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Identitet i profil | `docs/03-product/product-requirements.md`, `docs/02-platform/domain-model.md` | osoba, kompetencija | `definition-of-ready.md`, `create-domain-ownership-map.md`, `source-of-truth-map.md` | `create-domain-ownership-map.md` — red „Identitet i profil“ | profil, dokaz, status profila | validacija kreiranja profila, kontrola pristupa, istorija promena | otvaranje profila, promena statusa, odbijen dokaz | Gate 1-5, Tier 2/3 prema obimu promene |
| Procena i validacija | `docs/03-product/use-cases-and-user-journeys.md`, `docs/04-policies/security-ethics-and-compliance.md` | procena, rezultat, evaluator | `ai-governance-plan.md`, `release-gates.md`, `manual-review-checkpoints.md` | `create-domain-ownership-map.md` — red „Procena i validacija“ | zahtev za procenu, odluka, ljudska revizija | pozitivni i negativni scenariji procene, žalbe, override | trag odluke, žalba, ručna supervizija | Gate 1-6 kada utiče na MVP odluke, najmanje Tier 3 |
| Licence | `docs/02-platform/global-work-licenses.md`, `docs/03-product/product-requirements.md` | licenca, obnova licence | `definition-of-done.md`, `role-permission-model.md`, `error-taxonomy.md` | `create-domain-ownership-map.md` — red „Licence“ | izdavanje licence, pregled statusa, obnova | statusi licence, zabrana nevažećih prelaza, autorizacija | izdavanje, obnova, suspenzija | Gate 1-6 kada menja create tok, najmanje Tier 2/3 |
| Partneri i angažmani | `docs/02-platform/domain-model.md`, `docs/05-operations/operating-model.md` | partner, posao, projekat, angažman | `create-domain-ownership-map.md`, `external-integration-map.md` | `create-domain-ownership-map.md` — red „Partneri i angažmani“ | dodela partnera, potvrda angažmana | partner pristup, potvrda učinka, sporni angažman | partner akcije, potvrde | Gate 1-5, Tier 2/3 prema integracionom uticaju |
| Audit i KPI | `docs/05-operations/kpi-framework.md`, `docs/04-policies/data-governance.md` | audit, izveštavanje | `observability-plan.md`, `create-data-governance-plan.md`, `event-naming-standard.md` | `create-domain-ownership-map.md` — red „Audit i KPI“ | audit događaj, KPI agregat | kompletiranje događaja, integritet metrika, korelacija | neizmenjiv trag, praćenje učinka | Gate 1-6 za produkcione signale, najmanje Tier 3 |
| Regulatorna pravila | `docs/04-policies/legal-and-regulatory-framework.md`, `docs/04-policies/data-governance.md` | regulator, jurisdikcija, region | `localization-and-jurisdiction-plan.md`, `release-gates.md`, `data-classification-and-handling.md` | `create-domain-ownership-map.md` — red „Regulatorna pravila“ | pravilo jurisdikcije, izuzetak, ograničenje | lokalna pravila, blokade tokova, override evidencija | osnov odluke, lokalno pravilo | Gate 1-6 kada blokira MVP tok, najmanje Tier 3 |

## Pravilo održavanja

- svaka nova funkcionalnost mora proširiti najmanje jedan red ili dodati novi red
- nijedan API ugovor ne ulazi u finalizaciju bez reference na izvorni dokument, kontrolni dokument i test posledice
- osetljivi tokovi moraju imati eksplicitno naveden audit fokus i model dozvola kada je relevantno
- kada dokument postane source-of-truth za oblast, mora biti dodat i u `source-of-truth-map.md`
- svaki red mora ostati usklađen sa ownership mapom, release nivoom i readiness dokazom relevantnog sloja
