# Using WHERE with text

### **Consulta SQL:**
```sql
-- Count the Spanish-language films
SELECT COUNT(language) AS count_spanish
FROM films
WHERE language = 'Spanish';
```

### **Descripción de la consulta:**
1. **`SELECT COUNT(language) AS count_spanish`:** Esta parte de la consulta cuenta el número de registros en la columna `language` y utiliza el alias `count_spanish` para nombrar el resultado. Esto te permitirá obtener cuántas películas están en un idioma específico, en este caso, español.
   
2. **`FROM films`:** Los datos se obtienen de la tabla `films`.

3. **`WHERE language = 'Spanish'`:** Se aplica un filtro para seleccionar solo los registros donde el valor en la columna `language` sea igual a `'Spanish'`. Esto asegura que solo se cuenten las películas cuyo idioma sea español.

### **Resultado esperado:**
La consulta devolverá el número total de películas que están en español (`language = 'Spanish'`), mostrando el resultado bajo el alias `count_spanish`.

### **Conclusión:**
Esta consulta es útil cuando necesitas contar registros basados en texto, en este caso, para contar películas en un idioma específico (español). La cláusula `WHERE` se utiliza para filtrar por texto, y `COUNT` se usa para contar cuántos de esos registros cumplen la condición.