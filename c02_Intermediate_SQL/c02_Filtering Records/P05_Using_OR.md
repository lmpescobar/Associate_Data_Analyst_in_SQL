# Using OR

### **Primera consulta:**
```sql
-- Find the title and year of films from 1990 or 1999
SELECT title, release_year
FROM films
WHERE release_year = 1990
OR release_year = 1999;
```

#### Descripción:
- **Propósito:** Seleccionar el título (`title`) y el año de lanzamiento (`release_year`) de las películas que fueron lanzadas en el año 1990 o 1999.
- **Instrucciones:**
   1. **SELECT title, release_year:** Selecciona las columnas `title` y `release_year` para mostrar los títulos y años de lanzamiento de las películas.
   2. **FROM films:** Los datos se obtienen de la tabla `films`.
   3. **WHERE release_year = 1990 OR release_year = 1999:** Filtra los resultados para incluir solo las películas que fueron lanzadas en 1990 o 1999.
- **Resultado esperado:** Una lista de películas que fueron lanzadas en los años 1990 o 1999.

---

### **Segunda consulta:**
```sql
-- Add a filter to see only English or Spanish-language films
SELECT title, release_year
FROM films
WHERE (release_year = 1990 OR release_year = 1999)
AND (language = 'English' OR language = 'Spanish');
```

#### Descripción:
- **Propósito:** Filtrar las películas para incluir solo las que están en inglés o español, además de las que fueron lanzadas en 1990 o 1999.
- **Instrucciones:**
   1. **SELECT title, release_year:** Selecciona las columnas `title` y `release_year`.
   2. **FROM films:** Los datos se obtienen de la tabla `films`.
   3. **WHERE (release_year = 1990 OR release_year = 1999) AND (language = 'English' OR language = 'Spanish'):** Filtra las películas que se lanzaron en 1990 o 1999 y que están en inglés o español.
- **Resultado esperado:** Películas en inglés o español que se lanzaron en 1990 o 1999.

---

### **Tercera consulta:**
```sql
-- Filter films with more than $2,000,000 gross
SELECT title, release_year
FROM films
WHERE (release_year = 1990 OR release_year = 1999)
AND (language = 'English' OR language = 'Spanish')
AND (gross > 2000000);
```

#### Descripción:
- **Propósito:** Filtrar las películas para incluir solo aquellas que generaron más de 2 millones de dólares en ingresos brutos, además de cumplir con los criterios anteriores (año y idioma).
- **Instrucciones:**
   1. **SELECT title, release_year:** Selecciona las columnas `title` y `release_year`.
   2. **FROM films:** Los datos se obtienen de la tabla `films`.
   3. **WHERE (release_year = 1990 OR release_year = 1999) AND (language = 'English' OR language = 'Spanish') AND (gross > 2000000):** Filtra las películas que cumplen con los tres criterios: se lanzaron en 1990 o 1999, están en inglés o español, y generaron más de 2 millones de dólares en ingresos brutos.
- **Resultado esperado:** Una lista de películas que cumplan con todas las condiciones mencionadas.

---

### **Resumen del uso de `OR` y `AND`:**
- El operador **`OR`** permite combinar múltiples condiciones y devuelve los resultados que cumplan **al menos una** de las condiciones especificadas.
- El operador **`AND`** asegura que **todas** las condiciones se cumplan simultáneamente para que los registros sean devueltos.