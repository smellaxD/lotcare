# Lotcare — Sito ufficiale

Sito web di Lotcare, l'app desktop per la gestione di lotti di produzione, clienti e fornitori.

## Struttura

```
.
├── index.html      # Landing page (variante "Dark Bold" — la scelta)
├── assets/         # Logo e asset visivi
├── archivio/       # Varianti di design non scelte (V1 artigianale, V2 SaaS) + screenshot
└── download/       # NON versionato: setup.exe + blockmap + latest.yml
                    # (caricati come asset della Release GitHub per l'auto-update)
```

## Pubblicazione

- **Sito**: GitHub Pages servito dalla root del branch `main` →
  `https://smellaxd.github.io/lotcare/`
- **Installer + auto-update**: asset della Release GitHub (repo `lotcare`).
  Il pulsante "Scarica" punta a:
  `https://github.com/smellaxd/lotcare/releases/latest/download/lotcare-1.0.0-setup.exe`
- **Auto-update app**: `electron-builder.yml` → `publish: provider github`.

## Come aggiornare una release

1. `npm run build:win` in `C:\Users\emanu\benvenuto-app`
2. `gh release create vX.Y.Z dist/lotcare-X.Y.Z-setup.exe dist/lotcare-X.Y.Z-setup.exe.blockmap dist/latest.yml`
3. Il sito punta sempre a `releases/latest/download/...` → nessuna modifica al sito necessaria.

## Varianti archiviate

Le varianti non scelte restano in `archivio/` per eventuali usi futuri:
- `V1-artigianale.html` — serif/crema, postura editoriale calda
- `V2-saas-moderno.html` — Inter/bianco, postura SaaS pulita
