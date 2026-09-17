# Upravljanje promenama

## Kako se predlaže nova ideja

1. opis problema ili prilike
2. procena sloja na koji utiče
3. definisanje opsega i ograničenja
4. procena uticaja na arhitekturu, podatke i usklađenost
5. odluka kroz odgovarajući upravljački dokument ili ADR zapis

## Razvojni lifecycle

1. predlog
2. analiza uticaja
3. ADR ili upravljačka odluka
4. specifikacija domena i interfejsa
5. validacija spremnosti
6. implementacija
7. verifikacija i release odluka

## Ko odobrava promene

- strateške promene: globalni upravljački sloj
- operativne promene: odgovorni operativni vlasnici
- tehničke promene: tehnički vlasnici uz proveru uticaja na arhitekturu i politike

## Obavezne tačke pregleda

- bezbednost i privatnost kada promena utiče na identitet, procenu, licence ili integracije
- audit kada promena uvodi novu odluku, status ili osetljiv događaj
- regulatorna usklađenost kada promena zavisi od jurisdikcije, sektora ili lokalnih pravila
- produktna potvrda kada promena širi MVP opseg ili menja korisnički tok

## Istorija odluka

- velike tehničke odluke ulaze u ADR
- promene pravila ostaju u odgovarajućim dokumentima iz sloja `docs/04-policies/`
- promene vizije i prioriteta ostaju u dokumentima iz slojeva `docs/01-foundation/` i `docs/03-product/`
