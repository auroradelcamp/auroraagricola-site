# auroraagricola.com

Static version of the Aurora Agrícola website, served by Cloudflare Pages. It replaces the old WordPress site.

## Layout

- `public/` is the whole site. Every page is a plain HTML file at `public/<page>/index.html`.
- `public/css/site.css` holds all styles.
- `public/img/` holds the images, keeping the old WordPress `uploads` year/month folders.
- `public/_redirects` sends retired WordPress URLs (the Portuguese page, the duplicate precision hoe page, `/wp-content/uploads/...`) to their new homes.
- `public/_headers` sets security and caching headers.

There is no build step. To change a page, edit its HTML file. The header and footer are repeated in each page, so a menu or contact change needs a search-and-replace across `public/`.

## Cloudflare Pages settings

- Framework preset: None
- Build command: (leave empty)
- Build output directory: `public`

## Preview locally

```sh
python3 -m http.server 8000 --directory public
```

Then open http://localhost:8000.
