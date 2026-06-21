# seegfui-print-assets

Öffentliche **Druck-Assets** (freigestellte PNGs + Vektor-SVGs) der Marke **Seegfui**,
ausgeliefert über **jsDelivr** als CDN für die Gelato-Druckanbindung.

> Quelle der Wahrheit ist das (private) Code-Repo `djmana78/seegfui`, Verzeichnis `designs/`.
> Dieses Repo wird daraus **1:1 gespiegelt** (nur `*_transparent.png` und `*_vektor.svg`)
> und auf einen Tag gepinnt. Nicht von Hand bearbeiten.

## Nutzung (ASSET_BASE_URL)

```
https://cdn.jsdelivr.net/gh/djmana78/seegfui-print-assets@v1
```

Beispiel:
```
https://cdn.jsdelivr.net/gh/djmana78/seegfui-print-assets@v1/Seegfui-Ammersee-Paket/Orte/hell/<datei>_transparent.png
```

Liefert `200` + `Content-Type: image/png`, ohne Auth — direkt von Gelato ladbar.

## Aktualisieren

Im Code-Repo `djmana78/seegfui`: `scripts/assets/publish-jsdelivr.sh` spiegelt `designs/`
und pusht den nächsten Tag (v2, v3, …). Danach `ASSET_BASE_URL` umstellen und
`npm run verify-assets` ausführen. Hintergrund: SEE-12 / SEE-24.
