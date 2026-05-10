# Visuell Instruktionsbok - Lövstaölets Vänner

Projektet publiceras via GitHub Pages från `main`-branchen.

Publik sida:
- `https://larswpettersson.github.io/lovstaolets-vanner-instruktionsbok/`

## Filer att jobba vidare i

- `index.html`: publik startsida med visuell steg-för-steg-guide.
- `bryggprotokoll.html`: interaktivt bryggprotokoll som räknar om ingredienser baserat på bryggvolym.

## Uppdatera `index.html`

1. Justera text, steg och bildreferenser direkt i `index.html`.
2. Behåll bildfiler i samma mapp som HTML-filen om de refereras med relativa sökvägar (t.ex. `IMG_0472.JPG`).
3. Testa lokalt genom att öppna filen i webbläsare.

Tips:
- Lägg varje bryggsteg i en egen `<section class="step">` för konsekvent layout.
- Använd befintliga CSS-klasser (`.page`, `.title`, `.step`, `.photo`) för samma utseende.

## Uppdatera `bryggprotokoll.html`

Den interaktiva skalningen styrs av JavaScript längst ned i filen:
- `baseVolume` = receptets grundvolym (liter)
- `targetVolume` = önskad ny bryggvolym (liter)
- Skalfaktor = `targetVolume / baseVolume`

För att lägga till nya ingredienser:

- Malt (kg): lägg till rad med klass `malt-amount` och attribut `data-base`.
  - Exempel: `<td class="malt-amount" data-base="1.2"></td>`
- Humle (g): lägg till rad med klass `hop-amount` och attribut `data-base`.
  - Exempel: `<td class="hop-amount" data-base="25"></td>`

Skriptet räknar automatiskt om alla dessa celler när volymfält ändras.

## Publicera ändringar

Kör i projektmappen:

```bash
git add .
git commit -m "Beskrivning av ändring"
git push
```

GitHub Pages bygger om sidan automatiskt efter push.
