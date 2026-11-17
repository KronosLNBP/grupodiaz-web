# grupodiaz-web

Sitio de **Grupo Empresarial Díaz** (https://grupoempresarialdiaz.com.mx): portal del grupo que presenta sus siete empresas y lleva a cada una.

Sitio estático (HTML, CSS y JavaScript, sin compilación).

## Estructura

```
index.html                     Página de inicio (una sola página con secciones)
404.html                       Página de error
unidades.html, trayectoria.html, nosotros.html, contacto.html
                               Redirigen a las secciones nuevas (páginas del sitio anterior)
css/styles.css                 Estilos (índigo #0B0048 del logo "GD")
js/main.js                     Menú en celular
robots.txt, sitemap.xml        SEO
```

Las imágenes ya están en el hosting y no se tocan al publicar: `img/logo.png`, `img/gd.jpg`, `img/nosotros.jpg` y los logos de `img/unidades/`. El logo de Sports Medicine se carga desde sportsmedicine.com.mx.

## Empresas
Clínica de Rodillas · Cámara Hiperbárica · Sports Medicine México · Campuzano y Orrante · XT Negocio · XTres60 · Innovating Kids.

## Pendientes
- Confirmar el correo contacto@grupodiaz.com.mx (el dominio es distinto al del sitio).
- El sitio anterior mostraba un número de XT Negocio/Xtres60 (+52 771 234 5678) que parece de ejemplo; no se usó.
- Campuzano y Orrante no responde por https; el enlace usa http.
- Datos del área inmobiliaria si se quiere presentar como empresa.
- Logos de las empresas optimizados (algunos pesan ~200 KB).

## Publicación
Cada cambio en `main` se publica por FTP (`.github/workflows/deploy.yml`) con los secrets `FTP_SERVER`, `FTP_USERNAME`, `FTP_PASSWORD` y `FTP_SERVER_DIR` de este repositorio. Antes de subir, el flujo respalda las páginas que reemplaza en los *Artifacts* de cada ejecución (90 días).
