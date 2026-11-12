# uzunyx.com

Página web de [Uzunyx](https://github.com/antarest47/uzunyx), servida con GitHub Pages
en `https://uzunyx.com`. Es HTML estático, sin generador: `index.html`, las imágenes en
`img/` y `CNAME` con el dominio. `.nojekyll` evita que GitHub la pase por Jekyll.

Para verla en local:

```bash
python3 -m http.server -d . 8000
```

Las imágenes son copias reducidas de las del repo de Uzunyx (logos de `uzunyx-plymouth/art`,
fondos de `wallpapers/`, capturas de `uzunyx-lnf` y `uzunyx-iso`). Al publicar una ISO nueva,
cambiar la versión y los enlaces de descarga en `index.html`; si sube `uzunyx-archive-keyring`,
también su nombre en la sección `#apt` (R2 no lista carpetas: `dl.uzunyx.com/repo/` da 404).

## Publicar

1. En GitHub, *Settings → Pages → Build and deployment → Deploy from a branch*:
   `main`, `/ (root)`.
2. En Cloudflare, DNS de `uzunyx.com`, en modo *DNS only* (nube gris):
   - `A` `uzunyx.com` → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`,
     `185.199.111.153`
   - `CNAME` `www` → `antarest47.github.io`
3. En *Settings → Pages* del repo, dominio `uzunyx.com` y, cuando GitHub emita el
   certificado, *Enforce HTTPS*.
4. En los *Settings* de la cuenta → *Pages → Add a domain*: verificar `uzunyx.com` con el
   registro `TXT` que pide GitHub.

`dl.uzunyx.com` (ISO y repositorio APT, en Cloudflare R2) no cambia.

## Licencia

Código GPL-3.0-or-later, imágenes CC0-1.0, como Uzunyx.
