# How to: Blog-Post schreiben

## Neuen Post anlegen

Ordner und Datei erstellen:

```
content/blog/mein-post-slug/
├── index.md
└── bild.png        (optional)
```

## index.md Vorlage

```markdown
+++
title = "Titel des Posts"
date = 2026-02-08
description = "Kurzbeschreibung für Startseite und RSS-Feed."
[taxonomies]
tags = ["tag1", "tag2"]
+++

Einleitungstext, sichtbar auf der Startseite.

<!-- more -->

Ab hier nur auf der Post-Seite sichtbar.

## Unterüberschrift

Normaler Markdown-Text mit **fett**, *kursiv*, `code`.

![Bildbeschreibung](bild.png)

[Link zu anderem Post](@/blog/erster-post/index.md)
```

## Lokal testen

```bash
zola serve
```

Öffnet http://127.0.0.1:1111 mit Live-Reload.

## Veröffentlichen

```bash
git add content/blog/mein-post-slug/
git commit -m "Add post: Titel des Posts"
git push
```

Nach ca. 45 Sekunden automatisch live auf https://ichautomatisierdasjetzt.web.app.
