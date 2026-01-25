# Fejlesztesi alapelvek - statikus oldal

Ez a repo egy statikus HTML oldal, amely a 12-factor alapelveket es enterprise kiterjeszteseket mutat be. A tartalom Markdown fajlokbol keszul, amelyeket build lepessel alakitunk at a megjeleniteshez.

## Tartalom szerkezete
- `content/` - Markdown forrasok (minden tema kulon .md fajl)
- `assets/` - statikus assetek (pl. `index.html` sablon)
- `scripts/` - build script(ek)
- `build/` - generalt kimenet (HTML + adat)

## Build
Telepites:
```bash
npm install
```

Build:
```bash
npm run build
```

A build kimenete a `build/` mappaba kerul.

## Build es futtatas Dockerrel (npm nelkul)
A Dockerfile tartalmazza a Node build lepest es az nginx kiszolgalast.
```bash
docker compose up --build -d
```

## Lokal futtatas (nginx)
Docker-compose alapu kiszolgalas:
```bash
docker compose up -d
```

## Tartalom frissitese
1) Szerkeszd a megfelelo `content/*.md` fajlt.
2) Futtasd a `npm run build` parancsot vagy a `docker compose up --build -d` parancsot.
3) Nyisd meg a `build/index.html` fajlt.

## Megjegyzes
A Markdown szovegekben a cimkek (Angol/Magyar) a menu cimekhez hasznalodnak.
