# MVP create flow ugovori

## Svrha

Definisati minimalne ugovore koje prvi implementacioni talas mora pokriti da bi create tok bio celovit, proverljiv i povezan sa audit zahtevima.

## Prioritetni ugovori

### 1. Profil korisnika
- kreiranje profila
- pregled profila
- promena statusa profila
- evidentiranje istorije promena

### 2. Dokazi i kompetencije
- unos dokaza
- povezivanje dokaza sa kompetencijama
- označavanje validnosti i porekla dokaza

### 3. Procena i rezultat
- otvaranje zahteva za procenu
- evidentiranje rezultata
- beleženje ljudske revizije i žalbe
- potvrda konačne odluke

### 4. Licenca i status
- izdavanje licence
- pregled aktivnog statusa
- obnova, suspenzija ili odbijanje

### 5. Partner i angažman
- dodela partnera ili evaluatora
- potvrda učinka ili angažmana kada je relevantno za licencu

### 6. Audit događaj
- emitovanje događaja iz svakog koraka create toka
- korelacija događaja sa korisnikom, odlukom i jurisdikcijom kada je primenljivo

## Zajednički standardi

- svaki ugovor mora imati jasan identitet resursa i životni ciklus statusa
- svaki ugovor mora definisati obavezna polja, validaciona pravila, greške i audit posledice
- osetljivi tokovi moraju navesti potrebu za ljudskom revizijom i kontrolom pristupa
- ugovori se pišu tako da ostanu interoperabilni između aplikacija, servisa i jurisdikcija
- svaki ugovor mora biti povezan sa ownership mapom, traceability matricom i odgovarajućim test slojem
