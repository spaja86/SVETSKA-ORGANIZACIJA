# DEPLOYMENT GUIDE - SVETSKA ORGANIZACIJA

Ovaj dokument pruža instrukcije za deployment platforme SVETSKA ORGANIZACIJA.

## 🚀 Brzi početak

Platforma je spremna za deployment bez dodatne konfiguracije. Sve potrebne datoteke su već prisutne.

## 📦 Deployment opcije

### Opcija 1: GitHub Pages (Preporučeno)

GitHub Pages je besplatna hosting platforma idealna za statičke web stranice.

#### Koraci:

1. Idite na vaš GitHub repozitorijum: https://github.com/spaja86/SVETSKA-ORGANIZACIJA
2. Kliknite na **Settings** (Podešavanja)
3. U levom meniju izaberite **Pages**
4. Pod "Build and deployment":
   - **Source**: Deploy from a branch
   - **Branch**: Izaberite `main` (ili trenutni branch)
   - **Folder**: `/ (root)`
5. Kliknite **Save**
6. Sačekajte nekoliko minuta dok GitHub ne izgradi sajt
7. Vaš sajt će biti dostupan na: `https://spaja86.github.io/SVETSKA-ORGANIZACIJA/`

#### Custom domain (opciono):

Ako želite da koristite custom domain (npr. www.svetska-organizacija.org):

1. U sekciji "Custom domain" unesite vaš domen
2. U DNS podešavanjima vašeg domena dodajte:
   - CNAME zapis: `www` → `spaja86.github.io`
   - A zapisi za apex domen (svetska-organizacija.org):
     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```

### Opcija 2: Netlify

Netlify nudi automatski deployment, HTTPS, i CDN.

#### Koraci:

1. Idite na https://www.netlify.com/
2. Kliknite **Sign up** (ako nemate nalog) ili **Log in**
3. Kliknite **New site from Git**
4. Izaberite **GitHub** i autorizujte Netlify
5. Izaberite repozitorijum `SVETSKA-ORGANIZACIJA`
6. Build settings:
   - **Build command**: (ostavite prazno)
   - **Publish directory**: `/` (root)
7. Kliknite **Deploy site**
8. Sajt će biti dostupan na automatski generisanom URL-u (npr. `svetska-organizacija.netlify.app`)

#### Custom domain na Netlify:

1. U Netlify dashboard-u, idite na **Domain settings**
2. Kliknite **Add custom domain**
3. Pratite instrukcije za konfiguraciju DNS-a

### Opcija 3: Vercel

Vercel je još jedna odlična platforma za deployment.

#### Koraci:

1. Instalirajte Vercel CLI:
   ```bash
   npm i -g vercel
   ```

2. U terminalu, uđite u direktorijum projekta:
   ```bash
   cd SVETSKA-ORGANIZACIJA
   ```

3. Pokrenite deployment:
   ```bash
   vercel
   ```

4. Pratite instrukcije na ekranu

Alternativno, možete koristiti Vercel web interfejs:
1. Idite na https://vercel.com/
2. Povežite GitHub nalog
3. Importujte repozitorijum
4. Deploy će biti automatski

### Opcija 4: Lokalni server (za testiranje)

Za lokalno testiranje:

```bash
# Python 3
python3 -m http.server 8080

# Node.js (ako imate instaliran npx)
npx http-server -p 8080

# PHP
php -S localhost:8080
```

Zatim otvorite browser i idite na `http://localhost:8080`

## 🔧 Pre deployment-a

### Provera validnosti koda:

```bash
# Provera JavaScript sintakse
node -c scripts/main.js

# Provera HTML validnosti (online)
# Otvorite https://validator.w3.org/ i unesite URL ili upload fajlove
```

### Performance optimizacija:

Pre production deployment-a, razmotrite:

1. **Minifikacija CSS i JavaScript**:
   ```bash
   # Koristite online alate ili build tools
   # npr. https://www.minifier.org/
   ```

2. **Optimizacija slika** (kada ih dodate):
   - Kompresujte slike (JPEG, PNG, WebP)
   - Koristite responsive images sa `srcset`

3. **Dodavanje favicon-a**:
   - Napravite favicon.png i stavite u `/assets/`
   - Ili kreirajte pomoću https://favicon.io/

## 📊 Monitoring i Analytics

### Google Analytics (opciono):

Dodajte Google Analytics u `<head>` sekciju svih HTML stranica:

```html
<!-- Google Analytics -->
<script async src="https://www.googletagmanager.com/gtag/js?id=GA_MEASUREMENT_ID"></script>
<script>
  window.dataLayer = window.dataLayer || [];
  function gtag(){dataLayer.push(arguments);}
  gtag('js', new Date());
  gtag('config', 'GA_MEASUREMENT_ID');
</script>
```

## 🔒 Sigurnost

### HTTPS

Sve preporučene platforme (GitHub Pages, Netlify, Vercel) automatski pružaju HTTPS.

### Content Security Policy

Razmotrite dodavanje CSP headera za dodatnu sigurnost:

```html
<meta http-equiv="Content-Security-Policy" content="default-src 'self'; script-src 'self' 'unsafe-inline'; style-src 'self' 'unsafe-inline';">
```

## 🌍 SEO Optimizacija

Pre deployment-a, proverite:

- ✅ Meta tags su postavljeni (title, description)
- ✅ Open Graph tags za društvene mreže
- ✅ Sitemap.xml (možete kreirati pomoću online alata)
- ✅ robots.txt

Dodajte `robots.txt` u root direktorijum:

```txt
User-agent: *
Allow: /
Sitemap: https://spaja86.github.io/SVETSKA-ORGANIZACIJA/sitemap.xml
```

## 📱 PWA (Progressive Web App) - Opciono

`manifest.json` fajl je već kreiran. Za potpunu PWA funkcionalnost, dodajte Service Worker:

1. Kreirajte `sw.js` fajl
2. Registrujte ga u `scripts/main.js`

## 🎉 Gotovo!

Nakon deployment-a:

1. ✅ Testirajte sve stranice
2. ✅ Proverite responsivnost na različitim uređajima
3. ✅ Testirajte sve linkove i forme
4. ✅ Proverite performanse (Lighthouse audit)

## 🆘 Pomoć

Ako imate problema sa deployment-om:

- Proverite GitHub Pages dokumentaciju: https://docs.github.com/en/pages
- Netlify docs: https://docs.netlify.com/
- Vercel docs: https://vercel.com/docs
- Kreirajte Issue na GitHub-u: https://github.com/spaja86/SVETSKA-ORGANIZACIJA/issues

---

**SVETSKA ORGANIZACIJA** - Vaš sajt je spreman da menja svet! 🌍✨
