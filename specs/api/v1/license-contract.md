# Ugovor: licenca

## Izvor i ownership

- izvorni dokumenti: `docs/02-platform/global-work-licenses.md`, `docs/03-product/product-requirements.md`
- domen: licence
- povezani moduli: `apps/user-portal/`, `services/license-service/`, `packages/domain-license/`

## Resurs
- licenca i status licence

## Ključne operacije
- izdavanje licence
- pregled statusa licence
- obnova, suspenzija i odbijanje
- pregled istorije statusa

## Statusi
- `pending-issuance`
- `active`
- `rejected`
- `suspended`
- `expired`
- `renewal-pending`

## Kontrole
- validni prelazi statusa
- regulatorne blokade i ovlašćenja
- audit događaji za svaku promenu statusa
- ručna potvrda kada procena ili pravila nisu jednoznačni

## Klase grešaka
- `authorization-error`
- `regulatory-block`
- `conflict-error`
- `review-required`

## Test fokus
- validni i nevalidni prelazi statusa
- blokade po jurisdikciji
- audit za izdavanje, odbijanje i suspenziju
