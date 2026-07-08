# Cargos públicos de Canarias · Patrimonio y retribución

Visualizaciones interactivas (D3) de **ODESOCAN** sobre el patrimonio y las retribuciones
de los cargos públicos de Canarias, en tres bloques:

- **Parlamento de Canarias** — 70 diputados y diputadas de la XI Legislatura (arco en U).
- **Gobierno de Canarias** — Consejo de Gobierno (13 miembros).
- **Altos cargos** — estructura ejecutiva (147 cargos).

## Ver la visualización

Página completa (las 3 pestañas):

> https://cristianodesocan.github.io/viz-cargos-publicos/

## Datos

Los datos y las fotos **no van embebidos**: se sirven desde **Supabase** (proyecto
`bd_odesocan`, schema `cargos_publicos`) mediante su API REST pública y su Storage. La clave
que aparece en el código es la **`anon`**, pública y segura para navegador (acceso de solo
lectura, protegido por RLS). **No hay ninguna credencial secreta en este repositorio.**

## Incrustar en WordPress / Divi

Pega el contenido de [`DIVI_bloque_interactivo.html`](DIVI_bloque_interactivo.html) en un
módulo **Código** de Divi. Ya viene configurado con `BASE_URL` apuntando a este GitHub Pages;
solo tendrás que ajustar `SCROLL_OFFSET` (alto en px de tu menú fijo) si hace falta.

## Estructura

| Archivo | Qué es |
|---|---|
| `observatorio_cargos_publicos_canarias.html` | Shell de 3 pestañas (une los 3 hijos por iframe) |
| `parlamento_u_d3.html` · `gobierno_organigrama_d3.html` · `altos_cargos_gobierno_d3.html` | Los 3 hijos D3 (modo `?embed=1` para incrustar) |
| `d3.v7.min.js` | Librería D3 v7 |
| `logos_base64.js` | Logos de los partidos |
| `layout_u.js` · `salario_2025.js` · `gobierno_2025.js` | Geometría y datos auxiliares del Parlamento |
| `DIVI_bloque_interactivo.html` | Fragmento para el módulo Código de Divi |

Actualizar la web publicada = `git push` (GitHub Pages redespliega solo).
