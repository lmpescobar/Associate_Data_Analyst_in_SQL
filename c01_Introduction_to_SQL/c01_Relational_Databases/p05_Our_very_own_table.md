```markdown
# Exploración de una Tabla en SQL

## Descripción

Este ejercicio forma parte de una introducción a SQL en la que se explora el contenido de una tabla llamada `books`. La consulta proporcionada tiene como objetivo recuperar todos los registros y todas las columnas de la tabla `books` para poder observar sus datos.

## Instrucciones

1. **Consulta SQL**: Utilizamos la instrucción `SELECT` para extraer información de la tabla.
   
   ```sql
   SELECT *
   FROM books;
   ```

2. **Explicación de la Consulta**:
   - `SELECT *`: Esto significa que estamos seleccionando todas las columnas de la tabla. El asterisco (`*`) es un comodín que indica que se deben incluir todas las columnas de la tabla.
   - `FROM books`: Especifica que la información debe ser extraída de la tabla `books`.

## Resultado de la Consulta

Después de ejecutar la consulta, observamos los primeros 100 registros de la tabla `books` (de un total de 350 registros). Los campos extraídos incluyen:
- **id**: Identificador único del libro.
- **title**: El título del libro.

Ejemplos de algunos títulos obtenidos de la tabla:
1. *10-Day Green Smoothie Cleanse*
2. *11/22/63: A Novel*
3. *12 Rules for Life: An Antidote to Chaos*

## Conclusión

Este ejercicio es un excelente punto de partida para aprender a consultar bases de datos relacionales con SQL. La instrucción `SELECT *` permite ver todos los datos almacenados en una tabla, facilitando la exploración inicial de su contenido.