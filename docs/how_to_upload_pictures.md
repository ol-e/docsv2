# Hvordan laste opp og bruke bilder i MkDocs

Den beste måten i dette repoet er å lagre bilder **lokalt i `docs/images/`** og bruke relative stier i Markdown.

## Standard for galleri-bilder

- **Format:** WebP (foretrukket), JPEG som fallback.
- **Miniatyrer:** ca. 600–800 px bredde.
- **Større visning:** ca. 1800–2400 px bredde.
- **Komprimering:** hold filstørrelse lav nok til rask mobilvisning.

## Mappestruktur for foto-galleri

Bruk en stabil struktur under `docs/images/gallery/`:

```text
docs/images/gallery/<kategori>/<prosjekt>/
  thumbnails/
  full/
```

Eksempel:

```text
docs/images/gallery/portretter/2026-oslo-session/
  thumbnails/vinduslys-01.webp
  full/vinduslys-01.webp
```

## Filnavnregler

1. Små bokstaver
2. Bindestrek mellom ord
3. Ingen mellomrom eller spesialtegn
4. Legg på løpenummer ved serier (`-01`, `-02`, ...)

Eksempel: `vinduslys-01.webp`

## Arbeidsflyt: legg til, oppdater, fjern

### Legg til bilde

1. Eksporter miniatyr + stor versjon.
2. Legg filene i riktig `thumbnails/` og `full/`.
3. Legg inn bildet på gallerisiden med alt-tekst og metadata.
4. Kjør `mkdocs build` og sjekk at lenker fungerer.

### Oppdater bilde

1. Behold samme filnavn hvis URL skal være stabil.
2. Erstatt både miniatyr og stor versjon.
3. Oppdater metadata ved behov.

### Fjern bilde

1. Fjern referansen i Markdown først.
2. Slett filer i både `thumbnails/` og `full/`.
3. Kjør `mkdocs build` for å avdekke brutte lenker.

## Eksempel på referanse i Markdown

```md
[![Vinduslys](images/gallery/portretter/2026-oslo-session/thumbnails/vinduslys-01.webp)](images/gallery/portretter/2026-oslo-session/full/vinduslys-01.webp)
```

## Hvorfor dette er best

- Bildene versjoneres sammen med dokumentasjonen
- Fungerer lokalt og på GitHub Pages uten ekstra opplastingstjenester
- Enklere vedlikehold og færre brutte lenker
