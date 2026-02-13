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

Any changes pushed to `main` — whether from a local editor or directly via the GitHub web UI — will automatically trigger a Cloudflare Pages deployment and go live on [teacupsandart.com](https://teacupsandart.com) within seconds.

## Hosting & Deployment

The site is hosted on **Cloudflare Pages** with the following setup:

1. **Cloudflare Pages project** — connected to this Git repository. Pushes to `main` trigger a deployment automatically. No build command or framework is needed since the site is plain static HTML/CSS. See the [Cloudflare Pages docs](https://developers.cloudflare.com/pages/) for general setup instructions.
2. **Custom domains** — `teacupsandart.com` and `teacupsandart.be` are both added as custom domains in Cloudflare (managed DNS).
3. **Redirect rules** — Cloudflare Rules are used to:
   - Redirect `www.teacupsandart.com` → `teacupsandart.com`
   - Redirect `teacupsandart.be` (and `www.teacupsandart.be`) → `teacupsandart.com`

   These are configured under **Rules > Redirect Rules** in the Cloudflare dashboard. See the [Cloudflare Redirect Rules docs](https://developers.cloudflare.com/rules/url-forwarding/) for details.

## Local Development

Serve the files with any static file server, or use Docker:

```bash
docker compose -f docker/compose.yaml up
```

The site will be available at http://localhost:8080. See [docker/README.md](docker/README.md) for details.
