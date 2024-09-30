```markdown
# Uso de la Palabra Clave `DISTINCT` en SQL

## Descripción

La palabra clave `DISTINCT` en SQL se utiliza para devolver valores únicos de una columna, eliminando los duplicados. En este ejercicio, se exploran las diferentes maneras en que se puede utilizar `DISTINCT` para obtener resultados únicos de la tabla `books`.

La tabla contiene 350 libros, pero muchos de estos libros son escritos por los mismos autores. El objetivo es recuperar una lista de autores únicos, y posteriormente, una combinación única de autor y género.

## Instrucciones

### Paso 1: Seleccionar Autores Únicos

La primera tarea es escribir una consulta que devuelva una lista de todos los autores únicos en la tabla `books`. Para hacer esto, se utiliza la palabra clave `DISTINCT` en combinación con la columna `author`:

```sql
-- Seleccionar autores únicos de la tabla books
SELECT DISTINCT author
FROM books;
```

### Paso 2: Seleccionar Combinaciones Únicas de Autor y Género

En esta segunda parte del ejercicio, se actualiza la consulta para devolver combinaciones únicas de `author` y `genre`. Al seleccionar múltiples columnas con `DISTINCT`, SQL devolverá filas donde la combinación de valores en ambas columnas sea única.

```sql
-- Seleccionar combinaciones únicas de autor y género de la tabla books
SELECT DISTINCT author, genre
FROM books;
```

## Resultados

1. **Primera consulta**: Recupera una lista de todos los autores únicos. Incluso si un autor ha escrito varios libros, aparecerá una sola vez en el conjunto de resultados.
   
2. **Segunda consulta**: Recupera combinaciones únicas de autores y géneros. Si un autor ha escrito libros en diferentes géneros, aparecerá una vez por cada combinación de autor y género.

## Conclusión

El uso de la palabra clave `DISTINCT` es esencial cuando se desea obtener una lista única de valores y evitar la repetición en los resultados. Es especialmente útil en bases de datos con grandes volúmenes de datos donde puede haber duplicación de información en ciertos campos.