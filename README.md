# MediaSnap — Descargador Multimedia

Herramienta gratuita de conversión y descarga de medios.  
**Frontend:** GitHub Pages | **Backend:** Render (Flask + yt-dlp)

---

## Estructura de repos

```
mediasnap-frontend/   → GitHub Pages (este repo o carpeta /docs)
mediasnap-backend/    → Render (API Python)
```

---

## Deploy del Backend (Render)

1. Crea un repo en GitHub con la carpeta `mediasnap-backend/`
2. Ve a [render.com](https://render.com) → **New Web Service**
3. Conecta el repo
4. Configura:
   - **Build Command:** `bash build.sh`
   - **Start Command:** `gunicorn app:app`
   - **Plan:** Free
5. Copia la URL que te da Render (ej: `https://mediasnap-api.onrender.com`)

---

## Deploy del Frontend (GitHub Pages)

1. Crea un repo en GitHub con la carpeta `mediasnap-frontend/`
2. En `index.html`, línea ~220, cambia:
   ```js
   const API_BASE = "https://TU-API.onrender.com";
   ```
   por la URL real de tu backend en Render.
3. Ve a **Settings → Pages → Deploy from branch → main / root**
4. Tu sitio queda en `https://TU-USUARIO.github.io/mediasnap-frontend`

---

## Monetización con anuncios

En `index.html` hay **2 espacios marcados** con comentarios:

```html
<!-- PEGA AQUÍ TU CÓDIGO DE ANUNCIO -->
```

- **Banner superior** (728×90 o responsive)
- **Anuncio cuadrado medio** (300×250)

### Redes recomendadas (permiten este tipo de herramienta):
| Red | Registro | Aprobación |
|---|---|---|
| [Adsterra](https://adsterra.com) | Inmediato | 24-48h |
| [Propeller Ads](https://propellerads.com) | Inmediato | Rápido |
| [Hilltop Ads](https://hilltopads.com) | Inmediato | 24h |

---

## Notas legales

- El sitio no almacena archivos, solo los procesa en memoria temporal
- Agrega páginas `terminos.html`, `privacidad.html` y `dmca.html`
- Preséntate siempre como "conversor multimedia", no menciones plataformas en el copy
