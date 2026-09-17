# Traceability matrica

Ova matrica povezuje izvorne dokumente sa domenima, interfejsima, testovima i audit zahtevima.

| Oblast | Izvorni dokumenti | Domen | Budući API ugovori | Budući testovi | Audit fokus |
| --- | --- | --- | --- | --- | --- |
| Identitet i profil | `docs/03-product/product-requirements.md`, `docs/02-platform/domain-model.md` | osoba, kompetencija | profil, dokaz, status profila | validacija kreiranja profila, kontrola pristupa | otvaranje profila, promena statusa |
| Procena i validacija | `docs/03-product/use-cases-and-user-journeys.md`, `docs/04-policies/security-ethics-and-compliance.md` | procena, rezultat, evaluator | zahtev za procenu, odluka, ljudska revizija | pozitivni i negativni scenariji procene | trag odluke, žalba, ručna supervizija |
| Licence | `docs/02-platform/global-work-licenses.md`, `docs/03-product/product-requirements.md` | licenca, obnova licence | izdavanje licence, pregled statusa, obnova | statusi licence, zabrana nevažećih prelaza | izdavanje, obnova, suspenzija |
| Partneri i angažmani | `docs/02-platform/domain-model.md`, `docs/05-operations/operating-model.md` | partner, posao, projekat, angažman | dodela partnera, potvrda angažmana | partner pristup, potvrda učinka | partner akcije, potvrde |
| Audit i KPI | `docs/05-operations/kpi-framework.md`, `docs/04-policies/data-governance.md` | audit, izveštavanje | audit događaj, KPI agregat | kompletiranje događaja i integriteta metrika | neizmenjiv trag, praćenje učinka |
| Regulatorna pravila | `docs/04-policies/legal-and-regulatory-framework.md`, `docs/04-policies/data-governance.md` | regulator, jurisdikcija, region | pravilo jurisdikcije, izuzetak, ograničenje | lokalna pravila i blokade tokova | osnov odluke, lokalno pravilo |

## Pravilo održavanja

- svaka nova funkcionalnost mora proširiti najmanje jedan red ili dodati novi red
- nijedan API ugovor ne ulazi u finalizaciju bez reference na izvorni dokument i test posledice
- osetljivi tokovi moraju imati eksplicitno naveden audit fokus
