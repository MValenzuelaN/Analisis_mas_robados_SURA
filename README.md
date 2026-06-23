# Análisis de Vehículos Más Robados SURA

Automatización del análisis exploratorio de datos (EDA) para identificar las marcas y modelos de vehículos más robados en el último trimestre. Este proyecto utiliza un flujo de trabajo basado en Python y Quarto para procesar datos, generar visualizaciones y construir reportes HTML reproducibles.

## Descripción del Proyecto

El objetivo principal es proporcionar un reporte claro, detallado y parametrizable sobre los siniestros de robo de vehículos. La arquitectura separa los datos de entrada, las plantillas de análisis y los reportes generados para mantener el proyecto organizado y facilitar su ejecución periódica.

## Estructura del Repositorio

- `Entradas/`: Directorio destinado a los archivos de datos crudos requeridos para el análisis.
- `Plantillas/`: Contiene los notebooks de Quarto (`.qmd`), scripts de Python (`Orquestador.py`) y recursos estáticos (CSS, imágenes) que definen la lógica del reporte.
- `Salidas/`: Carpeta donde se almacenan los reportes HTML generados tras cada ejecución.
- `Correr_orquestador.bat`: Script de Windows para ejecutar el proceso de análisis completo.
- `pyproject.toml`: Archivo de configuración que define las dependencias del proyecto (Pandas, Polars, Plotly, Jupyter, etc.).

## Requisitos Previos

Para ejecutar este proyecto, es necesario contar con:

- Python 3.13 o superior.
- [Quarto CLI](https://quarto.org/docs/get-started/) instalado en el sistema.
- Las dependencias listadas en `pyproject.toml`.

> [!NOTE]
> Se recomienda el uso de entornos virtuales para gestionar las dependencias del proyecto y evitar conflictos con otras instalaciones de Python.

## Ejecución del Análisis

El proceso se ha simplificado mediante un archivo por lotes. Para generar un nuevo reporte:

1. Asegúrese de que los últimos datos estén ubicados en la carpeta `Entradas/`.
2. Ejecute el archivo `Correr_orquestador.bat` ubicado en la raíz del proyecto.
3. El script inicializará el orquestador (`Plantillas/Orquestador.py`), el cual se encargará de ejecutar las plantillas de Quarto con los nuevos datos.
4. Una vez finalizado sin errores, el reporte HTML actualizado estará disponible en la carpeta `Salidas/`.

> [!IMPORTANT]
> El archivo `Correr_orquestador.bat` mostrará la salida del proceso en tiempo real. En caso de error, revise la consola antes de cerrarla para obtener detalles sobre el fallo.
