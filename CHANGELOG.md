# Istoric versiuni

Toate schimbările importante ale aplicației, cele mai noi primele.

## [9.1] — 30 octombrie 2026

Prima versiune publicată din seria 9. Versiunea 9.0 a fost doar de test și n-a fost publicată.

### Adăugat
- Video editorul deschide și poze **WebP**, inclusiv cu fundal transparent. Zonele transparente sunt tratate ca fundal alb de studio.

### Schimbat
- Aplicația vine acum cu **installer** (`VinylVideoRender_Setup_9.1.exe`). Nu pune nicio întrebare: dublu-clic, bară de progres, iar aplicația pornește. Se instalează pentru utilizatorul curent, fără drepturi de administrator, și pune scurtături pe Desktop și în meniul Start. Exe-ul nu se mai dezarhivează singur în folderul temporar la fiecare pornire. Antivirusurile considerau asta suspect, iar aplicația pornește acum mai repede.
- Exe-ul are acum informații de versiune și autor (Proprietăți → Detalii).
- Actualizarea automată descarcă installer-ul, îl rulează fără ferestre și repornește aplicația.
- Pozele mari, făcute cu telefonul, se procesează mult mai repede și cu mult mai puțină memorie. O poză de 12 MP durează ~5 s în loc de ~30 s și folosește ~0,7 GB de memorie în loc de ~2,6 GB. Coperta și discul se exportă tot la rezoluția originală.
- Ferestrele **🎚 Poziție**, **✏️ Text** și **💿 Disc** nu mai blochează fereastra principală. Un al doilea clic aduce în față fereastra deja deschisă, în loc să deschidă încă una.
- **Aplică și exportă** lucrează pe fundal, iar fereastra nu mai îngheață la pozele mari.
- Pe ecranele mici, preview-ul din dreapta se micșorează ca butonul **▶ Procesează video** să rămână vizibil.

### Reparat
- La o poză complet uniformă, fără niciun obiect, detecția rula la nesfârșit și butoanele rămâneau blocate.
- Numele de fișier cu caractere interzise în Windows (`: ? * " < > |`), cu nume rezervate (`CON`, `NUL`…) sau foarte lungi dădeau un video gol de 0 KB sau o eroare tehnică. Numele se corectează acum automat.
- Un video existent cu același nume se suprascria fără întrebare. Acum aplicația întreabă.
- O copertă trasă greșit în editor (colțuri strânse într-un punct, încrucișate sau scoase din poză) se exporta ca imagine goală. Acum exportul se oprește, cu explicație.
- Dacă GitHub sau rețeaua trimiteau un răspuns neașteptat, de exemplu pagina de login a unui Wi-Fi public, butonul **⟳ Actualizări** rămânea blocat pe „Se verifică…”.
- Versiunea publicată ca v8.9 raporta în aplicație 8.8 și oferea la nesfârșit aceeași actualizare.

## [8.8] — 16 octombrie 2026

### Adăugat
- Tab nou, **🎵 Conversie tracklist**, chiar în aplicație. Lipești un tracklist brut, apeși **Procesează** și primești lista curată, fără timpi și cu artiștii invitați la sfârșit (Feat. A & B). Logica de conversie e cea din scriptul original, neschimbată.
- Tab nou, **🖼️ Aplicare șablon**: aplici o poză pe un șablon (față sau spate), cu logo opțional, exact ca în scriptul original.
- **Salvare pentru web** în tabul de șablon: WebP (implicit, calitate 90), JPEG sau PNG, cu glisor de calitate. La pozele de produs, WebP la 90 ocupă cu ~85% mai puțin decât PNG, fără diferență vizibilă.
- Tab-uri în partea de sus: **Video editor**, **Aplicare șablon** și **Conversie tracklist**.
- Buton **💿 Disc** pentru pozele care vin fără disc: taie un disc (implicit „vinyl overlay”, inclus în aplicație) și îl lipește lângă copertă, ca și cum ar ieși din ea. Poți alege cât iese din copertă (50% = jumătate) și cât de mare e, cu previzualizare, sau poți alege alt disc.
- Opțiunea **0** la „Discuri în poză”: detectează doar coperta, pentru pozele fără disc.
- Dacă poza pare să nu aibă disc, aplicația întreabă dacă folosește doar coperta, ca să poți adăuga un disc propriu.

### Schimbat
- Nu se mai salvează fișiere lângă poze (folderul `out`). Coperta, discul și imaginea combinată stau într-un folder temporar, șters la închiderea aplicației. Am scos bifa „Salvează și coperta lângă video” și butonul care deschidea folderul de rezultate.

### Reparat
- Diacriticele (Ă, Â, Î, Ș, Ț) de pe prima linie a textului de pe video apăreau tăiate sus. Acum se văd întregi, iar textul rămâne unde era.
- Pozele, videoclipurile și șabloanele din foldere cu litere românești în nume (ș, ț, ă…) se citesc și se salvează corect. Înainte, aplicația nu le deschidea sau nu salva nimic, fără mesaj.

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
