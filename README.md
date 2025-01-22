# Plantilla de Tesis Doctoral con Quarto

Este repositorio contiene una plantilla base para la elaboración de una tesis doctoral (o libro) utilizando [**Quarto**](https://quarto.org/). El objetivo principal es facilitar la estructura y el proceso de compilación, permitiendo centrarte en el contenido académico.

------------------------------------------------------------------------

## Objetivo

-   Proporcionar una estructura inicial para la escritura de una tesis o libro en formato Quarto.
-   Incluir archivos de ejemplo (`.qmd`) y un archivo `_quarto.yml` listo para configurar.
-   Simplificar el proceso de compilación a PDF (o HTML/EPUB) con unos pocos comandos.

------------------------------------------------------------------------

## Estructura del Proyecto

La estructura mínima de archivos es la siguiente:

```         
├── _quarto.yml          # Configuración principal de Quarto
├── index.qmd            # Documento base o introducción
├── prefacio.qmd         # Ejemplo de prefacio sin numeración
├── capitulo1.qmd        # Ejemplo de capítulo 1
├── capitulo2.qmd        # Ejemplo de capítulo 2
├── resultados.qmd       # Ejemplo de apartado de resultados
├── referencias.qmd      # Sección de referencias si se desea separar
├── referencias.bib       # Archivo de bibliografía
├── estilo-citas.csl     # (Opcional) Estilo de citas
└── README.md            # Este archivo con instrucciones
```

> Nota: Puedes renombrar o añadir otros capítulos o secciones según tu esquema de trabajo.

------------------------------------------------------------------------

## Requisitos Previos

1.  **Quarto**: Descárgalo e instálalo desde [quarto.org](https://quarto.org).
2.  **LaTeX**: Si deseas compilar a PDF, asegúrate de tener una distribución de LaTeX instalada:
    -   [TeX Live](https://www.tug.org/texlive/)
    -   [MiKTeX](https://miktex.org/)
    -   [TinyTeX](https://yihui.org/tinytex/) (instalable directamente en R).
3.  (Opcional) **R y RStudio**:
    -   Para un flujo de trabajo completo, puedes usar [RStudio](https://posit.co/products/open-source/rstudio/) y la integración con Quarto.

------------------------------------------------------------------------

## Cómo Usar la Plantilla

1.  **Clona este repositorio** o descárgalo como ZIP y descomprímelo.

    ``` bash
    git clone https://github.com/usuario/plantilla-tesis-quarto.git
    ```

2.  **Edita los archivos `.qmd`** con tu contenido:

    -   `index.qmd` puede funcionar como portada o introducción.
    -   `prefacio.qmd` está configurado como una sección sin numeración.
    -   `capitulo1.qmd`, `capitulo2.qmd`, etc., pueden ser capítulos con contenido académico.

3.  **Ajusta la configuración** en `_quarto.yml`:

    -   Título, autor, fecha y estructura de capítulos.
    -   Formato de salida (PDF, HTML, EPUB).
    -   Ajusta la bibliografía (`bibliography`) y el estilo de citas (`csl`) si corresponde.

------------------------------------------------------------------------

## Compilación

### Vía Terminal (CLI)

1.  Abre una terminal y navega a la carpeta del proyecto:

    ``` bash
    cd ruta/a/tu/proyecto
    ```

2.  Ejecuta el comando de compilación:

    ``` bash
    quarto render
    ```

    Esto generará un archivo PDF (u otro formato) en la misma carpeta.

### Vía RStudio

1.  Abre RStudio y selecciona `File > Open Project` para abrir la carpeta del proyecto.

2.  Asegúrate de que Quarto esté instalado y reconocido por RStudio (en la consola de R, prueba `system("quarto --version")`).

3.  Para compilar el libro, haz clic en el **botón "Render"** de la barra superior (si estás en un archivo `.qmd`) o ejecuta en la consola:

    ``` r
    quarto::quarto_render()
    ```

------------------------------------------------------------------------

## Personalización

-   **Portada**: Modifica `index.qmd` o crea un nuevo archivo `.qmd` para incluir portadas personalizadas.
-   **Dedicatorias y Agradecimientos**: Añade secciones sin numeración (`.unnumbered`) o ubícalas en `prefacio.qmd`.
-   **Estilo y Formato**: Ajusta parámetros en `_quarto.yml`, por ejemplo:
    -   `fontsize`, `papersize`, `geometry`, `classoption`, etc.
-   **Referencias y Bibliografía**:
    -   Ajusta `bibliography: referencias.bib` con tus propias referencias en formato BibTeX.
    -   Usa `[@nombreReferencia]` en el texto para citar.

------------------------------------------------------------------------

## Contribuciones y Soporte

Si encuentras errores o deseas contribuir con mejoras, por favor abre un *issue* o envía un *pull request*. Toda sugerencia es bienvenida.

------------------------------------------------------------------------

¡Disfruta escribiendo tu tesis con Quarto y ahorra tiempo en la maquetación!
