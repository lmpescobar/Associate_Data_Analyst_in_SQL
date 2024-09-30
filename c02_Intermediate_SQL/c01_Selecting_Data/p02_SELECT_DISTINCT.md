# **SELECT DISTINCT**

El uso de `SELECT DISTINCT` es útil cuando queremos obtener solo los valores únicos de una columna en una tabla, eliminando los duplicados en los resultados.

### **Primera consulta:**
```sql
-- Return the unique countries from the films table
SELECT DISTINCT country
FROM films;
```

#### Descripción:
- **Propósito:** Esta consulta devuelve todos los países que están representados en la columna `country` de la tabla `films`, pero eliminando cualquier valor duplicado.
- **Instrucciones:**
   1. **SELECT DISTINCT country:** Se seleccionan solo los valores únicos de la columna `country`.
   2. **FROM films:** Se especifica que los datos se obtienen de la tabla `films`.
- **Resultado esperado:** Una lista de todos los países representados en la tabla `films`, pero sin repetir ningún país.

---

### **Segunda consulta:**
```sql
-- Count the distinct countries from the films table
SELECT COUNT(DISTINCT country) AS count_distinct_countries
FROM films;
```

#### Descripción:
- **Propósito:** Esta consulta cuenta cuántos países únicos están representados en la tabla `films`, sin contar los duplicados.
- **Instrucciones:**
   1. **COUNT(DISTINCT country):** Esta función cuenta cuántos valores únicos hay en la columna `country`, eliminando los valores repetidos.
   2. **AS count_distinct_countries:** El resultado de `COUNT(DISTINCT country)` se etiqueta con el alias `count_distinct_countries`.
   3. **FROM films:** Se especifica que los datos provienen de la tabla `films`.
- **Resultado esperado:** Un número que representa cuántos países únicos están registrados en la tabla `films`.

---

### Resumen general:
En estas consultas estamos utilizando `SELECT DISTINCT` para:
1. Obtener los valores únicos de la columna `country`.
2. Contar cuántos valores únicos existen en esa columna.

La primera consulta devuelve una lista de países únicos, mientras que la segunda cuenta cuántos países únicos están presentes en la tabla.