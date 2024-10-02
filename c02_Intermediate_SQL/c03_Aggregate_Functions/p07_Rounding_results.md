# Rounding results

### Código SQL

```sql
SELECT title, ROUND(duration / 60.0, 2) AS duration_hours
FROM films;
```

### Explicación del código:

1. **`SELECT title, ROUND(duration / 60.0, 2)`**:
   - Aquí seleccionamos el título de la película (`title`).
   - **`duration / 60.0`**: Divide la duración de las películas, que está en minutos, entre 60.0 para convertirla a horas.
   - **`ROUND(..., 2)`**: Esta función redondea el resultado de la conversión a dos decimales. El número `2` indica el número de decimales a los que se redondea.
   - **`AS duration_hours`**: Se usa para asignar un alias a la columna resultante, llamándola `duration_hours`, lo que hace que la columna sea más legible.

2. **`FROM films`**:
   - Indica que los datos se obtendrán de la tabla `films`, que contiene la información sobre las películas.

### Objetivo:
- El objetivo de este ejercicio es redondear los resultados a dos decimales para mejorar la presentación de los datos y hacer que los resultados de la duración en horas sean más claros y legibles.