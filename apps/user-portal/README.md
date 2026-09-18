# User portal

## Svrha

Početni skelet za korisnički create tok: profil, dokazi, status licence i istorija zahteva.

## Izvorni dokumenti

- `docs/03-product/product-requirements.md`
- `docs/03-product/use-cases-and-user-journeys.md`
- `docs/06-developer/mvp-create-implementation-plan.md`

## Minimalni ekrani

- kreiranje i pregled profila
- unos i pregled dokaza
- pregled statusa procene i licence
- istorija promena i ključnih audit tačaka vidljivih korisniku

## Uloge i događaji

- primarna uloga: korisnik
- ključni događaji: `profile.created`, `evidence.submitted`, `license.status.changed`

## Zavisni moduli

- `services/profile-identity-service/`
- `services/license-service/`
- `packages/domain-profile/`
- `packages/domain-license/`
- `specs/api/v1/profile-contract.md`
- `specs/api/v1/evidence-contract.md`
- `specs/api/v1/license-contract.md`
