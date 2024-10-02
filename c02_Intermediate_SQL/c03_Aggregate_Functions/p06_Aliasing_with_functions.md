# Aliasing with functions

### 1. **Uso de la función `ROUND()`**

En el primer caso, estás utilizando la función `ROUND()` para redondear el promedio de los likes en Facebook a una sola posición decimal. Esto es útil para evitar trabajar con demasiadas cifras decimales y hacerlo más legible.

```sql
SELECT ROUND(AVG(facebook_likes), 1) AS avg_facebook_likes
FROM reviews;
```

**Explicación**:
- `AVG(facebook_likes)`: Calcula el promedio de los likes de Facebook.
- `ROUND(..., 1)`: Redondea este promedio a una sola posición decimal.
- `AS avg_facebook_likes`: Asigna un alias `avg_facebook_likes` para hacer el resultado más claro.

### 2. **Uso de `ROUND()` con un parámetro negativo**

En este ejemplo, redondeas el presupuesto promedio de las películas a miles usando un parámetro negativo en `ROUND()`.

```sql
SELECT ROUND(AVG(budget), -3) AS avg_budget_thousands
FROM films;
```

**Explicación**:
- `AVG(budget)`: Calcula el presupuesto promedio de las películas.
- `ROUND(..., -3)`: Redondea este valor a miles (es decir, tres posiciones a la izquierda de la coma decimal).
- `AS avg_budget_thousands`: Alias para representar el resultado en miles.

### 3. **Uso de operaciones aritméticas en SQL**

Esta consulta te pide calcular el descuento como porcentaje, dividiendo el descuento entre el precio pagado. La operación aritmética es sencilla, pero hay que tener cuidado con la división de enteros.

En SQL, si divides dos enteros sin convertirlos a decimales, el resultado podría truncarse a 0.

- Ejemplo: `2 / 10` sin conversión podría dar `0` en lugar de `0.2`.

### 4. **Alias con funciones y divisiones**

En esta consulta, calculas la duración de las películas en horas dividiendo la duración en minutos por `60.0`. Usar el alias ayuda a que el resultado sea más claro.

```sql
SELECT title, (duration / 60.0) AS duration_hours
FROM films;
```

**Explicación**:
- `duration / 60.0`: Convierte la duración de minutos a horas.
- `AS duration_hours`: Alias que clarifica que la columna representa horas.

### 5. **Porcentaje de personas fallecidas**

Aquí, calculas el porcentaje de personas fallecidas, usando las funciones `COUNT()` y un alias.

```sql
SELECT COUNT(deathdate) * 100.0 / COUNT(*) AS percentage_dead
FROM people;
```

**Explicación**:
- `COUNT(deathdate)`: Cuenta las personas con una fecha de fallecimiento.
- `COUNT(*)`: Cuenta todas las personas.
- Multiplicas por `100.0` para obtener el porcentaje.

### 6. **Décadas de cobertura de datos de películas**

Finalmente, calculas cuántas décadas cubren los datos de las películas.

```sql
SELECT (MAX(release_year) - MIN(release_year)) / 10.0 AS number_of_decades
FROM films;
```

**Explicación**:
- `MAX(release_year) - MIN(release_year)`: Calcula la diferencia entre el año más reciente y el más antiguo.
- `... / 10.0`: Divide por `10.0` para convertir los años a décadas.
- `AS number_of_decades`: Alias que representa el resultado como número de décadas.