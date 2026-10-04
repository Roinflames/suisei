# PRODIGITAL — sitio comercial (suisei.cl)

Sitio de presentación de **PRODIGITAL SpA**: software a medida, automatización e
IA aplicada para reducir el trabajo administrativo en empresas chilenas.
Su objetivo es convertir visitas en conversaciones (WhatsApp o formulario).

- **Dominio:** suisei.cl (Cloudflare). El dominio `prodigital.cl` es de otra empresa.
- **Contenido:** servicios, forma de trabajo, caso de farmacia (anónimo, sin autorización
  del cliente para nombrarlo) y contacto. Sin precios.

## Técnico

Página estática: un solo `index.html` más `assets/`, sin build ni dependencias.

- Vista local: `python3 -m http.server 3045` → http://127.0.0.1:3045
- Formulario: Formspree (`FORMSPREE_ID` en `index.html`).
- Publicación: Cloudflare. Ver el PR que introdujo este sitio para el estado del
  despliegue (Worker `morning-bird-44bd` vs. proyecto conectado a Git).

---

Forjado por **PRODIGITAL SpA** · Shogun a cargo: Rodrigo Reyes
