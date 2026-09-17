# Servisi

Ovde će se nalaziti budući backend servisi, integracioni sloj, obrada događaja, audit funkcije i regulatorni servisi.

## Prioritetni prvi artefakti

- servis profila i identiteta
- servis procene i validacije
- servis licenci i obnova
- servis partnera i angažmana
- audit servis i reporting servis
- regulatorni servis za lokalna pravila i ograničenja

## Pravilo granica

- servisi nose izvršavanje domena i integracija, ali ne redefinišu deljene modele van `packages/`
- svaki servis mora imati eksplicitne ulaze, izlaze, statuse i audit događaje
- regulatorna pravila i kontrole pristupa moraju biti ugrađeni u dizajn servisa od početka
