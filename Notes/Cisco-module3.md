### Modulo 3 - Preparación y limpieza de datos para el análisis
## Fuentes de datos
Existen muchas fuentes diferentes de datos, se puede encontrar una gran cantidad de datos históricos de archivos, como documentos en MS Word, correos electrónicos, hojas de cálculo, MS PowerPoints, PDFs, HTML y archivos de texto sin formato.

La selección de datos relevantes para su análisis incluye determinar el tipo de datos que necesita y encontrar una fuente para los datos. Al seleccionar datos para un proyecto, es importante centrarse en encontrar datos que puedan proporcionar información sobre su pregunta comercial original

## Worksheet links en Excel
La función de vinculos a libros o Workbook Links de Excel para crear enlaces externos y garantizar que los datos de las varias hojas de trabajo permanezcan sincronizados.

Para usar esta función, es necesario tener un libro de excel vacio y otro libro con los datos, y en la celda A1 se le pondrá el simbolo de "=" y en el libro que contiene los datos, simplemente se selecciona el contenido que se quiere copiar y posteriormente se presiona Enter y ya estarian vinculados.

## Datos estáticos y de transmisión en tiempo real
# Datos estáticos
Son aquellos datos que se reciben y se almacenan antes de realizar un análisis de los datos.

# Datos de transmisión en tiempo real (streaming)
Son aquellos datos que cuando cada evento se procesa y se analiza a medida que se recibe y los resultados posteriores se utilizan o almacenan.

## Tipos y formatos de datos
# Tipos de datos
1. Cadena
2. Entero
3. Punto flotante
4. Fecha y hora
5. Booleano

# Formatos de datos
Estandar           Representación                   Ejemplo
ISO 8601           AAAA-MM-DDthh:mm:mm+|-ss:mm      2023-01-20T15:20:09
RFC 1123           DÍA DD-MM-AAAA hh:mm:ss GMT|UT   Vie 20 Jan 2023 20:20:27 GMT
Norteamericano     MM/DD/AAAA hh:mm:ss AM|PM        01/20/2023 3:20:09 PM

## Datos en archivos estructurados
Los datos estructurados se refieren a datos que se ingresan y mantienen en campos definidos dentro de un archivo o un registro. Estos se introducen, clasifican, consultan, y analizan con facilidad mediante una computadora.

# Características
- Estructura bien definida y organizada.
- Se puede almacenar en tablas, generalmente dentro de coloumnas verticales y filas horizontales.
- Se documenta el contenido y el formato de los datos.
- Esta organizado en archivos, registros y campos.
- Se puede buscar, clasificar y consultar.
- Los controles de entrada pueden reducir la posibilidad de datos no válidados.

# Tipos de archivos estructurados
1. BD relacionales

2. Registros -> Los archivos de registro son un registro historico generado por una máquina de todo lo que sucede dentro de un sistema, como transacciones, errores o intrusiones. Los archivos de registro generalmente se consideran datos estructurados, ya que se generan automáticamente y, por lo tanto, se adhieren a un formato estándar.

3. Hojas de cálculo

4. Lecturas de sensores -> La salida del sensor generalmente se recopila en un formato estandarizado, que puede variar según el fabricante. Las lecturas individuales pueden estar seperadas solo por un delimitador o pueden depender del tiempo, como 1 salida por segundo, separadas por marcas de tiempo.

5. Registros transaccionales -> Los registros de transacciones se pueden almacenar en muchos formatos diferentes, segun el tipo de transaccion y su origen. Algunas transacciones se ingresan manualmente en formularios, mientras que otras pueden generarse automaticamente.

# Archivos CSV
Los archivos de valores separados por comas (CSV) son un tipo de archivo de texto sin formato ampliamente utilizado para estandarizar los datos. Los archivos CSV usan comas u otros caracteres, como tabulaciones, espacios o 2 puntos, para separar columnas en una tabla de datos y el carácter de nueva línea para separar filas.

Se usan comúnmente para importar y exportar datos a hojas de cálculo y bases de datos tradicionales, pero también se pueden usar como entrada para programas de análisis y herramientas de visualización.

Cada fila tambíen se puede denominar como un "registro".

# Archivos JSON y XML
JSON (JavaScript Object Notation) y XML (lenguaje de marcado extensible) también son tipos de archivos de texto sin formato estandarizados y comunes que se usan a menudo para representar registros de datos.

# JSON
JSON es un formato ligero de intercambio de datos fácil de leer y escribir para los humanos.

# XML
XML es un lenguaje de marcado similar a HTML. Estos formatos de archivo son compatibles con una amplia gama de aplicaciones. La conversión de datos en un formato común es una manera valiosa de combinar datos de diferentes orígenes.

## Datos no estructurados
El Big Data requiere un enfoque diferente en cuanto al análisis, el cómputo y los mecanismos de almacenamiento.

Los datos no estructurados carecen de la organización de los datos estructurados, son datos sin procesar, no organizados de una manera predefinida. No poseen un esquema fijo que identifique el tipo de datos o su formato. Este tipo de datos carecen de una forma establecida de ingresarlos o agruparlos y luego analizarlos.

# Fuentes de datos no estructurados
- BD NoSQL y Data Lakes -> Los datos no estructurados a menudo se almacenan en BD NoSQl o en Data Lakes, que son repositorios centralizados para datos obtenidos de dispoistivos IoT, sitios web, apps moviles, medios sociales y otras fuentes de datos sin procesar. Estos tipos de repositorios se utilizan para almacenar datos en tiempo real en su formato original.

- Extracción de datos web -> Las herramientas de extracción de datos (web scraping) extraen automáticamente diversas formas de datos de páginas HTML. Normalmente, la extracción web es un proceso automatizado que utiliza un bot o rastreador web para recopilar y copiar datos específicos de la web a una base de datos o una hoja de cálculo. Los datos pueden luego analizarse fácilmente.

- APIs -> Muchos grandes proveedores de servicios web, como Facebook, proporcionan interfaces estandarizadas para recopilar datos de ellos automáticamente, utilizando API. El enfoque más común es utilizar interfaces de programación de aplicaciones (API) RESTful. Las API RESTful utilizan HTTP como protocolo de comunicación y archivos JSON para almacenar los datos. Los sitios web de Internet como Google y Twitter recopilan grandes cantidades de datos estáticos y en streaming. Las API de estos sitios permiten a los analistas e ingenieros de datos acceder a subconjuntos de las grandes cantidades de datos que generan constantemente.

## Preparación de datos
Para que los datos esten en un formato utilizable, es posible que primero deban limpiarse. La limpieza de datos puede implicar eliminar cualquier dato no deseado, cambiar datos incorrectos y completar cualquier dato faltante. Una vez que se limpian los datos, se pueden buscar, analizar y visualizar.

# Procesos ETL y ELT
ETL y ELT son dos versiones del mismo proceso para mover datos a través de una canalización. Contienen los mismos pasos pero en diferentes órdenes para diferentes casos de uso.

# ETL
La Extracción, Transformación y Carga (ETL) es un proceso para recopilar datos de esta variedad de fuentes, transformarlos y luego cargarlos en una BD.

En un proceso de ELT, los pasos de carga y transformación se invierten, ELT permite que los datos sin procesar omitan el paso de transformación y vayan directamente al almacenamiento de forma no estructurada. La transformación se produce en los datos almacenados a medida que se utilizan. Este proceso se usa principalmente para grandes cantidades de datos no estructurados.

# Pasos del ETL
1. Extraer: Los datos se ubican y recopilan de varias fuentes para convertirse a un formato único para el analisis. Los datos pueden extraese de una BD relacional, BD NoSQL, archivos sin formato, archivos XML u otros formatos.

2. Transformar: Los datos generalmente deben transformarse antes de poder cargarse en un depósito de datos para su análisis. El paso de transformación utiliza reglas para transformar los datos de origen al tipo de datos necesario para la base de datos de destino. Esto incluye la conversión de cualquier dato medido a la misma dimensión (por ejemplo, imperial a métrico). El paso de transformación también requiere varias tareas adicionales. Algunas de estas consisten en combinar datos de varios orígenes, agregar, clasificar, determinar nuevos valores que se calculan de datos agregados y luego aplicar reglas de validación.

Los datos (que posiblemente incluyan algunos datos vacíos o con errores) pueden pasar por otra parte del paso de transformación conocida como “limpieza” o “depuración” de datos, y la validación le permite saber si los datos necesitan limpieza. Algunos ejemplos de limpieza de datos son la eliminación de registros en blanco y la estandarización de formatos como la fecha, la hora y la ubicación. La parte de limpieza del paso de transformación garantiza aún más la uniformidad de los datos de origen.

3. Carga: Luego, los datos transformados se cargan en la base de datos para realizar consultas. El proceso de carga real varía ampliamente, dependiendo de los tipos de datos de origen, el tipo de base de datos de destino y el tipo de consulta que se debe realizar. Algunas organizaciones también pueden sobrescribir datos existentes con datos acumulativos más nuevos. Durante el paso de carga, se aplican las reglas que se han definido en el esquema de base de datos. Estas reglas verifican las características necesarias, como la unicidad y la coherencia de los datos, o que los campos obligatorios no estén vacíos. Estas reglas ayudan a garantizar que la carga y cualquier consulta posterior de los datos sea correcta.

## Funciones utiles para la limpieza de datos en excel
=MAYUSC(dirección de celda) - para conversión a mayúsculas

=MINUSC(dirección de celda) - para conversión a minúsculas

=NOMPROPIO(dirección de celda): para la conversión a mayúsculas en la primera letra de cada palabra.

=LARGO() o LEN() = Longitud

=ESPACIOS() o TRIM() = Elimina espacios