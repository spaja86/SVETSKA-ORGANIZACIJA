# License service

## Svrha

Servis za izdavanje, odbijanje, suspenziju, obnovu i istoriju statusa licence.

## Ulazi i izlazi

- ulazi: potvrđena odluka procene, regulatorna pravila, ovlašćenja aktera
- izlazi: status licence, istorija promena, audit događaji licence

## Granice odgovornosti

- menja status licence i čuva istoriju prelaza
- ne obrađuje originalne dokaze niti logiku procene
- poštuje regulatorne blokade pre svake statusne promene

## Povezani artefakti

- `packages/domain-license/`
- `packages/shared-statuses/`
- `specs/api/v1/license-contract.md`
- `tests/domain/README.md`
- `tests/audit/README.md`
