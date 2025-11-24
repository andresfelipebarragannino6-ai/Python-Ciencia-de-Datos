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

# Resultados y Hallazgos Clave:

Tienda,Facturación Total (COP),Calificación Promedio
Tienda 1,"$1,150,880,400.00",3.98 estrellas
Tienda 2,"$1,116,343,500.00",4.04 estrellas
Tienda 3,"$1,098,019,600.00",4.04 estrellas
Tienda 4,"$1,038,375,700.00",4.00 estrellas
