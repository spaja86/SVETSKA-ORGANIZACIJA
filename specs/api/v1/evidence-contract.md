# Ugovor: dokazi

## Izvor i ownership

- izvorni dokumenti: `docs/03-product/product-requirements.md`, `docs/04-policies/data-governance.md`
- domen: identitet i profil
- povezani moduli: `apps/user-portal/`, `services/profile-identity-service/`, `packages/domain-profile/`

## Resurs
- dokaz kompetencije

## Ključne operacije
- unos dokaza
- pregled istorije dokaza
- promena validnosti ili statusa dokaza

## Kontrole
- validacija formata, porekla i povezanosti sa profilom
- retencija i minimizacija podataka
- audit događaji za unos i odbijanje
- ručna revizija kada dokaz nosi visok regulatorni rizik

## Klase grešaka
- `validation-error`
- `authorization-error`
- `regulatory-block`
- `review-required`

## Test fokus
- negativni scenariji za nekompletan dokaz
- poreklo i veza sa profilom
- audit za unos, odbijanje i vraćanje na dopunu
