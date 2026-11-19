# Etheris OS website

Static website for the **Etheris OS** Linux distribution. No build step — open the HTML files directly.

**Live (GitHub Pages):** https://saarniuimonen-beep.github.io/etheris-website/

**OS source:** https://github.com/saarniuimonen-beep/etheris-os

**Latest development ISO (not hosted here):** `etheris-2026.11.19-x86_64.iso`  
SHA256: `10ea77d5b2c183341b85635a9f10693bd102f02b620cf809170e08c394482265`  
Build with `./build.sh` in the OS repo. See [Download](pages/download.html).

**Intended custom domain:** `etheris-os.org` (available — buy it, then set DNS below)

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
