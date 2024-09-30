```markdown
# Consultando la Tabla `books` en SQL

## Descripción

En este ejercicio, se practica el uso de las consultas SQL básicas para recuperar datos de la tabla `books` utilizando las palabras clave `SELECT` y `FROM`. Estas palabras clave son fundamentales en SQL para seleccionar campos específicos y determinar de qué tabla se extraerán los datos.

## Instrucciones

### Paso 1: Seleccionar todos los títulos de los libros

Se utiliza la consulta SQL para recuperar todos los títulos de la tabla `books`. La instrucción `SELECT` permite elegir qué campos se van a incluir en el conjunto de resultados, mientras que `FROM` especifica la tabla de donde se extraen estos datos.

```sql
-- Devolver todos los títulos de la tabla books
SELECT title 
FROM books;
```

### Paso 2: Seleccionar los campos `title` y `author`

Para recuperar múltiples campos en la consulta SQL, se enumeran los nombres de los campos separados por comas después de la instrucción `SELECT`. En este caso, se seleccionan tanto el título como el autor de los libros:

```sql
-- Seleccionar título y autor de la tabla books
SELECT title, author
FROM books;
```

### Paso 3: Seleccionar todos los campos de la tabla `books`

Si se desea seleccionar todos los campos de la tabla, se puede utilizar el asterisco (`*`) en lugar de listar cada campo por separado. Esto permite obtener toda la información disponible en la tabla `books`.

```sql
-- Seleccionar todos los campos de la tabla books
SELECT *
FROM books;
```

## Resultados

Después de ejecutar estas consultas:

1. **Primera consulta**: Recupera solo los títulos de los libros.
2. **Segunda consulta**: Recupera tanto los títulos como los autores de los libros.
3. **Tercera consulta**: Recupera todos los campos disponibles de la tabla `books`, mostrando toda la información asociada con cada libro.

## Conclusión

Estas consultas son fundamentales para cualquier interacción con bases de datos. Con `SELECT` y `FROM`, puedes recuperar tanto campos específicos como toda la información contenida en una tabla. Al seleccionar campos específicos, las consultas se vuelven más eficientes y concisas, mientras que al utilizar `SELECT *` se obtiene todo el conjunto de datos de una tabla.