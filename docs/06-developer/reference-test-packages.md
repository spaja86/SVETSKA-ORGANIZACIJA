# Referentni test paketi

## Svrha

Referentni test paketi obezbeđuju da create tok ostane proverljiv kroz vreme i kroz više implementacionih talasa.

## Prioritetni test paketi

- paket za dokumentacionu konzistentnost i navigaciju
- paket za ugovorne validacije i kompatibilnost statusa
- paket za domenska pravila profila, procene i licenci
- paket za end-to-end create tok
- paket za audit korelaciju, KPI signal i regulatorne blokade

## Pravilo održavanja

- svaki novi ugovor ili status mora imati odgovarajući test paket ili proširenje postojećeg
- negativni i granični scenariji su obavezni za osetljive tokove
- test paketi ostaju vezani za traceability matricu i release vrata
