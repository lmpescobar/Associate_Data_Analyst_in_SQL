```markdown
# Uso de Alias en SQL

## Descripción

En SQL, es posible asignar **alias** a las columnas o tablas utilizando la palabra clave `AS`. Los alias permiten cambiar temporalmente el nombre de una columna en el conjunto de resultados para mejorar la claridad, legibilidad o para proporcionar nombres más significativos. En este ejercicio, se practica cómo usar alias para renombrar una columna en los resultados.

## Instrucciones

El objetivo es agregar un alias a la columna `author` para que en el conjunto de resultados aparezca bajo el nombre `unique_author`. Esto es útil para clarificar la intención detrás de la columna, especialmente en escenarios donde los nombres de las columnas pueden no ser suficientemente descriptivos.

### Consulta Original

```sql
-- Renombrar la columna 'author' a 'unique_author' utilizando un alias
SELECT DISTINCT author AS unique_author
FROM books;
```

### Explicación del Código

1. **`SELECT DISTINCT author AS unique_author`**: 
   - `DISTINCT author` selecciona autores únicos de la tabla `books`.
   - El alias `AS unique_author` renombra la columna `author` en los resultados como `unique_author`.

2. **`FROM books`**: 
   - Especifica que los datos provienen de la tabla `books`.

### Resultado

El resultado de la consulta muestra una lista de autores únicos, pero en lugar de aparecer bajo la columna `author`, los resultados aparecen bajo el alias `unique_author`. Esto ayuda a entender mejor el propósito de los datos mostrados.

| unique_author     |
|-------------------|
| John Hellemann    |
| Sheryl Sandberg   |
| Brené Brown       |
| ...               |

## Conclusión

El uso de alias en SQL es una técnica útil para mejorar la claridad de los conjuntos de resultados, especialmente cuando los nombres de las columnas no son suficientemente descriptivos o cuando quieres hacer que los resultados sean más legibles para quienes consumen los datos. Utilizar alias no afecta los nombres de las columnas en la tabla original, ya que los alias son temporales y solo se aplican al conjunto de resultados de una consulta.