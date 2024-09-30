# Practice with `COUNT()`

### **Primera consulta:**
```sql
-- Count the number of records in the people table
SELECT COUNT(*) AS count_records
FROM people;
```
#### Descripción:
- **Propósito:** Esta consulta tiene como objetivo contar el número total de registros en la tabla `people`.
- **Instrucciones:**
   1. **COUNT(*):** Esta función cuenta todas las filas de la tabla sin importar si contienen valores nulos.
   2. **AS count_records:** El resultado de `COUNT(*)` se etiqueta o se le asigna un alias llamado `count_records`.
   3. **FROM people:** Se especifica que la tabla de la cual se obtendrán los datos es `people`.
- **Resultado esperado:** Un número que representa el total de registros en la tabla `people`.

### **Segunda consulta:**
```sql
-- Count the number of birthdates in the people table
SELECT COUNT(birthdate) AS count_birthdate
FROM people;
```
#### Descripción:
- **Propósito:** Esta consulta cuenta cuántos registros en la tabla `people` tienen un valor no nulo en la columna `birthdate`.
- **Instrucciones:**
   1. **COUNT(birthdate):** A diferencia de `COUNT(*)`, esta función solo cuenta las filas donde `birthdate` tiene un valor no nulo.
   2. **AS count_birthdate:** El resultado se etiqueta con el alias `count_birthdate`.
   3. **FROM people:** Se especifica que la tabla a consultar es `people`.
- **Resultado esperado:** Un número que representa cuántas personas tienen una fecha de nacimiento registrada.

### **Tercera consulta:**
```sql
-- Count the records for languages and countries represented in the films table
SELECT COUNT(language) AS count_languages, COUNT(country) AS count_countries
FROM films;
```
#### Descripción:
- **Propósito:** Contar cuántos registros en la tabla `films` tienen valores no nulos en las columnas `language` y `country`.
- **Instrucciones:**
   1. **COUNT(language):** Cuenta cuántos registros tienen un valor no nulo en la columna `language`.
   2. **COUNT(country):** Cuenta cuántos registros tienen un valor no nulo en la columna `country`.
   3. **AS count_languages, count_countries:** Se asignan alias a los resultados: `count_languages` para la columna `language` y `count_countries` para la columna `country`.
   4. **FROM films:** Se especifica que los datos provienen de la tabla `films`.
- **Resultado esperado:** Dos números, uno que representa cuántas películas tienen un lenguaje registrado y otro que indica cuántas tienen un país registrado.

### Resumen general:
En cada consulta se utiliza la función **`COUNT`** para contar registros, ya sea en todas las filas o en columnas específicas, diferenciando si los valores son nulos o no. Además, se utilizan alias para nombrar los resultados de forma más comprensible al interpretar los datos.