# Ugovor: partner

## Izvor i ownership

- izvorni dokumenti: `docs/02-platform/domain-model.md`, `docs/05-operations/operating-model.md`
- domen: partneri i angažmani
- povezani moduli: `apps/partner-portal/`, `services/partner-engagement-service/`, `packages/domain-partner/`

## Governance veza

- centralni ulaz: `docs/06-developer/README.md`
- source-of-truth: `docs/06-developer/source-of-truth-map.md`, `docs/06-developer/api-contract-governance.md`, `docs/06-developer/domain-status-and-events-catalog.md`, `docs/06-developer/error-taxonomy.md`
- traceability: `docs/06-developer/traceability-matrix.md`
- repo-wide radni takt: zahtev → domen → odluka → ugovor i deljeni modeli → test posledice → audit i usklađenost → implementacija → verifikacija i release odluka

## Ownership trojka

- vlasnik odluke: operativni + tehnički vlasnik domena
- vlasnik isporuke: tehnički vlasnik implementacije ugovora i zavisnih modula
- vlasnik kontrole: bezbednosni, audit i regulatorni vlasnik prema tipu angažmana

## Resurs
- partner i angažman

## Ključne operacije
- akreditacija partnera
- dodela partnera ili evaluatora
- potvrda angažmana ili učinka

## Kontrole
- role-based pristup
- jasna odgovornost po angažmanu
- audit događaji za dodelu i potvrdu
- zabrana procene bez validne akreditacije

## Audit, manual review i test posledice
- audit posledice: svaki zahtev, promena statusa, ručna odluka, regulatorna blokada i izuzetak moraju ostaviti korelisan trag
- manual review: obavezan za sporni angažman, akreditaciju partnera i regulatorni izuzetak
- test posledice: `tests/contract/README.md`, `tests/domain/README.md`, `tests/integration/README.md`, `tests/audit/README.md`

## Klase grešaka
- `authorization-error`
- `validation-error`
- `conflict-error`
- `not-found`

## Test fokus
- akreditacija i deaktivacija partnera
- ograničenje angažmana po ulozi
- audit za dodelu i sporni angažman
