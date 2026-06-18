# latam-tools

Entrypoint hub for the **LATAM Tools** sites — a single static landing page at
**[latam-tools.com.br](https://latam-tools.com.br/)** that links to the community tools for
Ragnarok Online LATAM.

## Linked sites

| Site | URL |
|------|-----|
| Simulador | https://simulador.latam-tools.com.br/ |
| RagnaRecap | https://recap.latam-tools.com.br/ |
| Visuais | https://visuais.latam-tools.com.br/ |
| Calculadora | https://calc.latam-tools.com.br/ |

## Stack

Plain static HTML/CSS — no build step. Hosted on Firebase Hosting (project `latam-tools`).

```
public/
  index.html    # the hub page
  styles.css    # dark, responsive card layout
  favicon.png   # Poring sprite, rendered via ragassets (assets.latam-tools.com.br)
firebase.json   # Hosting config
.firebaserc     # default project = latam-tools
```

The favicon is a Poring sprite generated through the
[ragassets](https://github.com/adsonpleal/ragassets) gateway and committed to the repo:

```
https://assets.latam-tools.com.br/image?job=1002&frame=0
```

## Develop

Serve locally with the Firebase emulator (or any static server):

```bash
firebase emulators:start --only hosting
```

## Deploy

```bash
firebase deploy --only hosting
```

Live at https://latam-tools.com.br/
