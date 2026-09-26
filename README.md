# Especificación de requisitos de software

Plantilla modular en LaTeX para una Especificación de Requisitos de Software (SRS), redactada en español y basada en la estructura de IEEE Std 830-1998.

## Estructura del proyecto

```text
.
├── main.tex
├── capitulos/
│   ├── 00_instrucciones.tex
│   ├── 01_ficha_documento.tex
│   ├── 02_introduccion.tex
│   ├── 03_descripcion_general.tex
│   ├── 04_requisitos_especificos.tex
│   └── 05_apendices.tex
├── imagenes/
└── fuente/
    └── Plantilla SRS IEEE 830-1998.doc
```

## Modularidad y edición

- `main.tex` contiene la configuración del documento, los paquetes, los comandos comunes, la portada, el índice y las instrucciones `\input` que incorporan los demás archivos. No se debe redactar allí el contenido de los capítulos.
- Cada archivo de `capitulos/` contiene una parte del documento. Los capítulos principales están separados en archivos individuales; sus apartados se organizan dentro de cada archivo con `\section` y `\subsection`.
- Para agregar contenido, edite el archivo del capítulo correspondiente. Para incorporar un capítulo nuevo, cree un archivo `.tex` en `capitulos/` y agregue su `\input{capitulos/nombre}` en `main.tex`, en el orden deseado.
- `imagenes/` es el lugar para guardar diagramas, capturas y otras imágenes. Puede insertarlas desde un capítulo con `\includegraphics{nombre-del-archivo}`; la ruta de imágenes ya está configurada en `main.tex`.
- `fuente/` conserva el documento Word original como referencia.

Las secciones de instrucciones y ficha también están en archivos independientes dentro de `capitulos/`, por lo que `main.tex` queda reservado para la portada, la configuración y el ensamblaje del documento.

## Compilación

Desde esta carpeta, use una distribución LaTeX que incluya los paquetes indicados en el preámbulo y compile dos veces para actualizar el índice:

```sh
pdflatex main.tex
pdflatex main.tex
```

Los campos pendientes se indican entre corchetes, por ejemplo, `[Inserte aquí el texto]`. Reemplace esos marcadores y retire las notas de orientación al completar la especificación.
