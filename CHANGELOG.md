# Istoric versiuni

Toate schimbările importante ale aplicației, cele mai noi primele.

## [8.8] — 16 octombrie 2026

### Adăugat
- Tab nou, **🎵 Conversie tracklist**, chiar în aplicație. Lipești un tracklist brut, apeși **Procesează** și primești lista curată, fără timpi și cu artiștii invitați la sfârșit (Feat. A & B). Logica de conversie e cea din scriptul original, neschimbată.
- Tab nou, **🖼️ Aplicare șablon**: aplici o poză pe un șablon (față sau spate), cu logo opțional, exact ca în scriptul original.
- **Salvare pentru web** în tabul de șablon: WebP (implicit, calitate 90), JPEG sau PNG, cu glisor de calitate. La pozele de produs, WebP la 90 ocupă cu ~85% mai puțin decât PNG, fără diferență vizibilă.
- Tab-uri în partea de sus: **Video editor**, **Aplicare șablon** și **Conversie tracklist**.

## [8.7] — 13 octombrie 2026 (publicat ca v8.6b)

### Reparat
- Pe unele laptopuri butonul **⟳ Actualizări** spunea „Nu mă pot conecta la GitHub”, deși internetul mergea. Windows nu avea încă certificatul de securitate folosit de GitHub. Aplicația are acum propria listă de certificate.
- Mesajele de eroare la actualizare spun acum cauza: certificat sau antivirus, conexiune expirată, fără internet.

## [8.6] — 13 octombrie 2026

### Adăugat
- Mânere pe **laturile** chenarului copertei: tragi o latură și coperta se redimensionează doar pe acea direcție.
- Buton **📂 Folder** pentru folderul de export și opțiunea de a salva și **coperta (PNG)** lângă video. După procesare, aplicația oferă să deschidă folderul.

### Schimbat
- Câmpul „Casă de discuri” devine **„Piesă”**.
- Varianta (ex. Red Vinyl) e albă, ca restul textului. Linia de sub preț a fost scoasă, iar iconițele sunt puțin mai mari.
- Poziția implicită pe video: **X 37%, Y 48,5%**.
- Folderul `out` de lângă poză conține acum doar coperta și discul. Fișierele interne (imaginea de debug și cea combinată) nu mai apar acolo.

## [8.5] — 13 octombrie 2026

### Adăugat
- **Rotirea chenarului copertei** în editor, cu un mâner deasupra copertei. Se „lipește” de 0°, 90°, 180° și 270°.
- Butonul **⟲ Îndreaptă**, care readuce chenarul drept dintr-un click.
- Iconiță pentru aplicație: fișier, fereastră și bara de activități.

### Reparat
- După o actualizare, aplicația repornea cu eroarea „Failed to load Python DLL”. Repornirea merge acum corect, începând de la această versiune.

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
