# Organización de Datos en una Base de Datos Relacional

## Descripción

Entender la organización de una base de datos es fundamental cuando se trabaja con SQL. La base de datos relacional está compuesta por múltiples tablas que se relacionan entre sí mediante claves, permitiendo una estructura organizada y fácil de consultar.

## Tablas en la Base de Datos

En el ejemplo provisto, podemos observar tres tablas interrelacionadas:

1. **Tabla `employees`**:
   Esta tabla contiene información de los empleados, con las siguientes columnas:
   - `id`: identificador único del empleado.
   - `name`: nombre del empleado.
   - `dept_id`: identificador del departamento al que pertenece el empleado.
   - `job_level_id`: identificador del nivel del puesto que ocupa el empleado.
   
   Ejemplo de datos:
   | id    | name    | dept_id | job_level_id |
   |-------|---------|---------|--------------|
   | 54378 | Darius  | 1       | 3            |
   | 94722 | Raven   | 2       | 3            |
   | 45783 | Eduardo | 2       | 1            |

2. **Tabla `job_levels`**:
   Esta tabla define los diferentes niveles de trabajo que puede tener un empleado, con las siguientes columnas:
   - `id`: identificador único del nivel de trabajo.
   - `name`: nombre del nivel (e.g. Ejecutivo, Gerente).
   - `min_salary`: salario mínimo para ese nivel de trabajo.
   
   Ejemplo de datos:
   | id | name        | min_salary |
   |----|-------------|------------|
   | 1  | Executive   | 100000     |
   | 2  | Manager     | 70000      |
   | 3  | Contributor | 35000      |

3. **Tabla `departments`**:
   Esta tabla almacena información sobre los departamentos dentro de la empresa, con las siguientes columnas:
   - `id`: identificador único del departamento.
   - `dept_name`: nombre del departamento.
   - `dept_head`: jefe del departamento.
   
   Ejemplo de datos:
   | id | dept_name   | dept_head |
   |----|-------------|-----------|
   | 1  | Design      | Jack      |
   | 2  | Content     | Eduardo   |
   | 3  | Engineering | Vanessa   |

## Relación entre Tablas

Esta estructura refleja un modelo de base de datos relacional, donde las tablas están conectadas mediante claves foráneas.

- La tabla `employees` se relaciona con la tabla `departments` a través de la columna `dept_id`, que actúa como una clave foránea apuntando al `id` en `departments`. Esto indica en qué departamento trabaja cada empleado.
  
- De manera similar, la tabla `employees` también está conectada a `job_levels` mediante la columna `job_level_id`, que apunta al `id` en `job_levels`. Esto define el nivel de trabajo de cada empleado.

### Relaciones:

- **employees.dept_id → departments.id**: Muestra a qué departamento pertenece cada empleado.
- **employees.job_level_id → job_levels.id**: Muestra el nivel de trabajo de cada empleado.

## Respuesta Correcta a la Pregunta

La afirmación que describe correctamente la organización de esta base de datos es:

**"This is a relational database containing three tables: `employees`, `job_levels`, and `departments`."**

Este enunciado es correcto porque la base de datos está organizada de manera relacional, con tres tablas conectadas entre sí mediante claves foráneas.