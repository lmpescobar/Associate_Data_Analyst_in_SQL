# Using BETWEEN

### **Primera consulta:**
```sql
-- Select the title and release_year for films released between 1990 and 2000
SELECT title, release_year
FROM films
WHERE release_year BETWEEN 1990 AND 2000;
```

#### Descripción:
- **Propósito:** Seleccionar el título (`title`) y el año de lanzamiento (`release_year`) de las películas que se lanzaron entre 1990 y 2000, ambos inclusive.
- **Instrucciones:**
   1. **SELECT title, release_year:** Selecciona las columnas `title` y `release_year` para mostrar los títulos y los años de lanzamiento.
   2. **FROM films:** Los datos se obtienen de la tabla `films`.
   3. **WHERE release_year BETWEEN 1990 AND 2000:** Filtra las películas lanzadas entre 1990 y 2000.
- **Resultado esperado:** Películas lanzadas entre los años 1990 y 2000.

---

### **Segunda consulta:**
```sql
-- Narrow down your query to films with budgets > $100 million
SELECT title, release_year
FROM films
WHERE release_year BETWEEN 1990 AND 2000
AND budget > 100000000;
```

#### Descripción:
- **Propósito:** Filtrar las películas que tienen un presupuesto mayor a 100 millones de dólares, además de estar dentro del rango de años entre 1990 y 2000.
- **Instrucciones:**
   1. **SELECT title, release_year:** Selecciona las columnas `title` y `release_year`.
   2. **FROM films:** Los datos se obtienen de la tabla `films`.
   3. **WHERE release_year BETWEEN 1990 AND 2000 AND budget > 100000000:** Filtra las películas que se lanzaron entre 1990 y 2000 y que tienen un presupuesto mayor a 100 millones de dólares.
- **Resultado esperado:** Películas lanzadas entre 1990 y 2000 con presupuestos superiores a 100 millones.

---

### **Tercera consulta:**
```sql
-- Restrict the query to only return Spanish-language films
SELECT title, release_year
FROM films
WHERE release_year BETWEEN 1990 AND 2000
AND budget > 100000000
AND language = 'Spanish';
```

#### Descripción:
- **Propósito:** Filtrar las películas en español que cumplen con los criterios anteriores de rango de años y presupuesto.
- **Instrucciones:**
   1. **SELECT title, release_year:** Selecciona las columnas `title` y `release_year`.
   2. **FROM films:** Los datos se obtienen de la tabla `films`.
   3. **WHERE release_year BETWEEN 1990 AND 2000 AND budget > 100000000 AND language = 'Spanish':** Filtra las películas lanzadas entre 1990 y 2000, con un presupuesto superior a 100 millones, y que están en español.
- **Resultado esperado:** Películas en español lanzadas entre 1990 y 2000 con un presupuesto mayor a 100 millones.

---

### **Cuarta consulta:**
```sql
-- Amend the query to include Spanish or French-language films
SELECT title, release_year
FROM films
WHERE release_year BETWEEN 1990 AND 2000
AND budget > 100000000
AND (language = 'Spanish' OR language = 'French');
```

#### Descripción:
- **Propósito:** Filtrar las películas en español o francés que cumplan con los criterios anteriores de rango de años y presupuesto.
- **Instrucciones:**
   1. **SELECT title, release_year:** Selecciona las columnas `title` y `release_year`.
   2. **FROM films:** Los datos se obtienen de la tabla `films`.
   3. **WHERE release_year BETWEEN 1990 AND 2000 AND budget > 100000000 AND (language = 'Spanish' OR language = 'French'):** Filtra las películas lanzadas entre 1990 y 2000, con un presupuesto superior a 100 millones, que estén en español o francés.
- **Resultado esperado:** Películas en español o francés lanzadas entre 1990 y 2000 con un presupuesto mayor a 100 millones.

---

### **Resumen:**
- **`BETWEEN`**: Se utiliza para definir un rango de valores en SQL, en este caso para filtrar por el año de lanzamiento.
- **`AND`**: Se usa para combinar múltiples condiciones en una consulta.
- **`OR`**: Permite filtrar por más de una opción, en este caso, películas en español o francés.