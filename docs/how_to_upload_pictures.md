# Hvordan laste opp og bruke bilder i MkDocs

Den beste måten i dette repoet er å lagre bilder **lokalt i `docs/images/`** og bruke relative stier i Markdown.

## Anbefalt arbeidsflyt

1. Optimaliser bildet før opplasting (WebP/JPEG, fornuftig oppløsning).
2. Legg filen i `docs/images/`.
3. Gi filen et beskrivende navn med små bokstaver og bindestrek, f.eks. `kylling-suppe.webp`.
4. Referer bildet fra siden din med relativ sti.

## Eksempel

```md
![Kyllingsuppe](images/kylling-suppe.webp)
```

## Hvorfor dette er best

- Bildene versjoneres sammen med dokumentasjonen
- Fungerer lokalt og på GitHub Pages uten ekstra opplastingstjenester
- Enklere vedlikehold og færre brutte lenker
