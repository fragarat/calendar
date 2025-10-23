# README — Plantilla LaTeX: Calendario 2025 (con números de semana)

**Descripción**

Este repositorio contiene una plantilla LaTeX para generar un calendario anual de **2025** con los números de la semana incluidos. Está pensada como plantilla limpia y fácil de personalizar (idioma, formato de días, resaltado de festivos, estilos de color, etc.).

---

## Contenido

* `calendar2025.tex` — Archivo LaTeX principal (plantilla).
* `README.md` — Este documento.
* `assets/` *(opcional)* — Carpeta para imágenes o iconos que quieras incluir en el calendario.

---

## Requisitos

Para compilar la plantilla necesitarás una instalación LaTeX completa que incluya al menos los siguientes paquetes (la mayoría vienen con distribuciones modernas como TeX Live o MikTeX):

* `pgf` / `tikz` (para dibujar el calendario y usar `pgfcalendar`).
* Paquetes de manejo de fechas (`datetime2` o similares) — la plantilla usa utilidades para calcular y mostrar números de semana.
* `babel` o `polyglossia` (para idioma).
* `fontenc`, `inputenc` (si usas pdfLaTeX) o usar XeLaTeX/LuaLaTeX con UTF-8 (recomendado si incluyes caracteres especiales).
* `xcolor` (colores), `geometry` (márgenes), `calc` y `fancyhdr` (cabeceras/pies), entre otros.

> Nota: la plantilla incluye comentarios indicando qué paquetes son necesarios; si tu distribución falta algún paquete, instálalo mediante el gestor de paquetes de tu distribución LaTeX.

---

## Cómo compilar

Recomendado (UTF-8, fuentes del sistema):

```bash
xelatex calendar2025.tex
xelatex calendar2025.tex
```

Si prefieres `pdflatex` (asegúrate de que el archivo usa `\usepackage[utf8]{inputenc}`):

```bash
pdflatex calendar2025.tex
pdflatex calendar2025.tex
```

Se recomienda ejecutar el compilador dos veces para asegurar referencias y numeración correctas.

---

## Uso y personalización rápida

La plantilla está organizada y comentada para facilitar los cambios más habituales:

1. **Idioma:** Cambia la opción en `babel` (por ejemplo `\usepackage[spanish]{babel}`) o usa `polyglossia` con XeLaTeX.
2. **Inicio de la semana:** Por defecto la plantilla viene con la semana comenzando en **lunes** (sistema ISO). Puedes cambiarlo a domingo ajustando la configuración dentro del bloque `pgfcalendar`.
3. **Números de semana:** La plantilla calcula y muestra los números de semana (ISO-8601) en un margen o columna dedicada. Si quieres ocultarlos, desactiva la opción `showweeknumbers` en la cabecera de configuración.
4. **Formato de días/meses:** Puedes modificar el formato (tamaño de fuente, alineación, color) desde la sección de estilos.
5. **Festivos/fechas especiales:** Hay un bloque para añadir festivos manualmente (lista de fechas). También puedes marcar rangos (vacaciones) para resaltarlos con un color de fondo.
6. **Estética:** Cambia paleta de colores, tipografías y márgenes en la sección de `preamble`.

---

## Ejemplos de personalización (breve)

* Cambiar el color principal:

```latex
% en el preamble
\definecolor{main}{HTML}{1F77B4}
```

* Ocultar números de semana:

```latex
% en la parte de configuración de la plantilla
\def\showweeknumbers{0}
```

* Añadir un festivo:

```latex
% en la lista de festivos
\newcommand{\festivos}{ {2025-01-01}, {2025-04-18}, {2025-12-25} }
```

---

## Problemas comunes y soluciones

* **Fechas o números de semana erróneos:** Ejecuta la compilación dos veces y revisa que la zona horaria / paquete de fechas está correctamente configurado.
* **Caracteres con acentos raros:** Usa XeLaTeX o añade `\usepackage[utf8]{inputenc}` si usas `pdflatex`.
* **Paquetes faltantes:** Instala los paquetes solicitados (ej. `pgf`, `datetime2`) desde el gestor de tu distribución LaTeX.

---

## Licencia

Esta plantilla se entrega bajo licencia **MIT**. Puedes usarla, modificarla y redistribuirla libremente, aunque se agradece mantener el crédito del autor si la publicas.

---

## Contacto

Si quieres que personalice la plantilla (añadir tu logo, festividades locales, diseño a medida), escríbeme y puedo ayudarte a adaptar el `.tex` a tus necesidades.

¡Listo! Genera tu PDF con la plantilla y tendrás un calendario completo para 2025 con números de semana incluidos.
