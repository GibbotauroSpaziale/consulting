# Gibbotauro Consulting — consulting.gibbotauro.com

Landing consulenza di **Gibbotauro Spaziale**, servita su `consulting.gibbotauro.com`.
Sito separato dal sito principale (`gibbotauro.com`) e dal linktree (`space.gibbotauro.com`).
Identità visiva unica dell'ecosistema (cyberpunk HUD + palette YouTube dark).

## Struttura

```
/             consulting.gibbotauro.com   consulenza YouTube (hero, form candidatura)
CNAME         consulting.gibbotauro.com
```

## Stato attuale

- Landing v2 visual + bottoni outline v3.5 (bordo uniforme sull'angolo tagliato — `--ci = cut − bt·(2−√2)`; testo sopra base via `z-index:-1` + `isolation:isolate`)
- Decisione architettura (2026-10-02): 3 siti separati → 3 repo. Questa repo = **solo consulenza**
- **Stack**: HTML/CSS/JS statico, hosting GitHub Pages, nessun CMS

## Deploy

1. Push su GitHub (repo `gibbotauro-consulting`, branch `main`)
2. Pages → custom domain `consulting.gibbotauro.com` (CNAME già nel root)
3. DNS Aruba: `CNAME consulting` → `GibbotauroSpaziale.github.io.`

## Fasi CSS (split design system)

- `css/base.css` — tokens, reset, tipografia, utilità
- `css/consulenza.css` — stili della landing (eredita da style.css attuale)
- `css/layout.css` — header/nav condiviso, footer

NOTA: `stats.css` (griglia KPI) NON appartiene a questa repo — va nel sito principale (sponsor).

## Blocca il build finale

1. Endpoint form + email notifiche (Web3Forms o Formspree come endpoint gratuito)
2. 3-5 testimonianze da colleghi
3. Selezione video per sezione proof
4. Foto "chi sono"