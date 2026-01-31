# 📱 Ghid Instalare Lista Smart pe iPhone

## Metoda 1: GitHub Pages (RECOMANDAT - 100% GRATUIT)

### Pas 1: Creează cont GitHub (dacă nu ai)
1. Mergi pe https://github.com
2. Click pe "Sign up" 
3. Creează cont gratuit

### Pas 2: Creează Repository
1. Click pe "+" (sus-dreapta) → "New repository"
2. Nume: `lista-cumparaturi` (sau orice nume vrei)
3. Selectează: ✅ Public
4. Click "Create repository"

### Pas 3: Upload Fișierele
1. Click pe "uploading an existing file"
2. Trage toate cele 4 fișiere în browser:
   - lista_cumparaturi_smart.html
   - manifest.json
   - sw.js
   - README.md
3. Click "Commit changes"

### Pas 4: Activează GitHub Pages
1. Click pe "Settings" (tab-ul din repository)
2. Scroll până la "Pages" (în meniul din stânga)
3. La "Source" → selectează "main" branch
4. Click "Save"
5. Așteaptă 1-2 minute

### Pas 5: Obține Link-ul
După 1-2 minute, vei vedea un mesaj verde:
```
Your site is live at https://username.github.io/lista-cumparaturi/
```

### Pas 6: Deschide pe iPhone
1. Pe iPhone, deschide Safari
2. Intră pe: `https://username.github.io/lista-cumparaturi/lista_cumparaturi_smart.html`
3. Click Share (pătratul cu săgeată) → "Add to Home Screen"
4. Gata! 🎉

---

## Metoda 2: Netlify (și mai simplu, fără GitHub)

### Pas 1: Mergi pe Netlify
1. Deschide: https://app.netlify.com/drop
2. NU trebuie să te loghezi!

### Pas 2: Upload Fișierele
1. Trage toate cele 4 fișiere în zona "Drag and drop"
2. Așteaptă 10 secunde
3. Vei primi un link gen: `https://random-name-123456.netlify.app`

### Pas 3: Deschide pe iPhone
1. Pe iPhone, deschide Safari
2. Intră pe linkul primit
3. Adaugă `/lista_cumparaturi_smart.html` la final
4. Share → "Add to Home Screen"

**ATENȚIE:** Link-ul Netlify free dispare după 7 zile dacă nu creezi cont!

---

## Metoda 3: Local pe Computer + iPhone (același WiFi)

### Pe Computer (Windows):

#### Pas 1: Pune toate fișierele într-un folder
```
C:\lista-smart\
  ├── lista_cumparaturi_smart.html
  ├── manifest.json
  ├── sw.js
  └── README.md
```

#### Pas 2: Rulează Server Python
1. Deschide Command Prompt în folderul acela
2. Rulează:
```cmd
python -m http.server 8000
```

Sau dacă ai Python 2:
```cmd
python -m SimpleHTTPServer 8000
```

#### Pas 3: Găsește IP-ul computerului
```cmd
ipconfig
```
Caută "IPv4 Address" (ex: 192.168.1.100)

### Pe iPhone:
1. Asigură-te că ești pe același WiFi ca PC-ul
2. Deschide Safari
3. Intră pe: `http://192.168.1.100:8000/lista_cumparaturi_smart.html`
4. Add to Home Screen

---

## Metoda 4: Rapid Test cu File Hosting

### Folosește catbox.moe (fără cont):
1. Mergi pe https://catbox.moe
2. Upload `lista_cumparaturi_smart.html`
3. Primești link direct
4. Deschide în Safari pe iPhone
5. Add to Home Screen

**LIMITARE:** Nu vei putea uploada toate fișierele (manifest, sw.js)

---

## 🏆 RECOMANDAREA MEA:

**Folosește GitHub Pages** - e gratuit, permanent, și poți actualiza ușor fișierele.

## ❓ Ai nevoie de ajutor?

Dacă întâmpini probleme la oricare din pași, spune-mi și te ajut!

Alternativ, îți pot crea un link temporar unde să testezi aplicația înainte să o instalezi.
