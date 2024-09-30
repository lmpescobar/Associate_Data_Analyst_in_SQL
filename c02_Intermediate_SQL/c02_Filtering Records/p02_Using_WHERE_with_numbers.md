# Using WHERE with numbers

### **Primera consulta:**
```sql
-- Select film_ids and imdb_score with an imdb_score over 7.0
SELECT film_id, imdb_score
FROM reviews
WHERE imdb_score > 7.0;
```
#### Descripción:
- **Propósito:** Seleccionar las columnas `film_id` e `imdb_score` de las películas que tienen una puntuación en IMDB mayor a 7.0.
- **Instrucciones:**
   1. **SELECT film_id, imdb_score:** Selecciona las columnas `film_id` (ID de la película) y `imdb_score` (puntuación de la película en IMDB).
   2. **FROM reviews:** Extrae los datos de la tabla `reviews`.
   3. **WHERE imdb_score > 7.0:** Filtra los resultados para incluir solo aquellas películas cuya puntuación en IMDB sea mayor a 7.0.
- **Resultado esperado:** Devuelve una lista de películas con sus respectivas puntuaciones, pero solo las que tienen una puntuación superior a 7.0.

---

### **Segunda consulta:**
```sql
-- Select film_ids and facebook_likes for ten records with less than 1000 likes
SELECT film_id, facebook_likes
FROM reviews
WHERE facebook_likes < 1000
LIMIT 10;
```
#### Descripción:
- **Propósito:** Seleccionar las columnas `film_id` y `facebook_likes` de las primeras diez películas que tienen menos de 1000 "me gusta" en Facebook.
- **Instrucciones:**
   1. **SELECT film_id, facebook_likes:** Selecciona las columnas `film_id` y `facebook_likes` (número de "me gusta" en Facebook).
   2. **FROM reviews:** Extrae los datos de la tabla `reviews`.
   3. **WHERE facebook_likes < 1000:** Filtra los resultados para incluir solo películas que tienen menos de 1000 "me gusta" en Facebook.
   4. **LIMIT 10:** Limita el número de resultados a las primeras 10 películas que cumplen con el criterio anterior.
- **Resultado esperado:** Devuelve hasta 10 películas con menos de 1000 "me gusta" en Facebook.

---

### **Tercera consulta:**
```sql
-- Count the records with at least 100,000 votes
SELECT COUNT(num_votes) AS films_over_100K_votes
FROM reviews
WHERE num_votes >= 100000;
```
#### Descripción:
- **Propósito:** Contar cuántas películas tienen al menos 100,000 votos (`num_votes`) y dar un alias al resultado.
- **Instrucciones:**
   1. **SELECT COUNT(num_votes):** Cuenta el número de registros que cumplen la condición de tener al menos 100,000 votos.
   2. **AS films_over_100K_votes:** Asigna un alias `films_over_100K_votes` al resultado de la función `COUNT`.
   3. **FROM reviews:** Extrae los datos de la tabla `reviews`.
   4. **WHERE num_votes >= 100000:** Filtra los resultados para incluir solo las películas con 100,000 votos o más.
- **Resultado esperado:** Devuelve un número que representa cuántas películas tienen 100,000 votos o más.

---

### Resumen general:
1. La primera consulta selecciona películas con una puntuación superior a 7.0 en IMDB.
2. La segunda consulta selecciona 10 películas que tienen menos de 1000 "me gusta" en Facebook.
3. La tercera consulta cuenta cuántas películas tienen al menos 100,000 votos.