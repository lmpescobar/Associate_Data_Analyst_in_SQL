# Practice with NULLs

En estas imágenes se muestra cómo trabajar con valores nulos en SQL, utilizando las condiciones **`IS NULL`** y **`IS NOT NULL`** para realizar consultas.

### **Primera consulta:**
```sql
-- List all film titles with missing budgets
SELECT title AS no_budget_info
FROM films
WHERE budget IS NULL;
```

#### Descripción:
- **Propósito:** Esta consulta selecciona el título de todas las películas que no tienen información registrada en la columna de presupuesto (`budget`), es decir, donde el presupuesto es `NULL`.
- **Instrucciones:**
   1. **SELECT title AS no_budget_info:** Selecciona la columna `title` y le asigna el alias `no_budget_info` para indicar que las películas seleccionadas no tienen información de presupuesto.
   2. **FROM films:** Los datos se obtienen de la tabla `films`.
   3. **WHERE budget IS NULL:** Filtra los resultados para incluir solo aquellos registros donde el valor en la columna `budget` es nulo.
- **Resultado esperado:** Una lista de películas cuyo presupuesto no está registrado.

---

### **Segunda consulta:**
```sql
-- Count the number of films with a language associated with them
SELECT COUNT(*) AS count_language_known
FROM films
WHERE language IS NOT NULL;
```

#### Descripción:
- **Propósito:** Contar cuántas películas tienen un valor asociado en la columna de idioma (`language`), es decir, aquellas donde el campo `language` no es nulo.
- **Instrucciones:**
   1. **SELECT COUNT(*) AS count_language_known:** Utiliza `COUNT(*)` para contar todas las filas donde la columna `language` tiene un valor no nulo, y el resultado se almacena en el alias `count_language_known`.
   2. **FROM films:** Los datos se obtienen de la tabla `films`.
   3. **WHERE language IS NOT NULL:** Filtra los resultados para contar solo las películas donde el idioma está registrado.
- **Resultado esperado:** Un número que indica cuántas películas tienen un idioma asociado.

---

### **Resumen del uso de `IS NULL` y `IS NOT NULL`:**
- **`IS NULL`**: Se utiliza para seleccionar los registros donde una columna específica tiene valores nulos, es decir, no se ha registrado un valor en esa columna.
- **`IS NOT NULL`**: Se utiliza para seleccionar los registros donde una columna tiene un valor asociado, excluyendo los valores nulos.

Estas consultas son muy útiles para manejar datos incompletos en bases de datos y garantizar que los análisis o informes se basen en registros completos o para identificar qué datos faltan.