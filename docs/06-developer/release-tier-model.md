# Model release nivoa

## Svrha

Ovaj model određuje minimalni nivo kontrole koji promena mora proći pre daljeg zaključavanja ili izdanja.

## Nivoi promena

| Nivo | Opis | Minimalne kontrole |
| --- | --- | --- |
| Tier 1 — dokumentacioni | menja navigaciju, opis, source-of-truth ili governance objašnjenje | Gate 1 i Gate 5 |
| Tier 2 — contract | menja ugovore, greške, statuse ili metadata pravila | Gate 1, 2, 3 i 5 |
| Tier 3 — domain | menja ownership, modele, zavisnosti ili servisne granice | Gate 1, 2, 3, 4 i 5 |
| Tier 4 — implementation | uvodi izvršni skelet ili runtime ponašanje | svi gate-ovi uključujući Gate 6 kada utiče na MVP tok |

## Pravilo korišćenja

- svaka promena mora eksplicitno navesti svoj nivo ili dominantni nivo kada kombinuje više slojeva
- viši nivo ne preskače niže kontrole
- kada postoji sumnja, koristi se stroži nivo kontrole
