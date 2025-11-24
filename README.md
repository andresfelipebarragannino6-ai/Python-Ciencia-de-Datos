# Python-Ciencia-de-Datos

# Descripción del Proyecto:

## Este proyecto consiste en el análisis exploratorio de datos (EDA) para cuatro tiendas (Tienda 1, Tienda 2, Tienda 3 y Tienda 4) de AluraStore LATAM. El objetivo principal fue consolidar la información de ventas, aplicar ingeniería de características y calcular métricas clave de desempeño para comparar el rendimiento de cada tienda.

# Estructura del Análisis:

## El análisis se desarrolló en un entorno Python utilizando la librería pandas y siguió los siguientes pasos:

## Importación de Datos: Se cargaron cuatro archivos CSV (uno por tienda) desde repositorios remotos de GitHub.

## Unificación de Datos: Se concatenaron los cuatro DataFrames individuales en un único DataFrame combinado para facilitar el análisis global de las 9435 filas de datos.

## Ingeniería de Características: Se crearon nuevas columnas clave para el análisis:

## Ingresos (basada en el Precio).

## Reseñas (basada en la Calificación).

## Rendimiento de Ventas (cálculo adicional, potencialmente Ingresos/Cantidad de cuotas).

## Análisis de Métricas Clave: Se calcularon y compararon la facturación total, la calificación promedio y el costo promedio de envío entre las cuatro tiendas.

## Segmentación por Categoría: Se identificaron 8 categorías de producto únicas y se prepararon visualizaciones de datos para cada una de ellas para un análisis cualitativo posterior.

# Hallazgos Clave:

# Carga e Importación de Datos:

## El primer paso fue cargar la librería pandas y obtener los datos de cada tienda desde sus respectivas URL remotas.

# Código Python:

## import pandas as pd. 
## Explicación: "Importa la librería pandas, esencial para la manipulación y análisis de datos en DataFrames."

## "url = ""...""
## Explicación: ",Define las URLs de los archivos CSV para cada una de las cuatro tiendas.

## tienda = pd.read_csv(url)
## Explicación: "Carga cada archivo CSV desde su URL a un DataFrame individual (tienda, tienda2, tienda3, tienda4)."

# Unificación e Ingeniería de Características:

## Una vez cargados los datos, se combinaron en un único DataFrame para el análisis global y se crearon nuevas métricas.

# Código Python:

## "df_combined = pd.concat([tienda, tienda2, tienda3, tienda4], ignore_index=True)"
## Explicación: "Combina los cuatro DataFrames de tiendas en un solo DataFrame (df_combined), apilando las filas. El argumento ignore_index=True asegura un índice continuo y limpio."

## df_combined['Ingresos'] = df_combined['Precio']
## Explicación: "Crea la columna Ingresos, que es una copia directa de la columna Precio, representando la facturación bruta por venta."

## df_combined['Reseñas'] = df_combined['Calificación']
## Explicación: "Crea la columna Reseñas, que es una copia directa de la columna Calificación, para estandarizar el nombre."

## df_combined['Rendimiento de Ventas'] = df_combined['Ingresos'] / df_combined['Cantidad de cuotas']
## Explicación: "Crea la columna Rendimiento de Ventas para obtener el valor promedio de la venta por cuota, como una métrica de desempeño adicional."

# Cálculo de Métricas Clave:

## Se utilizó un bucle (for) para iterar sobre los DataFrames de cada tienda y calcular las métricas principales (Facturación Total y Calificación Promedio) de manera comparativa.

# Código Python:
## "dataframe = [tienda,tienda2,tienda3,tienda4]"
## Explicación: Lista que contiene los DataFrames individuales para facilitar la iteración.

## "for i, df in enumerate(dataframe):"
## Explicación: Inicia un bucle para procesar cada tienda.

## "df[""Precio""].sum()"
## Explicación: Calcula la Facturación Total de la tienda actual (suma de la columna Precio).

## df['Calificación'].mean()
## Explicación: Calcula la Calificación Promedio de la tienda actual (media de la columna Calificación).
