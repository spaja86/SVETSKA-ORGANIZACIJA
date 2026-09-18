# Ugovor: profil

## Izvor i ownership

- izvorni dokumenti: `docs/03-product/product-requirements.md`, `docs/02-platform/domain-model.md`
- domen: identitet i profil
- povezani moduli: `apps/user-portal/`, `services/profile-identity-service/`, `packages/domain-profile/`

## Resurs
- profil korisnika

## Ključne operacije
- kreiranje profila
- pregled profila
- promena statusa profila
- pregled istorije promena

## Statusi
- `draft`
- `active`
- `pending-review`
- `suspended`
- `archived`

## Kontrole
- obavezna polja i validacija identiteta
- audit događaji za kreiranje i promenu statusa
- kontrola pristupa po ulozi
- povezivanje sa dokazima i istorijom profila

## Klase grešaka
- `validation-error`
- `authorization-error`
- `conflict-error`
- `not-found`

## Test fokus
- validacija kreiranja profila
- zabrana nevažećih promena statusa
- istorija promena i audit događaja
