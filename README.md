# teacupsandart.com (LittleLink)

Link-in-bio landing page for [teacupsandart.com](https://teacupsandart.com). Static HTML/CSS site built on [LittleLink](https://github.com/sethcottle/littlelink), hosted on Cloudflare.

## Project Structure

| Path | Description |
|---|---|
| `index.html` | Main landing page with social links |
| `images/avatar.jpg` | Profile avatar |
| `images/og-image.jpg` | Open Graph image for social sharing |
| `images/favicon.png` | Favicon source image |
| `privacy.html` | Privacy policy |
| `terms-and-conditions.html` | Terms and conditions |
| `sitemap.xml` | XML sitemap |
| `wrangler.toml` | Cloudflare Workers deployment config |

## Editing

Edit `index.html` to update links or content. The site uses no JavaScript or build step — just static HTML and CSS. LittleLink ships with 100+ branded button styles out of the box — see the [LittleLink Button Builder](https://builder.littlelink.io) to browse available buttons and copy the HTML.

## Deployment

The site is deployed to Cloudflare via `wrangler.toml`. Pushes to `main` trigger a deployment automatically.

## Local Development

Serve the files with any static file server, or use Docker:

```bash
docker compose -f docker/compose.yaml up
```

The site will be available at http://localhost:8080. See [docker/README.md](docker/README.md) for details.
