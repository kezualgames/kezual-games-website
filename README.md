# Kezual Games — website

A single-page static site. No build step, no dependencies. Open `index.html` in a browser to preview it locally.

```
index.html          the whole site
assets/
  logo-dark.svg     logo for light backgrounds
  logo-white.svg    logo for dark backgrounds
  icon.svg          the K badge on its own
  icon-32.png       favicon
  icon-180.png      home-screen icon for iOS
  og-image.png      preview image shown when the site is shared
```

## Publishing on GitHub Pages

1. Create a repository on github.com. A free account needs it to be **public** for Pages to work.
2. Upload `index.html`, the `assets` folder and this README. You can drag the files straight onto the repository page in your browser.
3. Go to **Settings → Pages**, set **Source** to "Deploy from a branch", pick the `main` branch and the `/ (root)` folder, then save.
4. Wait a minute. The site appears at `https://<your-username>.github.io/<repository-name>/`.

## Using your own domain

In **Settings → Pages**, enter the domain under "Custom domain". GitHub will tell you which DNS records to add at your registrar. Once it verifies, tick **Enforce HTTPS**.

## Filling in the content

Search `index.html` for `[` to find every placeholder:

- `[ONE-LINE STUDIO DESCRIPTION]` — the sentence under the headline
- `[GAME TITLE 1]` … `[GAME TITLE 5]` — the games
- `[GENRE]` — the small grey tag on each game card
- `[One or two lines on what makes this game fun.]` — each game's description
- `[A teaser line about your next release.]` — the dashed "in development" card
- `[Two or three sentences about Kezual Games…]` — the studio section
- `[YOUR EMAIL]` — the contact button text; also update the `mailto:` address next to it

**Store links:** each game has two `<a class="store" href="#">` links. Replace the `#` with the real App Store and Google Play URLs.

**Social links:** in the footer, replace the `#` in each `<a href="#">` with your real profile URLs, or delete the ones you do not use.

**Game artwork:** each card's art is a coloured `<div class="game__art">` with shapes inside. To use a real screenshot, replace the whole div with:

```html
<img class="game__art" src="assets/game-1.png" alt="Screenshot of [GAME TITLE 1]" style="object-fit:cover;width:100%">
```

and put the image in the `assets` folder.

## Changing the colours

Every colour is defined once at the top of the `<style>` block, under `:root`. Change `--accent` to recolour every button, tag and the footer at once.
