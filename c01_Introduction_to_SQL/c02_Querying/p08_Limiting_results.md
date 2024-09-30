```markdown
# Limitación de Resultados en SQL

## Descripción

Cuando se trabaja con grandes volúmenes de datos, es útil limitar la cantidad de resultados que devuelve una consulta. Esto es especialmente importante cuando se prueba código o se exploran datos, ya que las tablas de bases de datos pueden contener miles de registros. La cláusula `LIMIT` en SQL permite restringir el número de filas que se devuelven en una consulta.

En este ejercicio, se practica el uso de `LIMIT` para limitar los resultados de una consulta a solo 10 filas.

## Instrucciones

La tarea es seleccionar el campo `genre` de la tabla `books` y devolver únicamente los primeros 10 resultados utilizando la cláusula `LIMIT`.

### Consulta SQL

```sql
-- Seleccionar los primeros 10 géneros de la tabla books utilizando PostgreSQL
SELECT genre
FROM books
LIMIT 10;
```

### Explicación del Código

1. **`SELECT genre`**: Selecciona el campo `genre` de la tabla. El campo contiene los géneros de los libros almacenados en la tabla `books`.
   
2. **`FROM books`**: Especifica que los datos deben ser extraídos de la tabla `books`.
   
3. **`LIMIT 10`**: Restringe el número de filas devueltas por la consulta a solo 10. Esto es útil cuando se desean ver solo una muestra de los datos.

### Resultados

El resultado de la consulta muestra solo los primeros 10 géneros disponibles en la tabla `books`. Esto ayuda a reducir la cantidad de datos visualizados cuando se trabaja con grandes volúmenes de información.

| genre        |
|--------------|
| Non Fiction  |
| Fiction      |
| Non Fiction  |
| ...          |

## Conclusión

La cláusula `LIMIT` es una herramienta útil en SQL para restringir el número de resultados de una consulta. Esto no solo mejora la eficiencia durante el desarrollo y la prueba de consultas, sino que también facilita la exploración de los datos al devolver solo una cantidad manejable de registros.