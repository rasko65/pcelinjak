# Dnevnik pčelinjaka

Web aplikacija za vođenje dnevnika aktivnosti po košnicama: sirup, pogača, lek protiv varoe, pregledi, matica, ramovi i nastavci, vrcanje meda.

- Radi na telefonu kao aplikacija (ikonica na početnom ekranu).
- Radi i bez interneta, pa je upotrebljiva i na pčelinjaku bez signala.
- Podaci se čuvaju na samom telefonu (localStorage), bez servera i naloga.
- Rezervna kopija (.json) i izvoz za Excel (.csv) nalaze se u meniju **Podešavanja**.

## Postavljanje na GitHub Pages

1. Na github.com napravi novi repozitorijum, na primer `pcelinjak`. Može biti javan.
2. Klikni **Add file → Upload files** i prevuci sve fajlove iz ovog foldera, pa **Commit changes**.
3. Idi na **Settings → Pages**, pa podesi:
   - **Source:** Deploy from a branch
   - **Branch:** `main`, folder `/ (root)`
   - Klikni **Save**.
4. Posle 1 do 2 minuta aplikacija je dostupna na:
   `https://TVOJE-KORISNIČKO-IME.github.io/pcelinjak/`

## Instalacija na telefonu

1. Otvori gornju adresu u pregledaču na telefonu.
2. Dodaj je na početni ekran:
   - **Android (Chrome):** meni ⋮ → **Instaliraj aplikaciju** ili **Dodaj na početni ekran**
   - **iPhone (Safari):** dugme za deljenje → **Dodaj na početni ekran**

## Važno o podacima

Unosi postoje samo na telefonu na kome su napravljeni. Ne dele se sa računarom.

Povremeno napravi rezervnu kopiju: **Podešavanja → Sačuvaj kopiju**, pa taj fajl pošalji sebi mejlom ili sačuvaj na Drive.

Podaci se gube ako obrišeš podatke pregledača ili promeniš telefon. Tada ih vraćaš preko **Podešavanja → Vrati iz kopije**.

## Izmene

Kada izmeniš `index.html`, u fajlu `sw.js` povećaj verziju (`pcelinjak-v1` → `pcelinjak-v2`). Tako telefon povlači novu verziju umesto one iz keša.

## Fajlovi

| Fajl | Namena |
|---|---|
| `index.html` | cela aplikacija |
| `manifest.webmanifest` | naziv, boje i ikonice za instalaciju |
| `sw.js` | rad bez interneta |
| `icon-*.png`, `apple-touch-icon.png` | ikonice |
