# Combining aggregate functions with WHERE

### Imagen 1: Suma del total de ingresos (`gross`) de películas del año 2000 o posteriores
```sql
-- Calcula la suma de los ingresos brutos desde el año 2000 o posterior
SELECT SUM(gross) AS total_gross
FROM films
WHERE release_year >= 2000;
```

#### Explicación:
1. **SUM(gross)**: Esta función suma todos los valores de la columna `gross`, que representa los ingresos brutos de las películas.
2. **WHERE release_year >= 2000**: El filtro asegura que solo se consideren películas cuyo año de estreno (`release_year`) sea 2000 o posterior.

### Imagen 2: Promedio de ingresos de películas cuyos títulos comienzan con la letra "A"
```sql
-- Calcula el promedio de ingresos de películas cuyo título empieza con "A"
SELECT AVG(gross) AS avg_gross_A
FROM films
WHERE title LIKE 'A%';
```

#### Explicación:
1. **AVG(gross)**: Esta función calcula el promedio de los ingresos brutos (`gross`).
2. **WHERE title LIKE 'A%'**: El uso de `LIKE` con el comodín `%` selecciona todas las películas cuyos títulos comienzan con la letra "A".

### Imagen 3: Ingreso más bajo de una película del año 1994
```sql
-- Calcula el ingreso más bajo de una película en 1994
SELECT MIN(gross) AS lowest_gross
FROM films
WHERE release_year = 1994;
```

#### Explicación:
1. **MIN(gross)**: Esta función obtiene el valor mínimo de la columna `gross`, es decir, el ingreso más bajo.
2. **WHERE release_year = 1994**: Este filtro selecciona únicamente las películas estrenadas en el año 1994.

### Imagen 4: Ingreso más alto de películas estrenadas entre los años 2000 y 2012
```sql
-- Calcula el ingreso más alto de las películas estrenadas entre 2000 y 2012
SELECT MAX(gross) AS highest_gross
FROM films
WHERE release_year BETWEEN 2000 AND 2012;
```

#### Explicación:
1. **MAX(gross)**: La función `MAX` selecciona el valor más alto de la columna `gross`, es decir, el ingreso más alto.
2. **WHERE release_year BETWEEN 2000 AND 2012**: Este filtro selecciona las películas estrenadas entre los años 2000 y 2012, inclusive.