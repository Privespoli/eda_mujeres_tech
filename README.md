# 🌍 Mujeres, empleo y tecnología: análisis exploratorio de datos (EDA)

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=for-the-badge)
![Plotly](https://img.shields.io/badge/Plotly-3F4F75?style=for-the-badge&logo=plotly&logoColor=white)
![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=black)

## 📌 Descripción del proyecto

Este proyecto tiene como objetivo explorar la participación de las mujeres en el sector de las tecnologías de la información y la comunicación (TIC), utilizando datos estadísticos públicos de países europeos.

Mediante técnicas de análisis exploratorio de datos (*Exploratory Data Analysis*, EDA), se estudia cómo varía la representación femenina entre países y cómo evoluciona a lo largo del tiempo.

El análisis utiliza un conjunto de datos con observaciones anuales entre **2016 y 2025**, lo que permite comparar diferentes países y detectar patrones, diferencias y posibles tendencias temporales.

El proyecto combina limpieza y preparación de datos, análisis estadístico y visualizaciones para transformar los datos en información comprensible.

## 🎯 Objetivos

- Analizar las diferencias en la participación femenina entre países.
- Estudiar la evolución temporal del indicador entre 2016 y 2025.
- Identificar países con porcentajes medios relativamente altos o bajos.
- Examinar la variabilidad del indicador entre países y años.
- Detectar patrones geográficos y temporales mediante visualizaciones.
- Identificar limitaciones y necesidades de información para interpretar correctamente los resultados.

## ❓ Preguntas de investigación

El análisis se estructura en torno a cuatro preguntas principales:

1. **¿Cómo varía la participación femenina entre países?**
2. **¿Qué cambios se observan a lo largo del tiempo?**
3. **¿Qué diferencias aparecen entre indicadores?**
4. **¿Qué información falta para entender mejor las diferencias observadas?**

Para responder a estas preguntas se utilizan estadísticas descriptivas, comparaciones entre países y diferentes tipos de gráficos.

> **Nota:** el análisis principal se centra en un único indicador. Para comparar indicadores diferentes será necesario incorporar variables adicionales y comprobar que sus definiciones y unidades sean compatibles.

## 📊 Datos utilizados

El conjunto de datos contiene información estadística sobre la participación femenina en el sector TIC.

Las variables principales utilizadas en el análisis son:

| Variable | Descripción |
|---|---|
| `pais` | País o entidad geográfica a la que corresponde la observación. |
| `anio` | Año de referencia del dato. |
| `porcentaje` | Porcentaje de mujeres entre los especialistas en TIC. |

El archivo original también contiene metadatos y campos auxiliares, que se revisan durante la preparación de los datos.

### Periodo analizado

- **Año inicial:** 2016.
- **Año final:** 2025.
- **Cobertura:** países y entidades geográficas europeas incluidas en la fuente.
- **Frecuencia:** anual.

### Fuente de datos

Los datos proceden de estadísticas públicas europeas sobre empleo y participación femenina en el sector tecnológico.

Fuente: [Eurostat — Base de datos estadísticos](https://ec.europa.eu/eurostat/web/main/data/database).

## 🧹 Preparación y limpieza de datos

Antes de realizar el análisis, se llevaron a cabo las siguientes tareas:

1. Importación del archivo CSV mediante Pandas.
2. Inspección de las dimensiones y estructura del conjunto de datos.
3. Revisión de los tipos de variables.
4. Comprobación de registros duplicados.
5. Identificación de valores ausentes.
6. Selección de observaciones correspondientes a mujeres y expresadas en porcentajes.
7. Selección de las columnas necesarias para el análisis.
8. Renombrado de variables para facilitar su interpretación.
9. Comprobación de la disponibilidad de observaciones por país y año.

Durante la revisión inicial se identificaron **3 valores ausentes en el indicador**, sobre un total de 353 registros filtrados, equivalentes aproximadamente al 0,85 %.

También se comprobó que no había registros duplicados por país y año en la tabla de trabajo.

Los países no tienen necesariamente la misma cantidad de observaciones disponibles, por lo que esta diferencia se tiene en cuenta al comparar sus promedios.

## 📈 Visualizaciones y análisis

El proyecto incluye diferentes visualizaciones para estudiar los datos desde perspectivas complementarias.

### 1. Ranking de países

**Tipo:** gráfico de barras horizontales.

Permite comparar el porcentaje medio de mujeres especialistas en TIC entre países e identificar aquellos con valores relativamente altos o bajos.

Para facilitar la comparación principal, se priorizan los países con al menos ocho observaciones disponibles.

### 2. Evolución temporal

**Tipo:** gráfico de líneas.

Representa la evolución anual del indicador entre 2016 y 2025.

Permite estudiar las variaciones a lo largo del tiempo y comparar trayectorias nacionales con el agregado de la Unión Europea cuando los datos están disponibles.

### 3. Mapa de calor

**Tipo:** *heatmap*.

Representa los porcentajes por país y año mediante una escala de colores.

Facilita la identificación visual de patrones temporales, diferencias geográficas y posibles cambios en la distribución del indicador.

### 4. Distribución de los porcentajes

**Tipo:** diagrama de cajas (*boxplot*).

Permite analizar la distribución de los valores en cada año, comparar medianas y examinar la dispersión entre países.

### 5. Relación entre promedio y variabilidad

**Tipo:** gráfico de dispersión.

Compara el porcentaje medio de cada país con su desviación estándar durante el periodo analizado.

Esta visualización permite distinguir entre países con porcentajes medios similares, pero con diferentes niveles de variabilidad temporal.

### 6. Mapa geográfico

**Tipo:** mapa coroplético interactivo.

Representa mediante colores el porcentaje medio de mujeres especialistas en TIC por país.

Permite explorar la distribución geográfica del indicador y consultar los valores de cada territorio.

La cobertura geográfica del mapa depende de los países incluidos en el conjunto de datos.

## 🛠️ Tecnologías utilizadas

- **Python:** lenguaje de programación utilizado para el análisis.
- **Pandas:** manipulación, limpieza y transformación de datos.
- **NumPy:** operaciones numéricas.
- **Matplotlib:** creación de gráficos.
- **Seaborn:** visualizaciones estadísticas.
- **Plotly:** mapas y visualizaciones interactivas.
- **Google Colab:** entorno de desarrollo del análisis.

## 🚀 Cómo ejecutar el proyecto

### Requisitos

Se necesita Python y las siguientes bibliotecas:

```bash
pip install pandas numpy matplotlib seaborn plotly
```

### Ejecución en Google Colab

1. Abre el notebook del proyecto en Google Colab.
2. Carga el archivo CSV con los datos.
3. Ejecuta las celdas en orden.
4. Revisa las tablas descriptivas y las visualizaciones.
5. Interpreta los resultados y documenta las conclusiones.

Si ejecutas el notebook fuera de Google Colab, tendrás que adaptar la ruta del archivo CSV a la ubicación donde lo hayas guardado.

## ⚠️ Limitaciones del análisis

Los resultados deben interpretarse teniendo en cuenta las siguientes limitaciones:

- **Datos ausentes:** algunos países no disponen de observaciones para todos los años.
- **Cobertura desigual:** los promedios de determinados países se calculan con menos observaciones.
- **Comparabilidad geográfica:** el archivo puede incluir agregados estadísticos además de países individuales.
- **Interpretación del indicador:** el porcentaje mide la representación de las mujeres entre los especialistas en TIC, no el número absoluto de mujeres que trabajan en tecnología.
- **Análisis descriptivo:** las diferencias observadas no permiten establecer por sí solas las causas de la desigualdad.
- **Comparación entre indicadores:** para investigar diferencias entre indicadores será necesario incorporar otras variables y verificar su comparabilidad.
- **Evolución temporal:** los cambios observados deben interpretarse teniendo en cuenta la metodología y la disponibilidad de datos de la fuente.

## 🔎 Próximos pasos

Como posibles ampliaciones del proyecto, se plantean:

- Incorporar indicadores adicionales relacionados con educación, empleo y brecha de género.
- Comparar la participación femenina en TIC con la participación de las mujeres en el empleo general.
- Estudiar la evolución de países concretos mediante series temporales.
- Investigar las diferencias entre países con indicadores socioeconómicos complementarios.
- Mejorar la cobertura geográfica si se dispone de datos comparables de otras regiones del mundo.
- Automatizar la generación de estadísticas y gráficos.

## 👩‍💻 Autora

Proyecto personal de análisis de datos desarrollado con Python y Google Colab.

## 📄 Licencia

La licencia del proyecto y las condiciones de reutilización de los datos deben definirse de acuerdo con las licencias aplicables al código, al trabajo y a la fuente estadística original.
