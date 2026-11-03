# Alexander Marsh — Portfolio

A single-page, self-contained portfolio (`index.html`) built for GitHub Pages. No build step, no dependencies to install.

```
Alezanduh.github.io/
├── index.html                          # the whole site (HTML + CSS + a little JS)
├── assets/
│   ├── Alexander-Marsh-Resume.pdf      # linked from the Resume buttons
└── README.md                           # this guide
```

Because this repo is named `Alezanduh.github.io`, GitHub Pages serves it at **https://alezanduh.github.io**.

---

## Deploy to GitHub Pages in under 5 minutes

1. **Preview locally (optional, 30 sec).** Double-click `index.html`, or from this folder run:
   ```bash
   open index.html
   ```
2. **Commit and push to GitHub.**
   ```bash
   git add index.html assets README.md
   git commit -m "Add portfolio site"
   git push origin main
   ```
3. **Turn on Pages.** On GitHub, open the repo → **Settings** → **Pages** (left sidebar).
4. Under **Build and deployment → Source**, choose **Deploy from a branch**.
5. Under **Branch**, pick **`main`** and folder **`/ (root)`**, then click **Save**.
6. **Wait ~1 minute**, refresh the Pages settings screen, and you'll see
   *"Your site is live at https://alezanduh.github.io"*. Open it.
7. **Updating later:** edit, commit, push. The site redeploys automatically (about a minute).

> If you see a 404, check that the file is named exactly `index.html` (lowercase) in the repo root and that Pages is set to `main` / `(root)`.

---

## Customize it (search `index.html` for `REPLACE`)

Every spot that needs your input has a `<!-- REPLACE ... -->` comment.

| What | Where |
|---|---|
| **Fonts** | Titles use Bebas Neue (all caps, free from Google Fonts). Body text uses Dashiell Fine if you add it: put it in a Web Project at [fonts.adobe.com](https://fonts.adobe.com), paste the kit `<link>` at the `REPLACE WITH YOUR ADOBE FONTS KIT` comment, and confirm the CSS family name in `--font-text`. Until then the body falls back to Newsreader. |
| **Headshot** | Hidden for now. In `index.html`, find `HEADSHOT (currently hidden)`, delete the word `hidden`, add `assets/avatar.jpg`, delete the placeholder `<div>` and uncomment the `<img>`. |
| **Project images (optional)** | Uncomment the `REPLACE WITH YOUR PROJECT IMAGE` line at the top of each project card. |
| **Featured articles** | Two slots under `FEATURED ARTICLES`. Slot 1 links to your Heliocentrism and Success post. For each, replace the headline, link, summary, byline, image (`assets/article-1.jpg`, `article-2.jpg`) and the caption / credit shown beneath the image. |
| **Project GitHub links** | `REPLACE WITH THE GITHUB REPOSITORY LINK`. Three cards currently point to your GitHub profile because their repo URLs weren't in the resume. |
| **Resume** | Overwrite `assets/Alexander-Marsh-Resume.pdf` with your latest PDF. |
| **Colours** | Variables at the top of the `<style>` block. `--bg` is the dark brown background (`#241603`), `--forest` is the dark green, `--cream` is the text colour, `--burgundy` / `--coral` are the red accents, and `--teal-hi` is a light sage accent. The pinstripes are the `.stripes` rule (`--stripes` sets the count, `--stripe-color` the cream and its opacity). |
| **Link-preview image** | Uncomment the `og:image` tag in `<head>` and point it at an image in `assets/`. |

## Notes

- The Experience section intentionally uses lowercase text (except GEICO) per the requested style, so it uses the body font rather than the all-caps title font.
- The top bar, name, role line and section headers are lowercase italic (the same style as "talk ball?"). Section titles are written in Title Case in the HTML and displayed in all caps by the title font. The closing "talk ball?" header is intentionally lowercase and uses the body font.
- Bebas Neue and the Newsreader fallback load from Google Fonts; Adobe Fonts loads from `use.typekit.net` once you add your kit.
- Want a custom domain later? Settings → Pages → **Custom domain**.
