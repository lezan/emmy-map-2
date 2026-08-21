# Emmy Map 2

Mappa web statica pronta per GitHub Pages, realizzata con Leaflet e fondi
OpenStreetMap/OpenTopoMap.

La webapp pubblica i layer `area`, `massif`, `border` e `hut`. Il file
`data/manifest.json` definisce ordine, etichette francesi, URL e conteggio
delle feature.

I GeoJSON usano coordinate geografiche CRS84 (longitudine, latitudine),
compatibili con Leaflet. La vista iniziale è centrata sul perimetro di
`area.geojson`; i punti di `massif.geojson` mostrano etichette permanenti
derivate dal campo `range`. I rifugi usano il simbolo SVG condiviso con Emmy
Map 1.

## Provare la mappa in locale

Avviare un server HTTP dalla cartella della webapp, per esempio:

```powershell
python -m http.server 8000
```

Poi aprire `http://localhost:8000`. Il caricamento diretto di `index.html` dal
disco può essere bloccato dal browser perché la pagina legge i GeoJSON con
`fetch`.

## Pubblicazione

Il repository è predisposto per essere pubblicato dalla root tramite GitHub
Pages. Tutti i file pubblicati sono accessibili pubblicamente.
