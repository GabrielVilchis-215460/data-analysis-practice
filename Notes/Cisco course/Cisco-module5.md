### Modulo 5 - Analizar los datos con estadísticas
Una muestra es representativa de la poblacion en estudio.

## Estadisticas
# Estadistica descriptiva
Se usan para describir o resumir los valores y las observaciones de un dataset o un conjunto de datos.

Las estadisticas descriptivas basicas pueden incluir el numero total de puntos de datos en un conjunto de datos, el rango de valores que existen para esos puntos de datos numericos o la cantidad de veces que aparece un valor determinado en un conjunto de datos. Las estadisticas descripticas tambien pueden responder preguntas sobre la aparicion de tendencias.

Los resultados de las estadisticas descriptivas se suelen representar en graficos circulares, graficos de barras o histogramas.

# Estadistica inferencial
Se usan para resumir hallazgos basados en datos que ya ha registrado u observado sobre una población. Sin embargo, hay situaciones en las que recopilar datos de una poblacion muy grande puede no ser siempre practico o incluso posible. Sin embargo, es posible estudiar una muestra representativa mas pequeña de una poblacion y utilizar estadisticas inferenciales para probar hipotesis y sacar conclusiones sobre la poblacion mas grande.

La estadistica inferencial es el proceso de recopilar, analizar e interpretar los datos obtenidos de una muestra para generalizar o predecir algo sobre una población. Cuando se utiliza una muestra representativa, pueden surgir preocupaciones metodológicas que deben abordarse.

# Estadisticas y macrodatos
Diferentes enfoques estadisticas se utilizan en el analisis de Big Data.
Las estadisticas descriptivas describen una muestra (es util para comprender los datos de la muestra y para determinar la calidad de los datos).

En el analisis de Big Data se utilizan con mucha frecuencia una serie de analisis inferenciales, los cuales son:
- Analisis de clúster -> Se utiliza para encontrar grupos de observaciones que sean similares entre si.

- Analisis de asociación -> Se utiliza para encontrar apariciones concurrentes de valores de diferentes variables.

- Analisis de regresión -> Se utiliza para cuantificar la relación, de haber alguna, entre las variaciones de una o mas variables.

## Tipos de visualizacion de datos
1. Graficos de linea -> Usar cuando un se tenga un dataset continuo, cuando la cantidad de puntos de datos sea alta, o mostrar la tendencia en los datos con el tiempo.

2. Graficos de columna -> Usar para mostra valores de una variable especifica en categorias similares.

3. Graficos de barras -> Usar cuando los nombres de cada punto de datos sean largos.

4. Graficos circulares -> Usar para mostrar la composicion de un total.

5. Graficos de dispersion -> Usar para demostrar el agrupamiento o identificar valores atipicos en los datos. Visualizar correlaciones o para mostrar la distribucion de muchos puntos de datos.

## Abordar anomalias en los datos
Antes de que pueda comenzar el análisis de datos, se debe dedicar un tiempo considerable a la limpieza de los datos. Durante la fase de limpieza de datos, puede encontrar valores atípicos o anomalías en los datos. Si es así, deben investigarse para que se puedan corregir los datos o se pueda comprender el significado del punto de datos periférico.

Un valor atipico se define como un valor o punto de datos que varia significativamente de otros, ya sea mucho menor o mucho mayor. Algunas veces los valores atipicos son errores, y otra veces representan una informacion importante.

En el proceso de análisis de datos, los valores atípicos que son el resultado de errores pueden conducir a anomalías en los resultados obtenidos, mientras que los valores atípicos que no son errores pueden ser muy importantes para un análisis.

## Uso de Excel para solucionar problemas con los datos
# Funcion BUSCARV (VLOOKUP)
VLOOKUP es una herramienta de análisis de datos muy poderosa dentro de Excel y es excelente cuando necesita encontrar información en una hoja de cálculo grande o si busca constantemente el mismo tipo de información.

VLOOKUP es la abreviatura de “vertical lookup” (búsqueda vertical) y es una función que busca en una columna (vertical) de una tabla un valor específico. Esto significa que los datos deben organizarse en una tabla donde cada fila tiene formas de datos diferentes pero relacionadas en cada columna. Si se especifica una coincidencia aproximada en la fórmula, la primera columna (la columna de búsqueda) debe ordenarse en orden numérico o alfabético.

Una función VLOOKUP consta de 4 piezas de información clave:

1. El valor para buscar
2. El rango en el que buscar
3. La columna del rango que contiene el valor que desea que devuelva la función
4. Una indicación de si la función debe devolver una coincidencia aproximada (VERDADERO o TRUE, en la función) o solo una coincidencia exacta (FALSO) del valor devuelto. El valor predeterminado de VLOOKUP es una coincidencia aproximada si no se especifica FALSO o FALSE en la función.

VLOOKUP busca un valor en la columna más a la izquierda de una tabla y, cuando se encuentra el valor, devuelve información de la misma fila pero en otra columna.

# Funcion XLOOKUP
XLOOKUP es una función de búsqueda más reciente, similar a VLOOKUP, que no está disponible en todas las versiones de Excel actualmente en uso. Con XLOOKUP, puede buscar en cualquier columna (no solo en la más a la izquierda de una tabla) un término de búsqueda y devolver un resultado de la misma fila. 

Una diferencia es que XLOOKUP devuelve de forma predeterminada una coincidencia exacta, mientras que VLOOKUP predeterminado es la coincidencia más cercana, a menos que se use la palabra clave FALSE. 

# Ejemplo
=IF(ISNA(VLOOKUP(B2,$A$2:$A$10,1,FALSE)),"Unique","Duplicate")

Arriba, la fórmula se modifica agregando las funciones IF y ISNA , y los valores Único y Duplicado. La función IF realiza comparaciones lógicas y la función ISNA busca celdas que contengan el mensaje de error #N/A. Juntos, le dicen a Excel que devuelva "Único" si la función VLOOKUP no encuentra ningún duplicado (y, por lo tanto, devuelve un error) y que devuelva "Duplicado" en caso contrario.

# Funcion LARGUE o k.esimo.mayor
Esta funcion devuelve los valores mas altos o mayores en un conjunto de datos.

# Funcion SMALL
Esta funcion devuelve los valores mas bajos o menores en un conjunto de datos.

# Consideraciones adicionales
Una vez que se identifican los valores atípicos, el siguiente desafío es qué hacer con ellos. Los valores atípicos pueden indicar errores en los datos o pueden ser datos válidos que deben investigarse para saber por qué parece ser una anomalía. Hay un par de formas en que un analista de datos puede lidiar con los valores atípicos.

1. Eliminarlos. En un conjunto de datos grande, la eliminación de algunos valores atípicos probablemente no afecte el análisis general. Sin embargo, es importante crear una copia de los datos para poder investigar qué causó los valores atípicos en primer lugar. En este ejemplo, se podría eliminar la fila 72 del conjunto de datos de ventas de bicicletas.

2. Normalícelos (ajuste su valor). El valor de los valores atípicos se cambia para estar ligeramente por encima del valor máximo en el conjunto de datos. Este es un buen método si no sesga los datos. Existen varios métodos estadísticos para normalizar los datos. Investigue los diversos métodos antes de ajustar aleatoriamente los valores de los datos. En el conjunto de datos de ventas de bicicletas de ejemplo, el valor de Order_Quantity del 19 de diciembre de 43 a 20 podría estar justo por encima del valor máximo de 19.