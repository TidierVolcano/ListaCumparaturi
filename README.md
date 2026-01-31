# 🛒 Lista de Cumpărături Smart

## Caracteristici Noi ✨

### 1. **Optimizată pentru iOS** 📱
- PWA (Progressive Web App) - poate fi instalată ca aplicație nativă
- Gesture swipe pentru ștergere (iOS-friendly)
- Safe area support pentru iPhone X și modele mai noi
- Haptic feedback și animații fluide
- Dark mode automat pentru economisire baterie

### 2. **Sincronizare în Timp Real** 🔄
- Share prin WhatsApp, Email sau orice altă platformă
- Link de sincronizare pentru colaborare în timp real
- Modificările se propagă instant la toți utilizatorii
- Funcționează offline și sincronizează când revine conexiunea

### 3. **Acces Rapid la Lista Finală** 📋
- Tab persistent pentru "Lista de Cumpărături"
- Vizualizare organizată pe magazine
- Badge cu numărul de produse în listă
- Tranziții rapide între secțiuni

### 4. **Exclude Produse** 🚫
- Marchează produse ca "excluse" permanent din categorii
- Produsele excluse nu apar în sugestii
- Perfect pentru alergii sau preferințe alimentare
- Vizualizare instant a produselor excluse în statistici

### 5. **Cantități și Gestiune Avansată** 📊
- Adaugă cantități la fiecare produs (ex: Lapte x3)
- Butoane +/- pentru ajustare rapidă
- Listă organizată automat pe magazine
- Statistici detaliate (total, cumpărate, rămase)

### 6. **Multe Alte Îmbunătățiri** 🎯
- **Dark Mode** - economie baterie și confort vizual
- **Liste Multiple** - pentru diferite ocazii (săptămânal, party, etc.)
- **Swipe to Delete** - gesture iOS pentru ștergere rapidă
- **Export/Import** - backup și restaurare liste
- **Notificări** - pentru produse importante
- **Instalare PWA** - funcționează ca aplicație nativă
- **Offline Mode** - folosește lista fără internet
- **Statistici în Timp Real** - vezi progresul instant

## Instalare ca Aplicație iOS 📲

### Pas 1: Deschide în Safari
1. Deschide `lista_cumparaturi_smart.html` în **Safari** (nu Chrome/Firefox)
2. Apasă butonul de "Share" (pătratul cu săgeată în sus)
3. Scroll down și selectează **"Add to Home Screen"**
4. Confirmă și aplicația va apărea pe ecranul principal

### Pas 2 (Opțional): Activează Notificările
1. Deschide aplicația
2. Mergi la Settings (⚙️)
3. Activează "Notificări"
4. Permite notificările când îți cere permisiunea

## Configurare Firebase (pentru Sync) 🔥

Pentru a activa sincronizarea în timp real între dispozitive:

### 1. Creează un cont Firebase
- Mergi la [Firebase Console](https://console.firebase.google.com/)
- Creează un proiect nou (FREE tier e suficient)

### 2. Activează Realtime Database
- În consola Firebase, mergi la **Build** → **Realtime Database**
- Click pe **Create Database**
- Alege "Start in test mode" (sau configurează regulile de securitate)

### 3. Obține Configurația
- Mergi la **Project Settings** (roata dințată)
- Scroll down la **Your apps** → **Web app** → Click pe icona `</>`
- Copiază obiectul `firebaseConfig`

### 4. Actualizează Codul
În fișierul `lista_cumparaturi_smart.html`, găsește această secțiune:

```javascript
// IMPORTANT: Înlocuiește cu propriul tău Firebase config
const firebaseConfig = {
    apiKey: "YOUR_API_KEY",              // ← Înlocuiește
    authDomain: "YOUR_PROJECT.firebaseapp.com",
    databaseURL: "https://YOUR_PROJECT.firebaseio.com",
    projectId: "YOUR_PROJECT",
    storageBucket: "YOUR_PROJECT.appspot.com",
    messagingSenderId: "YOUR_SENDER_ID",
    appId: "YOUR_APP_ID"
};

let useFirebase = false; // ← Schimbă în true
```

**Important:** Schimbă `useFirebase = false` în `useFirebase = true` după ce ai configurat Firebase!

## Cum să Folosești Aplicația 📖

### Gestionare Produse
1. **Tab Produse** - vezi toate produsele organizate pe categorii
2. Bifează produsele pe care vrei să le cumperi
3. Apasă **🚫** pentru a exclude permanent un produs
4. Swipe left pe produs pentru ștergere rapidă (sau apasă lung)

### Lista de Cumpărături
1. **Tab Lista** - vezi produsele selectate
2. Organizate automat pe magazine
3. Bifează produsele cumpărate
4. Ajustează cantitățile cu +/-

### Share și Colaborare
1. Apasă butonul **📤** din header
2. Alege metoda de share (WhatsApp recomandat)
3. Trimite linkul către altă persoană
4. Modificările voastre se sincronizează în timp real!

### Liste Multiple
1. Mergi la **Tab Liste**
2. Apasă **+** pentru listă nouă
3. Creează liste pentru diferite ocazii:
   - "Săptămânal" - cumpărăturile obișnuite
   - "Party" - pentru petreceri
   - "Vacanță" - pentru călătorii

### Dark Mode
1. Apasă **⚙️** (Settings)
2. Activează "Mod Întunecat"
3. Se salvează automat preferința

## Tips & Tricks 💡

### Gesture-uri iOS
- **Swipe Left** pe produs → Șterge rapid
- **Long Press** pe categorie → Editează rapid
- **Pull to Refresh** → Sincronizează datele

### Organizare Eficientă
- Exclude produsele pe care nu le cumperi niciodată
- Creează categorii personalizate pentru magazinele tale favorite
- Folosește cantități pentru produse consumabile (ex: Iaurt x4)

### Backup și Restaurare
- Export lunar pentru siguranță (Settings → Export)
- Import rapid din backup-uri (Settings → Import)
- Datele se salvează automat în browser

### Notificări Smart
- Primești reminder când intri în magazin (dacă activezi locația)
- Notificări pentru produse importante
- Control complet din Settings

## Probleme Comune 🔧

### Aplicația nu se instalează pe iPhone
- **Soluție:** Folosește exclusiv Safari, nu alte browsere
- Verifică că ai iOS 11.3 sau mai recent

### Sincronizarea nu funcționează
- **Verifică:** `useFirebase = true` în cod
- **Verifică:** Ai configurat corect Firebase
- **Verifică:** Ai conexiune la internet

### Dark Mode nu se activează
- **Soluție:** Închide și redeschide aplicația
- Settings sunt salvate în localStorage

### Datele s-au șters
- **Prevenție:** Fă export periodic
- **Recuperare:** Import din ultimul backup

## Securitate și Confidențialitate 🔒

- Datele sunt stocate LOCAL în browser (localStorage)
- Firebase Realtime Database (dacă activat) folosește reguli de securitate
- Nu stocăm date personale
- Share link-urile conțin doar datele listei (nu informații personale)

## Actualizări Viitoare 🚀

Planuri pentru următoarele versiuni:
- [ ] Scanare coduri de bare
- [ ] Integrare cu magazine online
- [ ] Sugestii automate bazate pe istoric
- [ ] Statistici de cheltuieli
- [ ] Reminder-uri inteligente
- [ ] Widget pentru ecranul principal iOS

## Suport 💬

Pentru probleme sau sugestii:
- Creează un Issue pe GitHub
- Sau contactează-mă direct

## Licență 📄

MIT License - folosește liber și modifică după preferințe!

---

**Enjoy shopping smart! 🛒✨**
