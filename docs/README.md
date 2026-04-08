# Dokumentacija - SVETSKA ORGANIZACIJA

Dobrodošli u dokumentaciju za platformu SVETSKE ORGANIZACIJE.

## Sadržaj

1. [Uvod](#uvod)
2. [Instalacija](#instalacija)
3. [Struktura projekta](#struktura-projekta)
4. [Razvoj](#razvoj)
5. [Deployment](#deployment)
6. [API Reference](#api-reference)

## Uvod

SVETSKA ORGANIZACIJA je moderna web platforma kreirana sa ciljem unapređenja kvaliteta života za sve ljude na planeti. Platforma je razvljena korišćenjem najnovijih web tehnologija i best practices.

### Ciljevi platforme

- Globalna dostupnost
- Jednostavnost korišćenja
- Pristupačnost za sve korisnike
- Mobilna responzivnost
- Brz učitavanje

## Instalacija

### Predsuslovi

- Moderan web browser (Chrome, Firefox, Safari, Edge)
- Git (za kloniranje repozitorijuma)
- Text editor (VS Code, Sublime Text, itd.)

### Lokalna instalacija

```bash
# Klonirajte repozitorijum
git clone https://github.com/spaja86/SVETSKA-ORGANIZACIJA.git

# Uđite u direktorijum
cd SVETSKA-ORGANIZACIJA

# Otvorite index.html u browseru
open index.html  # macOS
start index.html # Windows
xdg-open index.html # Linux
```

## Struktura projekta

```
SVETSKA-ORGANIZACIJA/
│
├── index.html              # Glavna HTML stranica
│
├── styles/
│   └── main.css           # Glavni CSS fajl sa stilovima
│
├── scripts/
│   └── main.js            # Glavni JavaScript fajl
│
├── assets/                # Slike, ikone i drugi mediji
│   ├── images/
│   └── favicon.png
│
├── docs/                  # Dokumentacija
│   └── README.md
│
├── CONTRIBUTING.md        # Vodič za doprinosioce
├── LICENSE               # MIT licenca
└── README.md            # Glavna README stranica
```

## Razvoj

### HTML Struktura

Platforma koristi semantički HTML5:
- `<header>` - Navigacija
- `<main>` - Glavni sadržaj
- `<section>` - Različite sekcije stranice
- `<footer>` - Podnožje sajta

### CSS Stilovi

CSS je organizovan po sekcijama:
- Reset stilovi
- CSS promenljive (`:root`)
- Komponente
- Responsive Media Queries

#### CSS Promenljive

```css
:root {
    --primary-color: #2563eb;
    --secondary-color: #1e40af;
    --accent-color: #f59e0b;
    --text-color: #1f2937;
    /* ... */
}
```

### JavaScript Funkcionalnosti

Glavni JavaScript fajl sadrži:

1. **Mobile Menu Toggle** - Hamburger meni za mobilne uređaje
2. **Smooth Scrolling** - Glatko skrolovanje do sekcija
3. **Contact Form** - Obrada kontakt forme
4. **Scroll Animations** - Animacije pri skrolovanju
5. **Active Navigation** - Highlighting aktivnog linka

## Deployment

### GitHub Pages

1. Idite na Settings u GitHub repozitorijumu
2. U sekciji "Pages":
   - Source: Deploy from a branch
   - Branch: main
   - Folder: / (root)
3. Kliknite Save

Sajt će biti dostupan na: `https://spaja86.github.io/SVETSKA-ORGANIZACIJA/`

### Netlify

1. Povežite GitHub repozitorijum sa Netlify
2. Build settings:
   - Build command: (prazno)
   - Publish directory: `/`
3. Deploy

### Vercel

```bash
# Instalacija Vercel CLI
npm i -g vercel

# Deploy
vercel
```

## API Reference

### Kontakt forma

Kontakt forma trenutno koristi JavaScript validaciju i console logging. Za production okruženje, potrebno je implementirati backend endpoint.

#### Primer integracije

```javascript
contactForm.addEventListener('submit', async (e) => {
    e.preventDefault();
    
    const formData = {
        name: document.getElementById('name').value,
        email: document.getElementById('email').value,
        message: document.getElementById('message').value
    };

    try {
        const response = await fetch('/api/contact', {
            method: 'POST',
            headers: {
                'Content-Type': 'application/json',
            },
            body: JSON.stringify(formData)
        });
        
        if (response.ok) {
            alert('Poruka poslata!');
            contactForm.reset();
        }
    } catch (error) {
        console.error('Greška:', error);
    }
});
```

## Customizacija

### Izmena boja

Promenite vrednosti CSS promenljivih u `styles/main.css`:

```css
:root {
    --primary-color: #your-color;
    --secondary-color: #your-color;
    /* ... */
}
```

### Dodavanje novih sekcija

1. Dodajte HTML sekciju u `index.html`
2. Kreirajte CSS stilove u `styles/main.css`
3. Dodajte link u navigaciju

### Dodavanje animacija

Koristite Intersection Observer API za scroll animacije:

```javascript
const observer = new IntersectionObserver((entries) => {
    entries.forEach(entry => {
        if (entry.isIntersecting) {
            entry.target.classList.add('animate');
        }
    });
});
```

## Pristupačnost

Platforma prati WCAG 2.1 smernice:
- Semantički HTML
- ARIA labels
- Keyboard navigacija
- Dovoljan kontrast boja
- Alt tekstovi za slike

## Performance

### Optimizacije

- Minimalni JavaScript bundle
- CSS Grid i Flexbox za layout
- Lazy loading slika (kada se dodaju)
- Optimizovane slike

### Testiranje

```bash
# Lighthouse audit
npx lighthouse https://spaja86.github.io/SVETSKA-ORGANIZACIJA/

# HTML validacija
https://validator.w3.org/
```

## Browser podrška

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers

## Troubleshooting

### Problem: Stilovi se ne učitavaju

**Rešenje:** Proverite putanje do CSS fajlova i da li su fajlovi pravilno sačuvani.

### Problem: JavaScript ne radi

**Rešenje:** Otvorite Developer Console (F12) i proverite da li ima grešaka.

### Problem: Mobilni meni ne radi

**Rešenje:** Proverite da li je JavaScript učitan i da li postoje konflikti sa drugim skriptama.

## Kontakt i podrška

Za pitanja i pomoć:
- Email: support@svetska-organizacija.org
- GitHub Issues: https://github.com/spaja86/SVETSKA-ORGANIZACIJA/issues

---

**SVETSKA ORGANIZACIJA** - Za dobrobit čovečanstva 🌍
