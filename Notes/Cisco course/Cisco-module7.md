### Modulo 7 - Introduccion a las consultas estructuradas
**Nota**: El modulo anterior no fue incluido debido a que fue un tema orientado a SQL. Sin embargo, este modulo esta siendo incluido debido a que contiene un tema que no comprendi mucho en mi clase de BD.

## Join
JOIN en SQL consiste en una consulta SQL para encontrar atributos de cada tabla que permiten que la consulta encuentre los registros relacionados correctos.

# Ejemplo - Recuperar reviews de una pelicula y mostrarlas con el titulo y el año de la pelicula
```text
SELECT m.title, m.year, r.AuthorName, r.Score, r.Comment, r.Date //aqui se mostrara esto como columnas
FROM Review AS r
JOIN Movie AS m 
  ON m.movieId = r.movieId;
```

**Explicando la consulta**: Con el SELECT seleccionamos las columnas que queremos usar de ambas tablas, el FROM apunto a la tabla que queremos, como queremos recupear las reseñas, la tabla apuntada sera la de Reviews, y el JOIN indica que se va a unir a tabla de Movie y despues igualamos los IDs para conectarlos.

# Join con mas de 2 tablas
Si se le quiere incluir el title y el year seria asi:
```text
SELECT m.title, m.year, gi.year, gi.month, gic.Country, gic.Amount
FROM Gross_Income AS gi
JOIN Movie AS m 
  ON m.movieId = r.movieId;
JOIN Gross_Income_Country AS gic
  ON gi.movieId = gic.movieId AND gi.year = gic.year AND gi.month = gic.month;
```

## Tipos de Join
# Inner join
Devuelve solo los registros de las filas que coinciden con ambas tablas.

# Ejemplo de consulta
# Tablas de referencia
**bike_sales** = Trans_ID, Cust_ID, Model, Color, Sale_Price

**bike_models** = ID, Model, Color_Option, Cost

```text
SELECT bike_sales.Trans_ID, bike_sales.Model, bike_sales.Sale_Price, bike_models.Cost
FROM bike_sales
INNER JOIN bike_models
ON bike_sales.Model = bike_models.Model;
```

# Full Join
Devuelve todas las filas de ambas tablas se devolveran en la salida. Cualquier fila de una tabla que no coincida en la otra contendra valores nulos.

# Ejemplo de consulta
```text
SELECT bike_sales.Trans_ID, bike_sales.Model, bike_sales.Sale_Price, bike_models.Cost
FROM bike_sales
FULL JOIN bike_models
ON bike_sales.Model = bike_models.Model;
```

# RIGHT JOIN
Devuelve todos los registros de la tabla de la derecha y solo los registros coincidentes de la tabla de la izquierda.

# Ejemplo de consulta
```text
SELECT bike_sales.Trans_ID, bike_sales.Model, bike_sales.Sale_Price, bike_models.Cost
FROM bike_sales // esta es la tabla ubicada en la izquierda
RIGHT JOIN bike_models // esta es la tabla ubicada en la derecha
ON bike_sales.Model = bike_models.Model;
```

# LEFT JOIN
Devuelve todos los registros de la tabla de la izquierda y solo los registros coindicentes de la tabla de la derecha.
```text
SELECT bike_sales.Trans_ID, bike_sales.Model, bike_sales.Sale_Price, bike_models.Cost
FROM bike_sales // esta es la tabla ubicada en la izquierda
LEFT JOIN bike_models // esta es la tabla ubicada en la derecha
ON bike_sales.Model = bike_models.Model;
```

# NATURAL JOIN
Con NATURAL JOIN, se puede combinar 2 tablas basadas en campos comnues que existen en ambas tablas. Se producen cuando hay una columna o columna que existen en ambas tablas con el mismo nombre de campo y de tipo de datos (los campos comunes no necesitan ser PK o FK en ninguna de las tablas).

De manera predeterminada, la salida de la conuslta es la misma que la salida de una expresion INNER JOIN, solo que solo incluye una instancia de las columnas comunes, a diferencia de la salida INNER JOIN, que puede tener columnas duplicadas.

# Ejemplo de consulta
```text
SELECT bike_sales.Trans_ID, bike_sales.Model, bike_sales.Sale_Price, bike_models.Cost
FROM bike_sales 
NATURAL JOIN bike_models;
```

En este caso, la union natural se realizara correctamente debido que ambas tablas tienen una columna denominada "Modelo" con un tipo de datos VARCHAR. Adicionalmente, como NATURAL JOIN unira implicitamente cualquier columna de ambas tablas que tenga el mismo nombre y tipo de datos, no es necesaria una condicion "ON".

