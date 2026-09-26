# Especificación de requisitos de software

Plantilla en LaTeX de una Especificación de Requisitos de Software (SRS), organizada por capítulos y redactada en español. Su estructura sigue la plantilla IEEE Std 830-1998 incluida originalmente como documento Word.

## Contenido

- `main.tex`: documento fuente completo, con portada, ficha del documento, índice automático, capítulos y campos editables.
- `fuente/Plantilla SRS IEEE 830-1998.doc`: archivo Word original utilizado como referencia.

## Compilación

Con una distribución LaTeX que incluya los paquetes usados en el preámbulo, compile dos veces para generar el índice y las referencias:

```sh
pdflatex main.tex
pdflatex main.tex
```

Los campos pendientes se indican entre corchetes, por ejemplo, `[Inserte aquí el texto]`. Reemplace esos marcadores y retire las notas de orientación al completar la especificación.
