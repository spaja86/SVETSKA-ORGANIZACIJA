# Vlasništvo i release model

## Vlasništvo po slojevima

- `docs/01-foundation/` i `docs/03-product/` — strateški i produktni vlasnici
- `docs/04-policies/` — vlasnici politika, bezbednosti i usklađenosti
- `docs/06-developer/`, `specs/api/`, `packages/`, `services/`, `apps/`, `tests/` — tehnički vlasnici uz obaveznu proveru uticaja na politike

## Vlasništvo po budućim artefaktima

Svaki novi artefakt mora imati:

- vlasnika odluke
- vlasnika isporuke
- svrhu
- granice odgovornosti
- povezane izvorne dokumente
- vezu sa testovima i audit zahtevima kada je relevantno

Detaljna mapa domena i budućih servisnih granica održava se u `create-domain-ownership-map.md`.

## Tipovi promena

- mala promena — ograničen uticaj, bez promene arhitektonskog smera i bez proširenja produktnog opsega
- produktna promena — menja korisnički tok, MVP granice ili prioritete funkcionalnosti
- arhitektonska promena — menja granice modula, ugovore, odgovornosti servisa ili pravila interoperabilnosti
- kontrolna promena — menja audit, bezbednosna, privatnosna ili regulatorna pravila

## Release osnov

Pre ulaska u implementacioni talas promena mora:

- biti spremna prema `./definition-of-ready.md`
- imati validnu vezu sa politikama i zahtevima iz domena
- imati definisane API i test posledice kada utiče na interfejse ili tokove
- imati potvrđen audit i pristupni model za osetljive podatke i odluke

Pre ulaska u MVP izdanje promena mora:

- zadovoljiti kriterijume završetka
- imati usaglašene ugovore i domenske modele
- imati scenarije za pozitivne, negativne i granične tokove
- imati plan praćenja KPI, žalbi i audit događaja za produkciono ponašanje

Detaljna release vrata održavaju se u `release-gates.md`.
