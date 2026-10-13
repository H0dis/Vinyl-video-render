# Cum public o versiune nouă

Ghid pentru autor. Butonul **⟳ Actualizări** din aplicație citește ultimul *Release* din acest repository, deci o versiune nouă ajunge la utilizatori în momentul în care e publicată aici.

## 1. Mărește numărul versiunii

În `updater.py`:

```python
CURRENT_VERSION = "8.4d"
```

Textul de sub titlul aplicației (`©Hodis Florin v8.4d`) se ia automat de aici. Ordinea versiunilor: `8.4c` < `8.4d` < `8.5` < `9.0`.

## 2. Compilează exe-ul

În **auto-py-to-exe**:

| Câmp | Valoare |
|---|---|
| Script Location | `extract_disc_cover_gui.py` |
| Onefile | **One File** |
| Console Window | **Window Based** |
| Additional Files | **Add Folder** → folderul `fonts`, destinație `fonts` |

Apasă **CONVERT .PY TO .EXE**, apoi deschide exe-ul o dată și verifică rapid: încarcă o poză, apasă **Detectează** și deschide **✏️ Text**.

## 3. Publică pe GitHub

1. Pe pagina repository-ului: **Releases → Draft a new release**.
2. **Choose a tag**: scrie `v8.4d` (exact versiunea, cu `v` în față) și apasă *Create new tag*.
3. **Title**: de exemplu `Versiunea 8.4d`.
4. **Descriere**: ce e nou, în câteva rânduri. Textul apare utilizatorului în fereastra de actualizare.
5. Trage exe-ul în zona **Attach binaries** și așteaptă să se încarce complet.
6. **Publish release**.

## 4. Actualizează CHANGELOG.md

Adaugă o secțiune nouă sus, cu data și ce s-a schimbat.

## Verificare

Pe un calculator cu versiunea veche: **⟳ Actualizări** trebuie să arate noua versiune. După instalare, aplicația pornește singură, iar sub titlu apare noul număr.
