# Mapa ownership-a za create domene

## Svrha

Ovaj dokument povezuje domene, glavne artefakte i buduće servisne granice sa vlasnicima odluke, vlasnicima isporuke i vlasnicima kontrole.

## Pravilo ownership-a

- vlasnik odluke potvrđuje opseg, pravila i granice domena
- vlasnik isporuke potvrđuje da su artefakti potpuni, povezani i proverljivi
- vlasnik kontrole je jedan primarni odgovorni nosilac kontrola za domen
- vlasnik kontrole potvrđuje bezbednost, privatnost, audit, regulatorne blokade i release proveru
- isti vlasnik može pokrivati više uloga samo dok ne postoji potreba za odvajanjem odgovornosti
- isti vlasnik može privremeno pokrivati sve tri uloge samo dok sloj ostaje u dokumentacionoj fazi

## Domeni i odgovornosti

| Domen | Vlasnik odluke | Vlasnik isporuke | Vlasnik kontrole | Podrška kontroli | Primarni artefakti | Buduće granice |
| --- | --- | --- | --- | --- | --- | --- |
| Identitet i profil | produkt + tehnički vlasnik domena | tehnički vlasnik implementacije | bezbednosni vlasnik domena | privatnost, audit, tehnički vlasnik kontrole | `apps/user-portal/`, `services/profile-identity-service/`, `packages/domain-profile/`, `specs/api/v1/profile-contract.md`, `specs/api/v1/evidence-contract.md` | profil, identitet, dokazi, statusi |
| Procena i validacija | produkt + policy + tehnički vlasnik | tehnički vlasnik implementacije | AI governance vlasnik domena | policy, audit, tehnički vlasnik kontrole | `apps/partner-portal/`, `apps/admin-portal/`, `services/assessment-validation-service/`, `packages/domain-assessment/`, `specs/api/v1/assessment-contract.md` | procena, rezultat, žalba, ručna revizija |
| Licence | produkt + policy + tehnički vlasnik | tehnički vlasnik implementacije | policy vlasnik licence | audit, regulatorna usklađenost, tehnički vlasnik kontrole | `apps/user-portal/`, `services/license-service/`, `packages/domain-license/`, `specs/api/v1/license-contract.md` | izdavanje, obnova, suspenzija, istorija statusa |
| Partneri i angažmani | operativni + tehnički vlasnik | tehnički vlasnik implementacije | operativni kontrolni vlasnik partnera | audit, policy, tehnički vlasnik kontrole | `apps/partner-portal/`, `services/partner-engagement-service/`, `packages/domain-partner/`, `specs/api/v1/partner-contract.md` | partneri, angažmani, potvrde |
| Audit i KPI | operativni + policy + tehnički vlasnik | tehnički vlasnik implementacije | observability vlasnik domena | audit, policy, tehnički vlasnik kontrole | `apps/admin-portal/`, `services/audit-reporting-service/`, `packages/domain-audit/`, `specs/api/v1/audit-event-contract.md` | događaji, trag, KPI, incident signali |
| Regulatorna pravila | policy + operativni + tehnički vlasnik | tehnički vlasnik implementacije | regulatorni vlasnik domena | privatnost, audit, tehnički vlasnik kontrole | `apps/admin-portal/`, `services/regulatory-rules-service/`, `packages/domain-regulatory/` | jurisdikcije, ograničenja, izuzeci |

## Pravilo za nove artefakte

Svaki novi artefakt mora navesti:

- domen kome pripada
- vlasnika odluke i vlasnika isporuke
- vlasnika kontrole
- izvorni dokument ili dokumente
- povezane API, test i audit posledice

## Pravilo zabrane preklapanja

- aplikacija ne redefiniše domenski model koji pripada `packages/`
- servis ne redefiniše status ili događaj bez promene u centralnom katalogu
- ugovor ne menja ownership granice bez ažuriranja ove mape i traceability matrice
