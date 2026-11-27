# pets-ready-solutions
Public Material for Practitioners and Users alike

## Product pages

Each product has a small landing page with its video(s), published with GitHub Pages from `docs/`.

| Product | Page |
| --- | --- |
| PetalGuard | https://crypto-tii.github.io/pets-ready-solutions/petalguard/ |

### Layout

```
docs/
  .nojekyll             tells GitHub Pages to skip Jekyll (see below)
  index.html            hub page listing all products
  assets/site.css       shared styles
  <product>/
    index.html          product page
    media/              videos (MP4), poster frames, logo
```

`docs/.nojekyll` is an empty file. By default GitHub Pages runs every site through Jekyll, which ignores files and folders starting with `_` or `.` and adds build time. The pages here are plain HTML, so this file makes Pages publish `docs/` exactly as it is in the repo.

### Adding a product

1. Copy `docs/petalguard/` to `docs/<product>/` and edit the text, links and media.
2. Add a card for it in `docs/index.html`, inside `<nav class="cards">`, where the comment `Add one card per product here` sits:

   ```html
   <a class="card" href="<product>/">
     <img src="<product>/media/logo.png" alt="" width="56" height="56">
     <div>
       <h2>Product name</h2>
       <p>One-line description.</p>
     </div>
   </a>
   ```

3. Add a row for it to the table above.
4. Keep each MP4 small (H.264, 720p or 1080p, `-movflags +faststart`, ideally under 30 MB). GitHub rejects files over 100 MB, and Pages does not serve Git LFS files.

### Publishing

Settings → Pages → Source: "Deploy from a branch", Branch: `main`, folder `/docs`.
Generate poster QR codes only after the page URL is live.

## License
© 2026 <Your name or organization>. Licensed under
[CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/)
