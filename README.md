
# Laboratorio 2A: Calidad de datos con un dataset real

## Ciencia de Datos e Inteligencia Artificial Aplicada

**Herramientas:** RStudio, R, tidyverse y Quarto.

## 1. Descripción del proyecto

Este repositorio contiene el desarrollo del Laboratorio 2A,
orientado a evaluar la calidad de una base de datos real
de películas y series.

El análisis se realizó utilizando RStudio y Quarto,
aplicando procedimientos reproducibles de diagnóstico,
limpieza, transformación y validación de datos.

## 2. Pregunta de investigación

¿Qué características de una producción audiovisual
(año, formato y género) se asocian con su calificación?

## 3. Base de datos

La base original contiene:

- 9,999 registros.
- 9 variables.
- Información sobre películas y series.
- Variables como MOVIES, YEAR, GENRE, RATING,
  ONE.LINE, STARS, VOTES, RunTime y Gross.

## 4. Metodología

Se desarrollaron las siguientes actividades:

1. Importación y diagnóstico inicial.
2. Evaluación de valores faltantes.
3. Transformación de variables y expresiones regulares.
4. Identificación de valores centinela.
5. Análisis de mecanismos MCAR, MAR y MNAR.
6. Identificación y tratamiento de duplicados.
7. Evaluación de valores atípicos.
8. Validación mediante reglas de calidad.
9. Análisis exploratorio por género, año y formato.
10. Registro de decisiones y reproducibilidad.

## 5. Principales resultados

| Indicador | Resultado |
|---|---:|
| Registros originales | 9,999 |
| Calificaciones faltantes | 1,820 |
| Duraciones faltantes | 2,958 |
| Sinopsis faltantes identificadas | 1,265 |
| Duplicados exactos | 431 |
| Registros sin copias exactas | 9,568 |
| Títulos únicos consolidados | 6,422 |
| Duraciones mayores a 300 minutos | 41 |

## 6. Resultados exploratorios

Los documentales presentaron una calificación
promedio de 7.10, seguidos por las producciones
de animación, con 6.92.

Las producciones de terror registraron una media de 4.90.

El indicador provisional de serie mostró una media de
7.14 para TRUE y 6.37 para FALSE.

Estos resultados son descriptivos y no permiten
establecer relaciones causales.

## 7. Archivos del repositorio

- `Laboratorio_2A_Quarto_completo.qmd`:
  código fuente y documento reproducible.

- `Laboratorio_2A_Quarto_completo.html`:
  informe generado mediante Quarto.

- `datos/raw/movies.csv` o `data/raw/movies.csv`:
  base original, según la estructura del repositorio.

- `datos/processed/` o `data/processed/`:
  archivos procesados y registro de decisiones.

- `base_datos_2.Rproj`:
  archivo de proyecto de RStudio.

## 8. Reproducibilidad

Para reproducir el laboratorio:

1. Descargar o clonar el repositorio.
2. Abrir el proyecto en RStudio.
3. Instalar los paquetes necesarios:
   dplyr, tidyr, readr, stringr, ggplot2 y knitr.
4. Verificar la ruta del archivo CSV original.
5. Abrir `Laboratorio_2A_Quarto_completo.qmd`.
6. Ejecutar Render para generar el informe HTML.

## 9. Limitaciones metodológicas

La consolidación por título constituye un criterio
provisional de identificación de obras.

El indicador de serie se construyó a partir del
patrón temporal de YEAR y no representa una
clasificación definitiva del formato.

Los mecanismos MAR y MNAR no pueden distinguirse
con certeza únicamente mediante los datos observados.

## 10. Conclusión

El laboratorio evidencia la importancia de evaluar
la completitud, validez, consistencia y unicidad de
los datos antes de efectuar análisis estadísticos
o implementar modelos de inteligencia artificial.

La documentación de las transformaciones y la
conservación de los datos originales permiten
fortalecer la transparencia y reproducibilidad
de la investigación.
