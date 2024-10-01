# Combining filtering and selecting

### **Consulta SQL:**
```sql
-- Count the unique titles
SELECT COUNT(DISTINCT title) AS nineties_english_films_for_teens
FROM films
-- Filter to release_year to between 1990 and 1999
WHERE release_year BETWEEN 1990 AND 1999
-- Filter to English-language films
AND language = 'English'
-- Narrow it down to G, PG, and PG-13 certifications
AND certification IN ('G', 'PG', 'PG-13');
```

### **Explicación detallada de cada parte:**

1. **SELECT COUNT(DISTINCT title) AS nineties_english_films_for_teens:**  
   Esta parte selecciona el **número de títulos únicos** de películas usando `COUNT` y `DISTINCT` para asegurarse de que cada título se cuente solo una vez. El resultado se almacena con el alias `nineties_english_films_for_teens`.

2. **FROM films:**  
   Los datos provienen de la tabla `films`, que contiene información sobre las películas.

3. **WHERE release_year BETWEEN 1990 AND 1999:**  
   Este filtro limita los resultados a las películas que fueron lanzadas entre 1990 y 1999, inclusive.

4. **AND language = 'English':**  
   Este filtro adicional reduce los resultados a solo las películas cuyo idioma es el inglés.

5. **AND certification IN ('G', 'PG', 'PG-13'):**  
   Finalmente, este filtro selecciona solo las películas que tienen una clasificación adecuada para adolescentes, como "G", "PG", o "PG-13".

### **Resumen del objetivo de la consulta:**
La consulta tiene como objetivo contar cuántas películas únicas en inglés, lanzadas entre 1990 y 1999, tienen clasificaciones aptas para adolescentes (G, PG, PG-13). 

### **Resultados esperados:**
Un número que representa el total de títulos únicos de películas que cumplen con todos los filtros aplicados (año de lanzamiento, idioma y clasificación).