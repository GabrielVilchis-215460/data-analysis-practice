### Modulo 4 - Transformando datos con Excel
## Calculos de datos
Los cálculos se pueden realizar en una constante, como el número 5, o en los datos contenidos en una ubicación específica (generalmente una celda o un rango de celdas). Por ejemplo, la fórmula = L1/L7 divide el valor de la celda L1 entre el valor de la celda L7.

Dentro de una fórmula o función, cuando hay referencias de celda o rango, pueden ser relativas o absolutas. Una referencia es relativa cuando su valor depende de la ubicación de la referencia, mientras que una referencia absoluta se refiere a la misma celda o rango sin importar dónde aparezca la referencia. 

Por ejemplo, cuando realizó la práctica de laboratorio Manipulación de Datos, copió y pegó las fórmulas de una fila en las filas inferiores. Cuando hizo eso, debido a que las fórmulas tenían referencias relativas, usaron los valores de las filas inferiores para realizar los cálculos para esas filas. Este es el comportamiento predeterminado para fórmulas y funciones.

Si desea que una fórmula haga referencia a la misma celda o rango de celdas sin importar dónde se pegue la fórmula, puede hacer que la referencia sea absoluta agregando un signo de dólar ($) antes del indicador de columna o fila para esa referencia. Usemos el ejemplo mencionado anteriormente, = L1/L7. Si quisiera usar esta fórmula en varios lugares en su hoja de cálculo y siempre usar los valores en L1 y L7, en lugar de los valores que corresponden a la nueva ubicación de la fórmula, la escribiría como =$L$1/$L$7.

## Funciones nuevas
# CONCAT
La función CONCAT, abreviatura de “concatenar”, une cadenas de texto. La función puede incluir cadenas de texto reales entre comillas, así como referencias de celdas y rangos. También le permite combinar diferentes tipos de datos como números, fechas y cadenas de texto en una sola celda.

Un caso de uso de la función CONCAT es combinar diferentes piezas de información importante para que un humano pueda leer de un vistazo, en lugar de ir a varias columnas para encontrar esta información

# LEFT o IZQUIERDA
La función IZQUIERDA (LEFT) devolverá una cantidad específica de caracteres desde el inicio (izquierda) de una cadena de texto.

# RIGHT o DERECHA
La función DERECHA (RIGHT) devolverá un número específico de caracteres desde el final (derecha) de una cadena de texto.

# MID o EXTRAE
La función EXTRAE (MID) devolverá una cantidad específica de caracteres desde el medio de una cadena de texto.

Excel tiene muchas funciones estadísticas integradas que pueden realizar todo tipo de cálculos matemáticos y estadísticos. Algunas de las funciones estadísticas más comunes utilizadas por los analistas de datos incluyen CONTAR (COUNT), CONTAR.BLANCO (COUNTBLANK), CONTARA (COUNTA), CONTAR.SI (COUNTIF), PROMEDIO.SI (AVERAGEIF), MIN.SI.CONJUNTO (MINIFS) y MAX.SI.CONJUNTO (MAXIFS). 

# COUNT
La función CONTAR (COUNT) en Excel devuelve el conteo, o número, de valores numéricos en un conjunto o rango de celdas o valores. Esto significa que cuenta celdas con números y fechas, pero no celdas en blanco o de texto.

# COUNTBLANK
La función CONTAR.BLANCO (COUNTBLANK) devuelve el recuento de celdas en blanco en un rango de celdas.

# COUNTA
La función CONTARA (COUNTA) devuelve el recuento de celdas que no están en blanco en un rango, ya sea que las celdas contengan valores numéricos o valores de texto.

# COUNTIF
La función CONTAR.SI (COUNTIF) devuelve el recuento de celdas que cumplen con un criterio específico.

# AVERAGEIF
La función PROMEDIO.SI (AVERAGEIF) encuentra el promedio de todas las celdas de un rango que cumplen con un criterio determinado. 

# MINIFS - MAXIFS
La función MIN.SI.CONJUNTO (MINIFS) en Excel devuelve el valor mínimo de un conjunto de valores especificados por uno o más criterios. La función MAX.SI.CONJUNTO (MAXIFS) devuelve el valor máximo de un conjunto de valores especificados por uno o más criterios.

## Tablas dinamicas
Las tablas dinamicas o Pivot Tables son una funcion de Excel que es invaluable para los analistas de datos. Las tablas dinámicas proporcionan una manera de resumir, analizar, explorar y presentar datos automáticamente. Los gráficos dinámicos le permiten agregar visualizaciones a los datos en una tabla dinámica. Con estas herramientas integradas, puede identificar tendencias, hacer comparaciones entre elementos de datos y crear gráficos en diferentes estilos para visualizar sus datos.