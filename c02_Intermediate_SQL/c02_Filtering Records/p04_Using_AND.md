# Using AND

### **Primera consulta:**
```sql
-- Select the title and release_year for all German-language films released before 2000
SELECT title, release_year
FROM films
WHERE release_year < 2000
AND language = 'German';
```

#### Descripción:
- **Propósito:** Seleccionar los títulos (`title`) y años de lanzamiento (`release_year`) de las películas en alemán que se estrenaron antes del año 2000.
- **Instrucciones:**
   1. **SELECT title, release_year:** Selecciona las columnas `title` (título de la película) y `release_year` (año de lanzamiento).
   2. **FROM films:** Los datos se obtienen de la tabla `films`.
   3. **WHERE release_year < 2000 AND language = 'German':** El filtro especifica que las películas deben haber sido lanzadas antes del año 2000 y estar en alemán.
- **Resultado esperado:** Una lista de películas en alemán lanzadas antes del año 2000.

---

### **Segunda consulta:**
```sql
-- Update the query to see all German-language films released after 2000
SELECT title, release_year
FROM films
WHERE release_year > 2000
AND language = 'German';
```

#### Descripción:
- **Propósito:** Seleccionar los títulos (`title`) y años de lanzamiento (`release_year`) de las películas en alemán que se estrenaron después del año 2000.
- **Instrucciones:**
   1. **SELECT title, release_year:** Selecciona las columnas `title` y `release_year`.
   2. **FROM films:** Los datos se obtienen de la tabla `films`.
   3. **WHERE release_year > 2000 AND language = 'German':** Filtra las películas que fueron lanzadas después del año 2000 y están en alemán.
- **Resultado esperado:** Películas en alemán que se lanzaron después del año 2000.

---

### **Tercera consulta:**
```sql
-- Select all records for German-language films released after 2000 and before 2010
SELECT *
FROM films
WHERE release_year > 2000
AND release_year < 2010
AND language = 'German';
```

#### Descripción:
- **Propósito:** Seleccionar **todos los detalles** de las películas en alemán que se estrenaron entre 2000 y 2010.
- **Instrucciones:**
   1. **SELECT *:** Selecciona todas las columnas de la tabla `films`.
   2. **FROM films:** Los datos se obtienen de la tabla `films`.
   3. **WHERE release_year > 2000 AND release_year < 2010 AND language = 'German':** Filtra las películas lanzadas entre 2000 y 2010, y cuyo idioma es el alemán.
- **Resultado esperado:** Todas las películas en alemán lanzadas entre los años 2000 y 2010, mostrando todos los detalles.

---

### **Resumen del uso de `AND`:**
El operador **`AND`** permite combinar múltiples condiciones dentro de la cláusula `WHERE`. En estas consultas, se utiliza para filtrar por año de lanzamiento y por idioma, permitiendo refinar los resultados a películas en alemán dentro de un rango de años específico.