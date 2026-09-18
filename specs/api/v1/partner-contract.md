# Ugovor: partner

## Izvor i ownership

- izvorni dokumenti: `docs/02-platform/domain-model.md`, `docs/05-operations/operating-model.md`
- domen: partneri i angažmani
- povezani moduli: `apps/partner-portal/`, `services/partner-engagement-service/`, `packages/domain-partner/`

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

## Klase grešaka
- `authorization-error`
- `validation-error`
- `conflict-error`
- `not-found`

## Test fokus
- akreditacija i deaktivacija partnera
- ograničenje angažmana po ulozi
- audit za dodelu i sporni angažman
