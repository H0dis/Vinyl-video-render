# Cum public o versiune nouă

Ghid pentru autor. Butonul **⟳ Actualizări** din aplicație citește ultimul *Release* din acest repository, deci o versiune nouă ajunge la utilizatori în momentul în care e publicată aici.

## 1. Mărește numărul versiunii

În `src/updater.py`:

```python
CURRENT_VERSION = "9.0"
```

De aici se iau automat textul de sub titlul aplicației (`©Hodis Florin v9.0`), informațiile de versiune din exe și numele installer-ului. Ordinea versiunilor: `8.4c` < `8.4d` < `8.5` < `9.0` < `9.0a`.

## 2. Construiește installer-ul

O singură dată, instalează Inno Setup:

```powershell
winget install JRSoftware.InnoSetup
```

Apoi, la fiecare versiune, din folderul proiectului:

```powershell
powershell -ExecutionPolicy Bypass -File packaging\build.ps1
```

Scriptul face două lucruri:
- rulează PyInstaller în modul **folder** (onedir, cu fonturile, discurile, iconița și certificatele incluse);
- împachetează folderul cu Inno Setup.

La final afișează calea installer-ului (`build\<versiune>\VinylVideoRender_Setup_<versiune>.exe`), mărimea și amprenta SHA256.

Instalează-l o dată și verifică rapid: încarcă o poză, apasă **Detectează** și deschide **✏️ Text**.

> [!IMPORTANT]
> Nu mai folosi auto-py-to-exe cu **One File**. Un exe onefile se dezarhivează singur în folderul temporar la fiecare pornire, iar antivirusurile îl consideră suspect din cauza asta.

## 3. Publică pe GitHub

1. Pe pagina repository-ului: **Releases → Draft a new release**.
2. **Choose a tag**: scrie `v9.0` (exact versiunea, cu `v` în față) și apasă *Create new tag*.
3. **Title**: de exemplu `Versiunea 9.0`.
4. **Descriere**: ce e nou, în câteva rânduri. Textul apare utilizatorului în fereastra de actualizare.
5. Trage **doar installer-ul** (`VinylVideoRender_Setup_….exe`) în zona **Attach binaries** și așteaptă să se încarce complet. Nu atașa și alte `.exe`: versiunile 8.x iau orice `.exe` găsesc.
6. **Publish release**.

## 4. Actualizează CHANGELOG.md

Adaugă o secțiune nouă sus, cu data și ce s-a schimbat.

## Verificare

Pe un calculator cu versiunea veche: **⟳ Actualizări** trebuie să arate noua versiune. După instalare, aplicația pornește singură, iar sub titlu apare noul număr.

De la 8.x la 9.0, prima actualizare arată o bară de progres, apoi aplicația pornește din locul nou. Exe-ul 8.x rămas pe Desktop devine installer-ul 9.0: dacă e deschis din nou, vede că e deja instalată o versiune la fel de nouă sau mai nouă și doar pornește aplicația. De la 9.0 încolo, actualizările se instalează fără ferestre.
