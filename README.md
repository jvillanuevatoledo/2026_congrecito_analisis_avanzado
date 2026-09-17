**TALLER DE ANÁLISIS AVANZADO DE CITOMETRÍA DE FLUJO**

Bienvenidos al repositorio oficial del taller de análisis avanzado de citometría de flujo utilizando lenguajes y herramientas de programación en R.
En este taller, aprenderemos a utilizar el lenguaje de programación de R para analizar y visualizar datos de citometría de flujo.

Para participar en este taller, es importante que tengas instalado en tu equipo tanto R como Positron.

1. **INSTALACIÓN DE R Y POSITRON**

La versión de R con la que se trabajará es la **4.6.1**.

En macOS con chip Apple Silicon M1/M2/M3, asegurarse de descargar la versión ARM64 de R.

 -	**R**: Descargarlo e instalarlo desde [CRAN](https://cran.r-project.org/).
 -	**Positron**: Descargarlo e instalarlo desde el sitio oficial de [Positron](https://positron.posit.co/).


2. **INSTALAR HERRAMIENTAS DE COMPILACIÓN DE PAQUETES**

Según el sistema operativo receptor.

Muchos paquetes de R (especialmente en bioinformática y citometría) necesitan compilar código C/C++ o Fortran durante la instalación:
  - En **Windows**:
Descargar e instalar [Rtools](https://cran.r-project.org/bin/windows/Rtools/) (debe coincidir con la versión de R instalada, para la versión de R 4.6.1 se debe instalar [Rtools 4.5](https://cran.r-project.org/bin/windows/Rtools/rtools45/rtools.html).
  - En **macOS**:
Abrir la aplicación Terminal del sistema y ejecutar:

```bash
xcode-select --install
```

Seguir las instrucciones emergentes en pantalla para instalar las herramientas de línea de comandos de Xcode.

3. **EN POSITRON ABRIR LA CARPETA**
  - Descomprimir el archivo `.zip` recibido (o clonar este repositorio de GitHub).
  - Abrir Positron.
  - Ir a File > Open Folder... (o Ctrl + K, Ctrl + O en Windows / Cmd + O en macOS) y seleccionar la carpeta del proyecto.
Verificación: Al abrir la carpeta, Positron leerá automáticamente el archivo `.Rprofile` y en la consola de R aparecerá un mensaje indicando que el entorno renv se ha activado.

4. **RESTAURAR EL ENTORNO VISUAL EXACTO**:

**Windows** y **macOS**: En la consola de R dentro de Positron ejecutar:

```R
renv::restore()
```

  - El sistema leerá el archivo `renv.lock` y preguntará en la consola si desea proceder a descargar e instalar los paquetes. Escribir y (o yes) y presionar Enter.
  - `renv` descargará e instalará automáticamente las versiones exactas de las librerías necesarias.
Verificación: La consola mostrará el mensaje * The library has been successfully restored.


📂 **ESTRUCTURA DEL REPOSITORIO**

**datos/**: Conjuntos de datos de ejemplo (archivos .fcs o matrices procesadas) utilizados durante las prácticas.

**scripts/**: Código en R comentado paso a paso para el control de calidad, compensación, transformación, gating automatizado y reducción de dimensionalidad (t-SNE, UMAP).

**notebooks/**: Documentos interactivos (R Markdown / Quarto) con la explicación teórica y los resultados visuales de los flujos de trabajo.

**docs/**: Documentación complementaria, lecturas recomendadas y referencias bibliográficas.
