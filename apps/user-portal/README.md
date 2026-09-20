# User portal

## Svrha

Početni skelet za korisnički create tok: profil, dokazi, status licence i istorija zahteva.

## Izvorni dokumenti

- `../../docs/03-product/product-requirements.md`
- `../../docs/03-product/use-cases-and-user-journeys.md`
- `../../docs/06-developer/mvp-create-implementation-plan.md`

## Minimalni ekrani

- kreiranje i pregled profila
- unos i pregled dokaza
- pregled statusa procene i licence
- istorija promena i ključnih audit tačaka vidljivih korisniku

## Uloge i događaji

- primarna uloga: korisnik
- ključni događaji: `profile.created`, `evidence.submitted`, `license.status.changed`

## Centralna governance veza

- centralni ulaz: `../../docs/06-developer/README.md`
- source-of-truth: `../../docs/06-developer/mvp-create-implementation-plan.md`, `../../docs/06-developer/create-domain-ownership-map.md`, `../../docs/06-developer/role-permission-model.md`
- ownership: `../../docs/06-developer/create-domain-ownership-map.md`
- traceability: `../../docs/06-developer/traceability-matrix.md`

## Ownership i kontrola

- vlasnik odluke: produkt + tehnički vlasnik domena, plus produkt + policy + tehnički vlasnik za deo licence
- vlasnik isporuke: tehnički vlasnik implementacije
- vlasnik kontrole: bezbednosni vlasnik domena uz policy, audit i regulatornu podršku
- traceability signal: portal pokriva redove Identitet i profil i Licence iz traceability matrice i mora ostati usklađen sa njihovim statusima i kontrolama

## Readiness i release

- zavisni moduli: `../../services/profile-identity-service/`, `../../services/license-service/`, `../../packages/domain-profile/`, `../../packages/domain-license/`, `../../specs/api/v1/profile-contract.md`, `../../specs/api/v1/evidence-contract.md`, `../../specs/api/v1/license-contract.md`
- portal se otvara tek nakon potvrđenih ugovora, shared paketa i zavisnih servisa
- završna spremnost proverava se kroz `../../docs/06-developer/definition-of-ready.md`, `../../docs/06-developer/definition-of-done.md` i `../../docs/06-developer/release-gates.md`
