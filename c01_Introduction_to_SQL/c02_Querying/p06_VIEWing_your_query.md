```markdown
# Creación de Vistas en SQL

## Descripción

En SQL, una **vista** es una tabla virtual basada en el resultado de una consulta SQL. Las vistas no almacenan datos por sí mismas; en lugar de eso, almacenan la consulta que genera los datos. Las vistas son útiles cuando se quiere reutilizar una consulta compleja, facilitar el acceso a ciertos datos o crear una capa de abstracción.

En este ejercicio, se crea una vista llamada `library_authors`, basada en una consulta que devuelve autores únicos desde la tabla `books`. Posteriormente, se verifica que la vista haya sido creada correctamente consultando todos los datos de esa vista.

## Instrucciones

### Paso 1: Crear una Vista

Para crear una vista, se utiliza la instrucción `CREATE VIEW`. A continuación, se define la vista con el nombre `library_authors`, basada en una consulta que devuelve los autores únicos de la tabla `books`.

```sql
-- Guardar los resultados de esta consulta en una vista llamada library_authors
CREATE VIEW library_authors AS
SELECT DISTINCT author AS unique_author
FROM books;
```

### Paso 2: Consultar la Vista

Después de crear la vista, se puede consultar la vista como si fuera una tabla real. Aquí se seleccionan todas las columnas de la vista `library_authors` para verificar que fue creada correctamente y contiene los autores únicos.

```sql
-- Seleccionar todas las columnas de la vista library_authors
SELECT *
FROM library_authors;
```

## Resultado

1. **Primera Parte**: La vista `library_authors` es creada, almacenando la consulta que devuelve los autores únicos de la tabla `books`, con el alias `unique_author`.

2. **Segunda Parte**: Se consulta la vista para verificar que contiene los resultados esperados. Los resultados muestran una lista de autores únicos, con la columna renombrada como `unique_author`.

| unique_author     |
|-------------------|
| John Hellemann    |
| Sheryl Sandberg   |
| Brené Brown       |
| ...               |

## Conclusión

Las vistas en SQL proporcionan una manera eficiente de reutilizar consultas complejas y crear una capa de abstracción para los usuarios de la base de datos. Al usar una vista, se puede acceder a los resultados de una consulta sin necesidad de reescribir el código SQL cada vez, lo que facilita el mantenimiento y mejora la organización del código.