# AnalisisDeDatos

Repositorio academico con materiales de apoyo para una ruta formativa de ciencia de datos. El contenido esta organizado por modulos y combina libretas de Google Colab, documentos de referencia, una presentacion introductoria y un conjunto de datos en CSV.

## Objetivo del repositorio

Centralizar material didactico para trabajar conceptos de:

- fundamentos estadisticos para ciencia de datos
- analisis exploratorio de datos
- machine learning aplicado
- deep learning para clasificacion de imagenes
- proyecto integrador con flujo de trabajo por etapas

## Estructura del proyecto

```text
Modulos/
|-- Introduccion/
|   |-- DataSeet/
|   |   `-- MuertesMaternas .csv
|   |-- Libreta Colab/
|   |   `-- IntroduccionCienciaDeDatos.ipynb
|   `-- Intro a las Mates de la Ciencia de Datos.pptx
|-- Modulo1/
|   |-- LibretasCollab/
|   |   |-- Modulo1-LibretaColabConCodigo.ipynb
|   |   `-- Modulo1-LibretaColabSinCodigo.ipynb
|   `-- Modulo1-CienciaDeDatos-EDA.docx
|-- Modulo2/
|   |-- LibretasCollab/
|   |   |-- Modulo2-LibretaConCodigoSinRespuestas.ipynb
|   |   |-- Modulo2-LibretaConCodigoYRespuestas.ipynb
|   |   `-- Modulo2-LibretaSinCodigoYRespuestas.ipynb
|   `-- Modulo2-MachineLearning.docx
|-- Modulo3/
|   |-- LibretasCollab/
|   |   |-- Modulo3-LibretaConCodigoYRespuestas.ipynb
|   |   `-- Modulo3-LibretaSinCodigoYRespuestas.ipynb
|   `-- Modulo3-DeepLearning.docx
`-- Modulo4/
    |-- LibretasCollab/
    |   |-- Modulo4-LibretaConCodigoYRespuestas.ipynb
    |   `-- Modulo4-LibretaSinCodigoYRespuestas.ipynb
    `-- Modulo4-ProyectoIntegrador.docx
```

## Contenido por modulo

### Introduccion

- Libreta: `IntroduccionCienciaDeDatos.ipynb`
- Enfoque: media, mediana, moda y analisis introductorio con el caso de mortalidad materna
- Dataset local incluido: `Modulos/Introduccion/DataSeet/MuertesMaternas .csv`
- Material complementario: `Intro a las Mates de la Ciencia de Datos.pptx`

Nota: esta libreta fue preparada para Google Colab y contiene montaje de Google Drive (`/content/drive`).

### Modulo 1: Ciencia de Datos y EDA

- Documento base: `Modulo1-CienciaDeDatos-EDA.docx`
- Libretas disponibles:
- `Modulo1-LibretaColabConCodigo.ipynb`
- `Modulo1-LibretaColabSinCodigo.ipynb`
- Temas detectados:
- carga de librerias y datos
- exploracion inicial
- estadistica descriptiva basica
- deteccion de valores nulos

### Modulo 2: Machine Learning aplicado a E-commerce

- Documento base: `Modulo2-MachineLearning.docx`
- Libretas disponibles:
- `Modulo2-LibretaConCodigoSinRespuestas.ipynb`
- `Modulo2-LibretaConCodigoYRespuestas.ipynb`
- `Modulo2-LibretaSinCodigoYRespuestas.ipynb`
- Flujo de trabajo cubierto:
- descarga de dataset desde UCI con `fetch_ucirepo(id=468)`
- exploracion y preparacion de datos
- entrenamiento de modelos supervisados
- comparacion entre Decision Tree, Random Forest y XGBoost
- registro de experimentos con MLflow
- exportacion de pipeline
- despliegue minimo como API REST con FastAPI

Nota: parte del contenido de este modulo asume instalacion de dependencias en Colab y uso opcional de `ngrok` para exponer la API.

### Modulo 3: Deep Learning

- Documento base: `Modulo3-DeepLearning.docx`
- Libretas disponibles:
- `Modulo3-LibretaConCodigoYRespuestas.ipynb`
- `Modulo3-LibretaSinCodigoYRespuestas.ipynb`
- Caso de estudio: clasificacion de imagenes con Fashion-MNIST
- Temas detectados:
- preprocesamiento de datos
- modelo base MLP
- modelo principal CNN
- comparacion de arquitecturas y evaluacion

### Modulo 4: Proyecto integrador

- Documento base: `Modulo4-ProyectoIntegrador.docx`
- Libretas disponibles:
- `Modulo4-LibretaConCodigoYRespuestas.ipynb`
- `Modulo4-LibretaSinCodigoYRespuestas.ipynb`
- Estructura observada:
- configuracion inicial
- agente 1: analisis exploratorio de datos
- agente 2: limpieza de datos
- continuacion del flujo integrador sobre modelado y entrega final

## Tipos de materiales incluidos

- `10` libretas `ipynb`
- `4` documentos `docx`
- `1` presentacion `pptx`
- `1` archivo de datos `csv`

## Requisitos sugeridos

El repositorio no incluye actualmente un `requirements.txt` o entorno reproducible. A partir de las libretas, las dependencias mas usadas son:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `tensorflow`
- `xgboost`
- `mlflow`
- `fastapi`
- `uvicorn`
- `ucimlrepo`
- `pyngrok`
- `nest_asyncio`

## Forma recomendada de uso

### Opcion 1: Google Colab

Recomendada para este material, porque varias libretas ya fueron disenadas para ese entorno y algunas incluyen comandos `!pip install` o referencias a Google Drive.

### Opcion 2: Jupyter local

Posible si se ajustan rutas y dependencias. En particular:

- la libreta de introduccion usa una ruta de Drive que debe reemplazarse por la ruta local del CSV
- el modulo 2 depende de paquetes adicionales para MLflow, FastAPI y despliegue
- algunas salidas guardadas en las libretas provienen de ejecuciones previas en Colab

## Observaciones del estado actual

- No hay codigo Python modular separado del material de notebooks; la mayor parte de la logica vive dentro de las libretas.
- No se encontro un archivo `README.md` previo.
- No se detecto un archivo de licencia ni un entorno de dependencias versionado.
- En `Modulo2`, la API con FastAPI aparece construida dentro de la libreta y no como archivo independiente del repositorio.

## Publico objetivo

Este repositorio esta orientado a:

- estudiantes que cursan una introduccion practica a ciencia de datos
- docentes que requieren material guiado con y sin respuestas
- personas que desean seguir una progresion desde estadistica descriptiva hasta modelos de aprendizaje automatico y profundo

## Proximas mejoras recomendadas

- agregar `requirements.txt` o `environment.yml`
- renombrar carpetas para homogeneizar nombres como `LibretasCollab`, `Libreta Colab` y `DataSeet`
- mover artefactos reutilizables del modulo 2 a archivos fuente independientes
- incluir licencia, instrucciones de contribucion y ejemplos de ejecucion por modulo
