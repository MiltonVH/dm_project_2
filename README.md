# Proyecto No. 2 - DOCS

## Conjunto de datos

[Resultados de evaluaciones](https://edu.mineduc.gob.gt/digeduca/?p=resultadosevaluacionesMain.asp) para el año 2023 del Ministerio de Educación de Guatemala

## Estructura de archivos

A continuación se describen los archivos disponibles en el directorio raíz del repositorio así como la estructura de carpetas para que sea más fácil poder reproducirlo al momento de clonarlo. 

*Carpetas*

- `graphs` directorio donde se guardan la imágenes generadas por el código R.
- `p2_data` nombre del directorio donde los scripts de R buscan el conjunto de datos, es necesario crear esta carpeta manualmente y colocar en ella el *dataset* luego de clonar el repositorio debido que se encuentra excluida ( archivo `.gitingnore` ) para evitar cargar los datos al momento de realizar un commit. 

*R Markdown*

Tipos de archivos similares a Jupyther Notebooks que pueden ser manipulados y ejecutados directamente desde RStudio.

- `load_and_clean.Rmd` archivo inicial que hace una limpieza básica de los datos y permite serealizar el conjunto de datos en un archivo .Rds para poder recuperarlos más rápidamente cuando se esta trabajando en los otros scripts.
- `rforest.Rmd` contiene la implementación de bosques aleatorios
- `dtree.Rmd` contiene la implementación de árboles de decisión 

*Notebooks*

- `nnet.ipynb` contiene la implementación de redes neuronales para predicción. Fue elaborado con Google Colab. 

## Código 

En general al utilizar solamente archivos tipo **Notebook** que permiten separar el código en bloques o celdas para ejecutar individualmente, en todos los archivos que contiene la implementación de un modelo, se tienen bloques de código con encabezados que describen su funcionamiento. A continuación solamente se hará mención a algunas situaciones específicas para aclarar el funcionamiento general del código. 

### R

Librerías utilizadas en código 

- `library(here)` permite utilizar la función `here()` para evitar escribir paths largos al momento de leer o escribir archivos. 

- `library(foreign)` permite leer archivos .SAV `read.spss()` directamente como data frames. 

- `library(rpart)`permite utilizar las funciones  `rpart()` y `rpart.plot()` para entrenar modelos de árboles de decisión y gratinarlos respectivamente. 

- `library(randomForest)` permite utilizar la función `randomForest()` para entrenar modelos de bosques aleatorios.

- `library(dplyr)` librería que permite manipular data frames y encadenar operaciones mediante el operado `%>%`

Definición de función para limpiar la consola de R al ejecutar clc()

```r
clc <- function() shell("cls")
```

Bloque de código para limpiar las variables y datos cargados en la sesión.

```r
rm(list = ls())
```


### Python 

Copia del contenido en MyDrive luego de montarlo hacia el entorno de trabajo dentro de Google Colab 

```
!cp '/content/drive/MyDrive/temp/2023-Grad-Internet.sav' '/content/
```

Instalación de librería necesaria para la lectura de archivos .SAV mediante Pandas. 

```
!pip install pyreadsta
```








----------

- Universidad de San Carlos de Guatemala 
- Facultad de Ingeniería 
- Escuela de Estudio de Postgrado
 - *Maestría en ingeniería para la industria con especialidad en ciencias de la computación*
- Introducción a la minería de datos

----------