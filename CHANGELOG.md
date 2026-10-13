# Istoric versiuni

Toate schimbările importante ale aplicației, cele mai noi primele.

## [8.4c] — 13 octombrie 2026

### Adăugat
- Buton **⟳ Actualizări**: verifică, descarcă și instalează ultima versiune din GitHub Releases, cu verificarea integrității fișierului.
- **Culori pentru text**: text principal, accent (variantă, linie, etichetă) și textul etichetei, din culori rapide sau paleta completă.
- Mutarea textului cu glisoare (stânga–dreapta, sus–jos) și cu săgețile tastaturii.

## 12 octombrie 2026

### Adăugat
- **Text pe video**: artist, album, variantă, casă de discuri, dată, preț și etichetă (PRE-ORDER, ÎN STOC…), cu fade-in. Se poate muta și mări direct pe preview.
- Alegerea **numărului de discuri** înainte de detecție. Poza se încarcă întâi neatinsă, iar detecția pornește la cerere.
- Poziționarea rezultatului pe video **pe ambele axe**, cu preview pe un cadru din video.
- Mod **dreptunghi / perspectivă liberă** pentru colțurile copertei. Linia de separare disc / copertă urmează coperta.

### Schimbat
- Interfață refăcută: imaginea se potrivește automat în fereastră, previzualizări pe tab-uri, pași numerotați, panou compact pentru laptopuri de 14".

### Reparat
- Distorsionarea marginilor copertei după detecție. Poza originală nu mai e modificată deloc.
- Mânerele liniei de separare acopereau colțurile din dreapta ale copertei.
- Discuri false „ascunse” sub copertă care adăugau fundal alb pe margini.

## 11 octombrie 2026

### Adăugat
- Slider și preview pentru poziția pe verticală a copertei pe video.

### Reparat
- Pe pozele mici (screenshot-uri, imagini de pe site-uri) al doilea disc nu era detectat. Pragurile se adaptează acum la rezoluția pozei.

## 29 septembrie 2026

### Schimbat
- Instrucțiunile compacte în antet, mai mult spațiu pentru poză pe ecrane mici.

### Reparat
- Conturul alb rămas pe marginile discurilor în video (compunere cu transparență corectă).
- Umbra de sub copertă inclusă din greșeală în decupaj.

## 26 septembrie 2026

### Reparat
- Conturul alb pe marginile copertei și discului, provenit din fundalul pozei.

## 24 septembrie 2026

### Schimbat
- Detecție automată mai robustă: poze înclinate, coperți gatefold, discuri suprapuse.
- Prima versiune distribuită ca `.exe`.

## 7–9 septembrie 2026

### Schimbat
- Coperta și discurile se exportă împreună, exact cum apar în poză. Elimină decalajul dintre disc și copertă din video.
- Optimizări de viteză.

## 6 septembrie 2026

### Schimbat
- Temă deschisă, culori armonizate.

## 18–22 august 2026

### Adăugat
- Detecția mai multor discuri suprapuse.
- Verificarea acoperirii și editorul manual pentru corecții fine.
- Interfață grafică nouă.

## 4 august 2026

### Adăugat
- Începutul aplicației actuale: decuparea automată a copertei și discului din poza produsului și aplicarea lor pe video.

## 5 martie 2026 — Vinyl Overlay

### Adăugat
- Prima aplicație: aplicarea pe video a unei coperți peste un șablon cu discuri predefinite, cu animație slide-in.
