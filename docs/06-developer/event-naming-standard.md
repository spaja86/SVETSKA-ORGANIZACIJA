# Standard imenovanja događaja

## Svrha

Ovaj standard obezbeđuje da audit i domain događaji ostanu konzistentni kroz pakete, ugovore, servise i testove.

## Pravilo imenovanja

- format je `domen.akcija` ili `domen.pod-domen.akcija` kada je dodatna preciznost nužna
- koristi se poslovni jezik, ne tehnički naziv interne funkcije
- događaj opisuje šta se desilo, ne ko je emitovao događaj
- statusna promena koristi obrazac `*.status.changed` samo kada detaljniji događaj nije dovoljan

## Obavezna metadata događaja

- jedinstveni identifikator događaja
- korelacioni identifikator create toka
- identifikator resursa
- izvorna uloga ili sistemski akter
- timestamp i jurisdikcija kada je relevantna
- prethodni i novi status kada postoji tranzicija

## Događaji sa pojačanom kontrolom

- `assessment.human-review.requested`
- `assessment.decision.confirmed`
- `license.rejected`
- `license.suspended`
- `audit.exception.flagged`
- `jurisdiction.blocked`

Ovi događaji moraju imati audit trag, razlog i test pokrivenost negativnih scenarija.
