# Practice with aggregate functions

### **Primera consulta:**
```sql
-- Query the sum of film durations
SELECT SUM(duration) AS total_duration
FROM films;
```
#### Descripción:
- **Propósito:** Esta consulta calcula la suma total de las duraciones de todas las películas en la tabla `films`.
- **Instrucciones:**
   1. **SUM(duration):** Suma los valores en la columna `duration`, que representa la duración de cada película.
   2. **AS total_duration:** Se utiliza para asignar un alias al resultado, en este caso `total_duration`, que indicará el tiempo total de duración de todas las películas.
   3. **FROM films:** Se especifica la tabla de donde se obtienen los datos, que en este caso es `films`.
- **Resultado esperado:** La suma total de las duraciones de todas las películas.

---

### **Segunda consulta:**
```sql
-- Calculate the average duration of all films
SELECT AVG(duration) AS average_duration
FROM films;
```
#### Descripción:
- **Propósito:** Esta consulta calcula la duración promedio de todas las películas.
- **Instrucciones:**
   1. **AVG(duration):** Calcula el valor promedio de la columna `duration`.
   2. **AS average_duration:** Asigna un alias al resultado, `average_duration`, para que el resultado sea más claro.
   3. **FROM films:** Se obtienen los datos de la tabla `films`.
- **Resultado esperado:** La duración promedio de todas las películas.

---

### **Tercera consulta:**
```sql
-- Find the latest release_year
SELECT MAX(release_year) AS latest_year
FROM films;
```
#### Descripción:
- **Propósito:** Encuentra el año más reciente de estreno en la tabla `films`.
- **Instrucciones:**
   1. **MAX(release_year):** Encuentra el valor máximo en la columna `release_year`, que representará el año más reciente.
   2. **AS latest_year:** Se asigna un alias al resultado, `latest_year`.
   3. **FROM films:** Se extraen los datos de la tabla `films`.
- **Resultado esperado:** El año más reciente de estreno en la tabla de películas.

---

### **Cuarta consulta:**
```sql
-- Find the duration of the shortest film
SELECT MIN(duration) AS shortest_film
FROM films;
```
#### Descripción:
- **Propósito:** Esta consulta encuentra la duración de la película más corta.
- **Instrucciones:**
   1. **MIN(duration):** Encuentra el valor mínimo en la columna `duration`, que representará la duración de la película más corta.
   2. **AS shortest_film:** Asigna un alias al resultado, `shortest_film`.
   3. **FROM films:** Los datos se obtienen de la tabla `films`.
- **Resultado esperado:** La duración de la película más corta.

---

### **Resumen de funciones agregadas utilizadas:**
1. **SUM():** Calcula la suma de todos los valores numéricos de una columna.
2. **AVG():** Calcula el promedio de todos los valores numéricos.
3. **MAX():** Encuentra el valor máximo de una columna.
4. **MIN():** Encuentra el valor mínimo de una columna.

Estas funciones son muy útiles para obtener resúmenes estadísticos o de valores clave dentro de una base de datos.