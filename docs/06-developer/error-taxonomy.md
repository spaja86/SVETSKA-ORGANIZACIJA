# Taksonomija grešaka

## Svrha

Ovaj dokument uvodi zajednički model grešaka za buduće API ugovore i servisne granice.

## Klase grešaka

| Klasa | Značenje | Primer posledice |
| --- | --- | --- |
| validation-error | ulaz nije potpun, dozvoljen ili dosledan | zahtev ostaje otvoren bez promene statusa |
| authorization-error | akter nema dozvolu za operaciju | događaj se beleži kao odbijen pristup |
| regulatory-block | lokalno pravilo zabranjuje nastavak toka | create korak se blokira uz razlog i jurisdikciju |
| conflict-error | resurs je u stanju koje ne dozvoljava operaciju | nema prelaza statusa bez korekcije |
| review-required | automatski nastavak nije dozvoljen bez ručne revizije | slučaj ide u `awaiting-human-review` |
| not-found | traženi resurs ili referenca ne postoji | audit beleži neuspešnu korelaciju ako utiče na tok |
| internal-integrity-error | događaj, model ili status nisu dosledni | incident signal i zaustavljanje prelaza |

## Pravilo ugovora

- svaki ugovor navodi koje klase grešaka može vratiti
- greške koje menjaju tok moraju imati audit posledicu
- `regulatory-block` i `review-required` nikada ne smeju biti svedeni na generičku grešku
- kodovi i poruke ostaju sekundarni u odnosu na poslovnu klasu greške
