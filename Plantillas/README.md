# Plantillas y Orquestación

Este directorio contiene el núcleo del código fuente y los documentos dinámicos requeridos para la generación del análisis de vehículos más robados.

## Componentes Principales

- **`Informe_mas_robados.qmd`**: Notebook principal de Quarto. Contiene la lógica del Análisis Exploratorio de Datos (EDA), el código de visualización y el texto del informe.
- **`Orquestador.py`**: Script en Python encargado de ejecutar los archivos `.qmd` programáticamente, y gestionar la salida de los reportes hacia la carpeta `Salidas/`.
- **`Notas.qmd`** y **`utilidades.qmd`**: Documentos secundarios o de soporte para modularizar análisis específicos o funciones utilitarias.
- **`css/`**: Contiene las hojas de estilo utilizadas para personalizar el aspecto visual del reporte HTML generado.
- **Recursos Gráficos**: Imágenes y logos (como `logo-sura-blanco.svg`, `tablas_AACH.png`, etc.) integrados en el informe final.

## Funcionamiento del Orquestador

El archivo `Orquestador.py` actúa como el controlador principal durante la ejecución. Su flujo de trabajo consiste en:

1. Configurar y preparar el entorno para la ejecución del análisis.
2. Llamar a la CLI de Quarto mediante Python para compilar y renderizar los documentos `.qmd`.
3. Organizar los resultados y asegurar que el reporte final quede almacenado de forma correcta.

> [!WARNING]
> No ejecute `Orquestador.py` directamente desde este directorio si utiliza rutas relativas que dependen de la raíz del proyecto. Utilice siempre el script `Correr_orquestador.bat` ubicado en la carpeta principal superior.

## Modificación del Informe

Para actualizar el análisis, ajustar gráficos o agregar nuevas secciones, modifique directamente `Informe_mas_robados.qmd`. Este archivo utiliza bloques de código de Python combinados con Markdown para estructurar el resultado final. La configuración de formato, estilo y parametrización se define en el encabezado YAML del propio archivo.
