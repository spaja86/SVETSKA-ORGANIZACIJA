# Upravljanje promenama

## Kako se predlaže nova ideja

1. opis problema ili prilike
2. referenca na izvorni strateški, produktni ili policy dokument
3. procena sloja i domena na koji promena utiče
4. definisanje opsega, ograničenja i očekivanog ishoda
5. procena uticaja na arhitekturu, podatke, bezbednost, privatnost, audit i usklađenost
6. odluka kroz odgovarajući upravljački dokument ili ADR zapis kada je potrebna

## Jedinstveni lifecycle promene

1. predlog
2. analiza uticaja
3. odluka
4. specifikacija domena, statusa i interfejsa
5. mapiranje testova, audita i regulatornih kontrola
6. validacija spremnosti
7. implementacija ili otvaranje skeleta
8. verifikacija i release odluka

## Ko odobrava promene

- strateške promene: globalni upravljački sloj
- operativne promene: odgovorni operativni vlasnici
- policy promene: vlasnici politika, bezbednosti i usklađenosti
- tehničke promene: tehnički vlasnici uz proveru uticaja na arhitekturu i politike

## Obavezne tačke pregleda

- bezbednost i privatnost kada promena utiče na identitet, dokaze, procenu, licence ili integracije
- audit kada promena uvodi novu odluku, status, događaj ili KPI signal
- regulatorna usklađenost kada promena zavisi od jurisdikcije, sektora ili lokalnih pravila
- produktna potvrda kada promena širi MVP opseg ili menja korisnički tok
- test posledice kada promena utiče na ugovor, deljeni model ili granicu servisa

## Istorija odluka

- velike tehničke odluke ulaze u ADR
- promene pravila ostaju u odgovarajućim dokumentima iz sloja `docs/04-policies/`
- promene vizije i prioriteta ostaju u dokumentima iz slojeva `docs/01-foundation/` i `docs/03-product/`
- release odluke i kontrolne tačke se proveravaju kroz `release-gates.md`
