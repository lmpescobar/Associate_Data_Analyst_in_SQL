```markdown
# Desarrollo del Estilo en SQL

## Descripción

Es importante prestar atención al formato de las consultas SQL para hacerlas más legibles y mantener las mejores prácticas. Aunque una consulta SQL puede ejecutarse correctamente con un formato básico o desordenado, seguir las convenciones de estilo recomendadas hace que el código sea más fácil de leer, mantener y entender.

En este ejercicio, se te pide que revises una consulta que extrae datos de la tabla `patrons`. El código funciona, pero es difícil de leer. La tarea es identificar qué sugerencias mejorarían el estilo de la consulta SQL.

## Consulta Inicial

```sql
SELECT CARD_NUM, TOTAL_FINE 
FROM patrons
```

La consulta anterior es funcional, pero se puede mejorar siguiendo mejores prácticas de estilo SQL.

## Sugerencias para Mejorar el Estilo de la Consulta

### Sugerencias a Implementar:

1. **Hacer `CARD_NUM` y `TOTAL_FINE` minúsculas**:
   - En SQL, los nombres de columnas generalmente se escriben en minúsculas. Esto mejora la consistencia con el resto del código y facilita la lectura.
   
2. **Agregar un `;` al final de la consulta**:
   - Es una buena práctica finalizar cada consulta SQL con un punto y coma (`;`). Aunque algunas bases de datos pueden ejecutar la consulta sin este símbolo, es estándar incluirlo para evitar posibles errores en consultas más largas o en sistemas que lo requieren.

3. **Capitalizar `FROM`**:
   - Los comandos SQL como `SELECT`, `FROM`, `WHERE` se suelen escribir en mayúsculas. Esto permite diferenciarlos claramente de los nombres de tablas y columnas, mejorando la legibilidad.

### Sugerencias a Evitar:

1. **Hacer que `SELECT` esté en minúsculas**:
   - Como se mencionó antes, los comandos SQL deben estar en mayúsculas para mejorar la legibilidad. Cambiar `SELECT` a minúsculas iría en contra de esta convención.

2. **Poner todo el código en una sola línea**:
   - Aunque la consulta podría ejecutarse en una sola línea, no es recomendable. Escribir el código en múltiples líneas mejora la organización y facilita la lectura, especialmente en consultas largas o complejas.

3. **Capitalizar `patrons`**:
   - Los nombres de tablas, al igual que los nombres de columnas, suelen estar en minúsculas para mantener la consistencia. No se recomienda capitalizar los nombres de las tablas.

## Consulta Mejorada

Aplicando las sugerencias correctas, la consulta quedaría de la siguiente manera:

```sql
SELECT card_num, total_fine
FROM patrons;
```

Este formato sigue las mejores prácticas de estilo SQL, lo que mejora la claridad y facilita el mantenimiento del código.

## Conclusión

Seguir las convenciones de estilo SQL es esencial para escribir consultas que no solo funcionen correctamente, sino que también sean legibles y fáciles de mantener. Utilizar mayúsculas para los comandos SQL, minúsculas para los nombres de tablas y columnas, y finalizar con un punto y coma son buenas prácticas que se deben adoptar desde el principio.