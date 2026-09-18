# Profile identity service

## Svrha

Servis za profil, identitet i dokaze kao ulazni sloj create toka.

## Ulazi i izlazi

- ulazi: profilni podaci, identitet, dokazi, korekcije korisnika
- izlazi: status profila, evidencija dokaza, događaji profila i validacioni ishodi

## Granice odgovornosti

- upravlja profilom, identitetom i dokazima
- ne donosi konačnu odluku procene ili licence
- ne redefiniše zajedničke modele van `packages/domain-profile/`

## Povezani artefakti

- `packages/domain-profile/`
- `packages/shared-validation/`
- `specs/api/v1/profile-contract.md`
- `specs/api/v1/evidence-contract.md`
- `tests/domain/README.md`
