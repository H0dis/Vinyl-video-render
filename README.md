<p align="center">
  <img src="docs/banner.png" alt="Vinyl Video Render" width="100%">
</p>

<p align="center">
  <a href="https://github.com/H0dis/Vinyl-video-render/releases/latest"><img alt="Ultima versiune" src="https://img.shields.io/github/v/release/H0dis/Vinyl-video-render?label=versiune&color=3a6df0"></a>
  <img alt="Platformă" src="https://img.shields.io/badge/platform%C4%83-Windows%2010%20%2F%2011-1caa76">
</p>

Aplicație desktop pentru magazinele de viniluri: încarci poza produsului (copertă + disc pe fundal de studio), programul decupează automat coperta și discurile și le animă peste videoclipul de prezentare al magazinului, împreună cu un bloc de text cu detaliile produsului.

## Cum funcționează

```mermaid
flowchart LR
    A[📷 Poza produsului] --> B[🔍 Detecție automată<br/>copertă + discuri]
    B --> C[✏️ Ajustare în editor<br/>opțional]
    C --> D[🎬 Aplicare pe video<br/>poziție + text]
    D --> E[📼 Video final MP4]
```

1. **Încarci poza** produsului. Ea apare neatinsă în editor.
2. **Alegi câte discuri** sunt în poză (1–4) și apeși **Detectează**.
3. **Verifici și ajustezi**, dacă e nevoie: colțurile copertei, cercurile discurilor, linia de separare.
4. **Alegi videoclipul-șablon**, poziția pe video și, opțional, textul cu detaliile produsului.
5. **Procesezi.** Rezultatul e un MP4 gata de publicat.

## Funcții

| | |
|---|---|
| 🔍 **Detecție automată** | Coperta și 1–4 discuri, inclusiv poze înclinate, coperți gatefold și discuri suprapuse. Funcționează și pe poze mici (screenshot-uri, imagini de pe site). |
| 🖼️ **Poza rămâne neatinsă** | Decupajul nu modifică niciun pixel. Marginile curate se obțin doar prin transparență, deci fără contur alb pe video. |
| ✏️ **Editor manual** | Colțurile copertei în mod dreptunghi sau perspectivă liberă, cercuri mutabile și redimensionabile, linie de separare disc / copertă. |
| 🎬 **Animație pe video** | Coperta și discurile intră împreună, ca un singur obiect, exact cum apar în poză. |
| 🎚️ **Poziție cu preview** | Muți rezultatul pe orizontală și verticală direct pe un cadru din video. |
| 🔤 **Text pe video** | Artist, album, variantă, piesă, dată, preț și etichetă (implicit PRE-ORDER), cu fade-in. Se poate muta, mări și colora. |
| 💿 **Disc propriu** | Pentru pozele care vin fără disc: aplicația taie un disc și îl lipește lângă copertă, ca și cum ar ieși din ea. Reglezi cât iese și cât de mare e, cu previzualizare. |
| 🖼️ **Aplicare șablon** | Un tab pentru pozele de produs: aplici o poză pe un șablon (față sau spate), cu logo opțional, și salvezi în **WebP**, JPEG sau PNG. WebP la calitate 90 e cu ~85% mai mic decât PNG, ideal pentru un site cu multe produse. |
| 🎵 **Conversie tracklist** | Al doilea tab: lipești un tracklist brut (de pe un site de discuri) și primești lista curată, fără timpi și cu artiștii invitați formatați ca „(Feat. A & B)”. |
| ⟳ **Actualizare dintr-un click** | Butonul **Actualizări** descarcă și instalează singur ultima versiune de aici. |

## Instalare

1. Deschide pagina **[Releases](https://github.com/H0dis/Vinyl-video-render/releases/latest)**.
2. Descarcă `VinylVideoRender_Setup_<versiune>.exe` din secțiunea *Assets*.
3. Dă dublu-clic pe el. Fără nicio întrebare: apare o bară de progres, apoi aplicația pornește. Se instalează doar pentru utilizatorul tău, fără drepturi de administrator, cu scurtături pe Desktop și în meniul Start.

Dezinstalarea se face din *Setări → Aplicații*, ca la orice program.

> [!NOTE]
> Windows SmartScreen poate avertiza la prima rulare a installer-ului, pentru că aplicația nu e semnată digital. Alege *Mai multe informații → Rulează oricum*.

## Actualizări

În aplicație, butonul **⟳ Actualizări** din colțul dreapta-sus verifică dacă există o versiune nouă aici. Dacă există, descarcă installer-ul, îi verifică integritatea și îl rulează fără ferestre. Aplicația se închide, se actualizează și pornește din nou singură.

> [!TIP]
> **Treci de la 8.x la 9.x?** Apasă **⟳ Actualizări** ca de obicei. Apare o bară de progres, apoi aplicația pornește singură, iar pe Desktop apare scurtătura nouă. Exe-ul vechi de pe Desktop poate rămâne: deschide pur și simplu aplicația instalată.

Istoricul complet al modificărilor e în **[CHANGELOG.md](CHANGELOG.md)**.

## Cerințe de sistem

- Windows 10 sau 11, 64-bit
- Ecran de minim 1280 × 720
- Conexiune la internet doar pentru actualizări

## Probleme frecvente

<details>
<summary><b>Detecția găsește prea multe sau prea puține discuri</b></summary>

Alege corect numărul de discuri înainte de **Detectează**. Dacă un disc e aproape complet ascuns în poză, mută-l manual în editor: trage de centrul cercului, apoi **Aplică și exportă**.
</details>

<details>
<summary><b>Coperta e detectată puțin mai mică decât în realitate</b></summary>

Se întâmplă la coperțile cu margine foarte deschisă pe fundal alb. Trage colțul copertei. Cu „Colțuri libere” debifat, chenarul rămâne dreptunghi.
</details>

<details>
<summary><b>„Lipsește fontul HankenGrotesk.ttf”</b></summary>

Instalarea e incompletă. Descarcă ultima versiune din Releases și rulează installer-ul din nou.
</details>

<details>
<summary><b>Actualizarea nu se instalează</b></summary>

Verifică dacă antivirusul nu blochează installer-ul descărcat. Altfel, descarcă manual ultimul `VinylVideoRender_Setup_….exe` din Releases și rulează-l: setările și scurtăturile rămân.
</details>

---

<p align="center">
  © 2026 Hodis Florin · Toate drepturile rezervate · <a href="LICENSE">Licență</a> · <a href="THIRD_PARTY_NOTICES.md">Componente terțe</a>
</p>
