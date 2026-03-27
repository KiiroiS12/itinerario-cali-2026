# Itinerario Cali 2026

Sitio estático con el itinerario de Semana Santa (Cali y Jamundí). Una sola página (`index.html`), tema claro/oscuro, calendario por día y presupuesto aproximado.

## Sitio publicado

Tras activar GitHub Pages (pasos abajo), la URL suele ser:

**https://kiirois12.github.io/itinerario-cali-2026/**

(Sustituye `kiirois12` por tu usuario de GitHub si es distinto.)

## Habilitar GitHub Pages (recomendado: GitHub Actions)

Este repositorio incluye un workflow en [`.github/workflows/pages.yml`](.github/workflows/pages.yml) que despliega automáticamente al hacer `push` a `main`.

1. En GitHub, abre el repositorio → **Settings** → **Pages** (menú lateral).
2. En **Build and deployment** → **Source**, elige **GitHub Actions** (no “Deploy from a branch”).
3. Haz push a `main` (o ejecuta el workflow manualmente en **Actions** → **Deploy to GitHub Pages** → **Run workflow**).
4. Espera a que el job termine; en **Settings → Pages** aparecerá “Your site is live at…”.

La primera vez, GitHub puede pedir aprobar permisos del workflow para **Pages**; acéptalos en la pestaña **Actions** si ves un aviso.

### Archivos relevantes para Pages

| Archivo / carpeta | Uso |
|-------------------|-----|
| [`index.html`](index.html) | Página principal |
| [`images/`](images/) | Imágenes del itinerario |
| [`.nojekyll`](.nojekyll) | Evita que Jekyll procese el sitio (archivos y rutas estáticas) |

## Opción alternativa: rama `main` y carpeta raíz

Si prefieres no usar Actions:

1. **Settings** → **Pages** → **Source** → **Deploy from a branch**.
2. **Branch**: `main`, carpeta **`/ (root)`** → **Save**.

Con este modo no hace falta el workflow; cada `push` a `main` actualiza el sitio.

> No actives **GitHub Actions** y **Deploy from a branch** a la vez para el mismo sitio: usa solo una fuente en **Settings → Pages**.

## Desarrollo local

Abre `index.html` en el navegador o sirve la carpeta para evitar limitaciones con rutas:

```bash
cd itinerario-cali-2026
python3 -m http.server 8080
```

Luego visita `http://localhost:8080`.

## Más información

- Lista de imágenes pendientes: [`IMAGENES_PENDIENTES.md`](IMAGENES_PENDIENTES.md).
