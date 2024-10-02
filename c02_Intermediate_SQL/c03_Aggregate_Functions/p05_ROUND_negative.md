# ROUND() with a negative parameter

```sql
-- Calcular el presupuesto promedio redondeado al millar
SELECT ROUND(AVG(budget), -3) AS avg_budget_thousands
FROM films;
```

### Explicación:
1. **AVG(budget)**: Esta función calcula el promedio de la columna `budget` de la tabla `films`, que representa los presupuestos de las películas.
   
2. **ROUND(AVG(budget), -3)**: La función `ROUND()` redondea el valor del promedio del presupuesto al millar más cercano. El parámetro `-3` indica que se debe redondear a los miles (3 posiciones a la izquierda del punto decimal).

3. **AS avg_budget_thousands**: Se le asigna el alias `avg_budget_thousands` al resultado, para que este sea el nombre de la columna en la salida de los resultados.

El uso de un valor negativo en `ROUND()` es útil cuando deseas redondear a un valor más grande, como cientos, miles o decenas de miles, y ayuda a simplificar la representación de grandes números.