# DT200G – Laboration 1.2

En responsiv webbplats för kursen **Grafisk teknik för webb**, skapad av
Maida Erovic. Temat är **Resor och stadsmiljöer**. Uppgiften utforskar
bildredigering och en sammanhållen visuell stil i skogsgrönt, gräddvitt och vitt.

Webbplatsen använder enbart semantisk HTML och CSS med systemtypsnitt.
Inga ramverk, JavaScript, npm-paket eller byggsteg behövs.

## Sidor

- [Startsida](index.html): en bred vinjettbild, introduktion och ett rutnätsgalleri
  med tre redigerade fotografier.
- [Bildredigering](bildredigering.html): original och redigerade bilder med
  beskrivningar av färgjusteringar, ändrad fasadfärg, borttaget flygplan och
  beskärning av himmel.
- [Om mig](om-mig.html): en kort presentation och ett frilagt porträtt mot grön
  bakgrund.

## Verktyg

- **Photopea:** fotoredigering och borttagning av porträttets bakgrund.
- **Figma:** formgivning av logotyp och favoritikoner.
- **HTML och CSS:** sidstruktur, tillgänglig navigation och responsiv layout.

## Mappstruktur

```text
.
├── index.html
├── bildredigering.html
├── om-mig.html
├── css/
│   └── style.css
├── images/
│   ├── logo.svg
│   ├── favicon.png
│   └── web/
│       ├── bildserie001.jpeg
│       ├── bildserie002.jpeg
│       ├── bildserie003.jpeg
│       ├── header.png
│       ├── portrait.png
│       └── favicon.ico
├── original/
│   ├── original001.jpg
│   ├── original002.jpg
│   └── original003.jpg
└── README.md
```

Webbplatsen använder de konverterade bilderna i `images/web/`.
De oanvända filerna med fel bildformat har tagits bort.
Originalfotografierna i `original/` är kvar för bildjämförelserna.
PNG-ikonen är 32 × 32 pixlar och ICO-ikonen är 16 × 16 pixlar.
Vinjettbilden är 579 × 193 pixlar och visas därför i en låg bildyta.

### Webbkopior och bildformat

De ursprungligen tillagda redigerade bilderna innehöll PSD-data trots
filändelserna JPEG och PNG. Därför exporterades webbversioner med
macOS-verktyget `sips`, innan de oanvända PSD-filerna togs bort:

- De tre fotografierna är riktiga JPEG-filer med 2000 pixlars bredd,
  bibehållna proportioner och JPEG-kvalitet 95.
- Vinjettbilden och porträttet är riktiga PNG-filer med alfakanal.
- HTML-sidorna använder kopiorna i `images/web/`. Inga nya motiv har skapats
  och inga ytterligare bildredigeringar har gjorts.

Den tidigare `favicon.ico` innehöll PNG-data snarare än en riktig ICO-fil.
En korrekt ICO-behållare med samma 16 × 16-bild har skapats som
`images/web/favicon.ico` och används på sidorna. Den oanvända filen togs bort.
`favicon.png` är en giltig PNG-fil i storleken 32 × 32 pixlar.
Originalfotografierna är giltiga JPEG-filer och logotypen är en SVG-fil.

## Visa lokalt

Öppna `index.html` direkt i en webbläsare. Ingen installation eller lokal
server behövs. Använd menyn för att besöka de andra två sidorna.

Kontrollera gärna webbplatsen med webbläsarens responsiva läge vid exempelvis
375, 768 och 1440 pixlars bredd. Navigationen radbryts på smala skärmar.
Galleriet och bildjämförelserna visas i en kolumn upp till 700 pixlars bredd.
Fotografierna behåller sina proportioner och visas i sin helhet; endast
vinjettbilden anpassas med `object-fit: cover`. På startsidan används lika
stora bildytor i formatet 4:3 med `object-fit: contain`, så att hela
fotografierna syns utan att beskäras eller sträckas. Kortens nederkanter
linjerar när de visas på samma rad.

Använd Tab för att kontrollera fokusmarkeringar och länken
”Hoppa till innehåll”. Varje sida har en markerad aktuell menylänk, logotyp
med länk till startsidan samt båda favoritikonerna.

## Publicera med GitHub Pages

1. Lägg till projektets filer i Git och skicka dem till GitHub när du själv
   är redo att publicera. Kontrollera att även bilderna följer med.
2. Öppna repots **Settings → Pages** på GitHub.
3. Välj **Deploy from a branch** under **Build and deployment**.
4. Välj grenen som innehåller webbplatsen och mappen **/ (root)**. Spara.
5. Vänta tills publiceringen är klar. Den riktiga webbplatsadressen visas
   på samma inställningssida.

Alla interna sökvägar är relativa så att webbplatsen även fungerar under
ett projektnamn på GitHub Pages. Ingen publicering görs automatiskt av
projektet.

## Genomförda kontroller

- Alla tre sidor har testats i webbläsare vid 375, 768 och 1440 pixlars
  bredd utan horisontell överströmning.
- Galleriet växlar mellan tre kolumner och en kolumn. Bildjämförelserna
  växlar mellan två kolumner och en kolumn.
- Alla bildsökvägar, interna länkar och ankarmål pekar på befintliga filer
  respektive element.
- Varje sida har en huvudrubrik, svensk alternativtext för bilderna,
  logotyp, båda ikonlänkarna och rätt aktuell menylänk.
- Tangentbordsfokus och hopplänkens förflyttning till huvudinnehållet har
  testats på startsidan.
- Samtliga bilder laddas i webbläsaren efter konverteringen. De tre
  redigerade fotografierna är 2000 pixlar breda och visas utan beskärning.
- Porträttets genomskinliga pixlar och den gröna bakgrunden har kontrollerats.
- Publicering på GitHub Pages har inte utförts eller testats.