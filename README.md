# Team LinkedIn Seite (HTmB 2026)

Eine einzelne, statische Seite mit einer Karte pro Teammitglied. Jede Karte verlinkt auf das jeweilige LinkedIn Profil. Kein Build-Prozess, keine Abhängigkeiten außer Google Fonts, funktioniert direkt auf GitHub Pages.

## Fotos einfügen

Lege die Fotos einfach mit exakt diesen Dateinamen in den Ordner `images/`:

- `images/inoussa-adouba.jpg`
- `images/radoslav-karastoyanov.jpg`
- `images/niklas-sohn.jpg`
- `images/tim-kramny.jpg`
- `images/julian-kupfer.jpg`
- `images/julien-sauter.jpg`
- `images/theresa-thiele.jpg`
- `images/marius-tschimmel.jpg`
- `images/lukas-bilger.jpg`
- `images/niklas-hohn.jpg`

Solange ein Foto fehlt, zeigt die Karte automatisch einen Platzhalter mit den Initialen der Person. Sobald du eine Datei mit dem passenden Namen in `images/` legst, wird sie automatisch geladen, ohne dass am Code etwas geändert werden muss. `.png` funktioniert auch, dann einfach die Dateiendung im jeweiligen `src="images/..."` im `index.html` anpassen.

Format: Hochkantfotos (3:4) sehen am saubersten aus, quadratische Bilder gehen aber auch, die Karte schneidet automatisch passend zu.

## Julian Kupfer

Julian hat noch keinen LinkedIn Link hinterlegt, seine Karte zeigt deshalb aktuell "Bald auf LinkedIn" statt eines Buttons. Sobald er ein Profil hat, im `index.html` bei seiner Karte einfach ersetzen:

```html
<span class="btn disabled">Bald auf LinkedIn</span>
```

durch:

```html
<a class="btn" href="HIER_LINK_EINFÜGEN" target="_blank" rel="noopener">
  <svg viewBox="0 0 24 24"><path d="M20.45 20.45h-3.56v-5.57c0-1.33-.02-3.04-1.85-3.04-1.86 0-2.14 1.45-2.14 2.94v5.67H9.34V9h3.42v1.56h.05c.48-.9 1.64-1.85 3.38-1.85 3.61 0 4.28 2.38 4.28 5.47zM5.34 7.43a2.07 2.07 0 1 1 0-4.13 2.07 2.07 0 0 1 0 4.13zM7.12 20.45H3.56V9h3.56z"/></svg>
  LinkedIn
</a>
```

## Auf GitHub Pages hosten

1. Neues Repository auf GitHub erstellen (z. B. `htmb-team`).
2. `index.html`, `README.md` und den `images/` Ordner (mit Fotos) in das Repository hochladen (per GitHub Web-Upload oder `git push`).
3. Im Repository auf **Settings → Pages**.
4. Bei **Source** die Branch `main` und den Ordner `/ (root)` auswählen, dann **Save**.
5. Nach ein bis zwei Minuten ist die Seite live unter:
   `https://DEIN-GITHUB-NAME.github.io/htmb-team/`

Diesen Link dann in einen QR-Code umwandeln (z. B. auf qr-code-generator.com) und auf der Team-Folie platzieren.

## Anpassen

Alles liegt in der einen Datei `index.html`, Struktur pro Person ist immer der gleiche Block:

```html
<div class="card">
  <div class="avatar">
    <div class="initials">XY</div>
    <img src="images/vorname-nachname.jpg" alt="Name" onerror="this.style.display='none'">
  </div>
  <div class="name">Name</div>
  <div class="role">Rolle im Projekt</div>
  <a class="btn" href="LINKEDIN_URL" target="_blank" rel="noopener">...LinkedIn</a>
</div>
```

Reihenfolge, Rollen oder Text lassen sich direkt im jeweiligen Block anpassen.
