# Elección de un Identificador Único en Bases de Datos

## ¿Qué es un Identificador Único?

Un **identificador único** (ID) es un valor que distingue a un registro de los demás dentro de una misma tabla en una base de datos. Esto es crucial para garantizar la integridad de los datos y para realizar consultas y actualizaciones de manera eficiente. El identificador único debe ser exclusivo para cada fila de datos y no repetirse.

## La Tabla `employees`

En la tabla `employees` del ejemplo, se presentan las siguientes columnas:

| id    | name    | dept_id | job_level_id |
|-------|---------|---------|--------------|
| 54378 | Darius  | 1       | 3            |
| 94722 | Raven   | 2       | 3            |
| 45783 | Eduardo | 2       | 1            |

- **id**: Este campo representa un número único asignado a cada empleado.
- **name**: Contiene el nombre del empleado.
- **dept_id**: Representa el identificador del departamento al que pertenece cada empleado.
- **job_level_id**: Representa el nivel del puesto que ocupa cada empleado.

## Elección del Mejor Identificador Único

De entre los campos mencionados, el **campo `id`** es el más adecuado para ser utilizado como identificador único. Aquí te explico por qué:

1. **id**: Este campo es exclusivo para cada empleado. Ningún otro empleado puede tener el mismo número de `id`, lo que lo convierte en el identificador ideal para distinguir a cada registro de los demás en la tabla.
   
2. **name**: Los nombres no son ideales como identificadores únicos, ya que varias personas pueden compartir el mismo nombre, lo que resultaría en duplicados.
   
3. **dept_id**: Este campo solo indica a qué departamento pertenece el empleado, pero varios empleados pueden pertenecer al mismo departamento, por lo que no es un identificador único.
   
4. **job_level_id**: Similar al caso anterior, varios empleados pueden tener el mismo nivel de trabajo, lo que descarta este campo como una opción válida para ser un identificador único.

### Respuesta Correcta

En la pregunta planteada, la opción correcta es:

**"id"** 

Es el campo más adecuado para ser utilizado como identificador único, ya que cada registro tiene un valor exclusivo en esa columna.