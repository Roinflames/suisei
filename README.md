# PRODIGITAL — sitio comercial (suisei.cl)

Sitio de presentación de **PRODIGITAL SpA**: software a medida, automatización e
IA aplicada para reducir el trabajo administrativo en empresas chilenas.
Su objetivo es convertir visitas en conversaciones (WhatsApp o formulario).

- **Dominio:** suisei.cl (Cloudflare). El dominio `prodigital.cl` es de otra empresa.
- **Contenido:** servicios, forma de trabajo, caso de farmacia (anónimo, sin autorización
  del cliente para nombrarlo) y contacto. Sin precios.
- **`farmacias.html`** (`/farmacias`): landing para prospección 1:1 de farmacias independientes; CTA solo WhatsApp (etiqueta `[farmacias]`) y correo.

## Técnico

Página estática: un solo `index.html` más `assets/`, sin build ni dependencias.

- Vista local: `python3 -m http.server 3045` → http://127.0.0.1:3045
- Formulario: Formspree (`FORMSPREE_ID` en `index.html`). Exige aceptar el aviso de privacidad.
- Publicación: Cloudflare Pages, proyecto `suisei` conectado a Git. Merge a `main` = producción;
  cada rama genera una vista previa en `<rama>.suisei-aa9.pages.dev`.
- Fuentes alojadas en `assets/fonts/`, sin Google Fonts (ver su README).
- `404.html` en la raíz desactiva el fallback SPA de Pages: las URL inexistentes responden 404.

## Datos personales (Ley 21.719)

`privacidad.html` es el aviso de privacidad. Si cambia algo de lo que declara, hay que
actualizar el aviso **en el mismo PR**: proveedores (Formspree, Cloudflare, Google, WhatsApp),
datos pedidos en el formulario, retención (12 meses sin relación comercial) o canal
ARCOP (`privacidad@suisei.cl`). El texto es un borrador pendiente de revisión legal.

---

Forjado por **PRODIGITAL SpA** · Shogun a cargo: Rodrigo Reyes
