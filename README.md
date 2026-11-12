# Etheris OS website

Independent static site for the **Etheris OS** Linux distribution (Ocean Glass / Neo-Aero). No build step.

**Live (GitHub Pages):** https://saarniuimonen-beep.github.io/etheris-website/

**Intended custom domain:** `etheris-os.org` (available — buy, then wire DNS below)

This project is not affiliated with Etheris Labs, Etheris AG, Etheris Chile, AETHERIS, or other “Etheris” brands. `etheris.com` / `etheris.org` are already taken by unrelated parties.

## Local preview

```bash
cd ~/etheris-website
python3 -m http.server 8765
# open http://127.0.0.1:8765/
```

Fonts are self-hosted. No analytics.

## Custom domain setup (`etheris-os.org`)

1. Register **etheris-os.org** at a registrar (Porkbun, Namecheap, Cloudflare Registrar, etc.).
2. Tell the site maintainer (or run the DNS steps yourself), then:
   - Add a repo root file `CNAME` containing exactly: `etheris-os.org`
   - In GitHub Pages settings, set custom domain to `etheris-os.org` and enable HTTPS
3. At the registrar, point DNS at GitHub Pages:

| Type | Name | Value |
|------|------|--------|
| A | `@` | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |
| AAAA | `@` | `2606:50c0:8000::153` |
| AAAA | `@` | `2606:50c0:8001::153` |
| AAAA | `@` | `2606:50c0:8002::153` |
| AAAA | `@` | `2606:50c0:8003::153` |
| CNAME | `www` | `saarniuimonen-beep.github.io` |

Propagation can take a few minutes to a few hours. HTTPS activates after GitHub verifies the domain.
