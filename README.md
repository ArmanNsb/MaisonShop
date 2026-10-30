# Maison De La Fork · Shop page (holiday redesign)

A single static page with no build step and no dependencies. Everything it needs is in this folder; the only thing loaded from outside is the KoHo font from Google Fonts.

```
index.html          the whole page (markup, styles and scripts)
assets/img/         product photos, Cupid crest, garland, logos, favicon
assets/fonts/       Dahlia (display type)
.nojekyll           tells GitHub Pages to serve the files as they are
```

## Preview on your computer

Open a terminal in this folder and run:

```
python3 -m http.server 8000
```

Then visit http://localhost:8000. Double-clicking `index.html` also works, but some browsers block local fonts from `file://`, so the local server is closer to the real thing.

## Deploy with GitHub Pages

1. Create a repository and upload the **contents** of this folder to its root, so `index.html` sits at the top level. Include the hidden `.nojekyll` file (on a Mac, press Cmd + Shift + . in Finder to see it).
2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, select `main` and `/ (root)`, and save.
4. After a minute the site is live at `https://<your-username>.github.io/<repository-name>/`.

All paths are relative, so the page works at a subpath as well as on a custom domain.

## Notes before launch

- This is a design build. The Add to Bag, Search, Sort and newsletter controls are not connected to the store yet; the menu, footer and "Begin" links point to the live maisondelafork.com pages.
- Product photos are 300 × 300 px. Replace them with the originals under the same file names in `assets/img/` for sharper images.
- Make sure the Dahlia licence covers web use.
