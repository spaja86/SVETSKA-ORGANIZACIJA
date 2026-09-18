# Aplikacije

Ovde se nalaze planirani portali i korisničke aplikacije za create tok i naredne faze.

## Aktivni skelet

- `public-portal/` — javni portal za programe, javne informacije i izveštaje
- `user-portal/` — korisnički tokovi za profil, dokaze i status licence
- `partner-portal/` — partnerski tokovi za procenu, potvrdu učinka i angažmane
- `admin-portal/` — administrativni tokovi za audit, KPI i regulatorni nadzor

## Pravilo granica

- aplikacije orkestriraju korisničke tokove, ali ne dupliraju domenska pravila iz paketa i servisa
- osetljivi tokovi moraju jasno razlikovati korisnički, partnerski i interni pristup
- svaki novi interfejs mora navesti izvorni dokument, ciljnu ulogu i zavisne API ugovore
- create ownership, statusi i release kontrole vode se centralno kroz `docs/06-developer/README.md`
