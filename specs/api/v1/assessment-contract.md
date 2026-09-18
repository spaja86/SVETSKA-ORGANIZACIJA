# Ugovor: procena

## Izvor i ownership

- izvorni dokumenti: `docs/03-product/use-cases-and-user-journeys.md`, `docs/04-policies/security-ethics-and-compliance.md`
- domen: procena i validacija
- povezani moduli: `apps/partner-portal/`, `apps/admin-portal/`, `services/assessment-validation-service/`, `packages/domain-assessment/`

## Resurs
- zahtev za procenu i rezultat

## Ključne operacije
- otvaranje zahteva za procenu
- evidentiranje rezultata
- potvrda ljudske revizije i žalbe
- potvrda konačne odluke

## Statusi
- `requested`
- `in-review`
- `awaiting-human-review`
- `approved`
- `rejected`
- `appealed`

## Kontrole
- audit trag za odluku i ručnu superviziju
- jasno razdvajanje preliminarne i konačne odluke
- manual review checkpoint za visokorizične odluke

## Klase grešaka
- `validation-error`
- `authorization-error`
- `review-required`
- `internal-integrity-error`

## Test fokus
- pozitivni i negativni scenariji procene
- žalbeni tok i override
- korelacija sa dokazima i licencom
