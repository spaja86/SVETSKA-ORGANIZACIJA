# Definition of Done

Promena je završena tek kada je dokumentacioni, ugovorni ili implementacioni trag zatvoren i proverljiv.

## Obavezni uslovi završetka

- cilj, opseg i ograničenja promene ostaju jasni i proverljivi u finalnom artefaktu
- postoji veza sa izvornim dokumentom, domenom i relevantnom odlukom ili ADR-om kada je potreban
- artefakt je na pravom mestu u strukturi repozitorijuma
- povezane API, paketne, servisne, aplikativne i test posledice su ažurirane kada su relevantne
- audit, bezbednost, privatnost i regulatorne kontrole su dokumentovane ili ugrađene kada promena utiče na osetljive tokove

## Dodatni uslovi za ugovore i skelet

- ugovori imaju definisane ulaze, izlaze, validacije, greške i audit posledice
- skelet direktorijuma ima jasno naznačenu svrhu, vlasništvo i granice odgovornosti
- statusi i događaji su usklađeni sa `domain-status-and-events-catalog.md`
- test scenariji su povezani sa traceability matricom i prioritetnim poslovnim tokom

## Dodatni uslovi za implementacioni talas

- ispunjeni su kriterijumi prihvatanja za pozitivne, negativne i granične scenarije
- definisan je minimalni signal za audit, KPI i operativno praćenje
- promena prolazi kroz odgovarajuća release vrata definisana u `release-gates.md`
- završetak ne uvodi protivrečnost sa strategijom, produktom ili policy slojem
