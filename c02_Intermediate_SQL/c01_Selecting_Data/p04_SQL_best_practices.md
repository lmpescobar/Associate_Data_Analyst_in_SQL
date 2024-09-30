# **Buenas prácticas (Best Practice):**

1. **Capitalizar las palabras clave (keywords):**  
   Las palabras clave como `SELECT`, `FROM`, `WHERE`, etc., deben estar en mayúsculas para que sean fácilmente reconocibles y se distingan de los nombres de columnas o tablas.
   
   **Ejemplo:**
   ```sql
   SELECT name, age
   FROM people;
   ```

2. **Terminar las consultas con punto y coma:**  
   El punto y coma (`;`) indica el final de una consulta. Aunque algunos sistemas pueden ejecutarla sin esto, es una buena práctica incluirlo siempre para evitar confusiones, especialmente cuando se escriben múltiples consultas.
   
   **Ejemplo:**
   ```sql
   SELECT name, age
   FROM people;
   ```

3. **Usar guiones bajos (underscores) en nombres de campos en lugar de espacios:**  
   En lugar de usar espacios o caracteres especiales en los nombres de columnas o tablas, utiliza guiones bajos (`_`). Esto mejora la legibilidad y evita problemas con la sintaxis de SQL.

   **Ejemplo:**
   ```sql
   SELECT first_name, last_name
   FROM employees;
   ```

### **Malas prácticas (Poor Practice):**
1. **Escribir la consulta en una sola línea:**  
   Aunque es posible, escribir una consulta SQL larga en una sola línea reduce la legibilidad, especialmente en consultas complejas. Es recomendable escribir cada cláusula en una línea nueva.

   **Ejemplo incorrecto:**
   ```sql
   SELECT name, age FROM people WHERE age > 30;
   ```

   **Mejor formato:**
   ```sql
   SELECT name, age
   FROM people
   WHERE age > 30;
   ```

2. **Escribir muchas consultas sin punto y coma:**  
   No terminar las consultas con un punto y coma puede generar errores, especialmente cuando se ejecutan varias consultas en el mismo bloque. Es una mala práctica escribir varias consultas sin separarlas correctamente.

3. **No capitalizar las palabras clave:**  
   Dejar las palabras clave en minúsculas hace que sea más difícil distinguir entre lo que es SQL y los nombres de columnas o tablas. Esto disminuye la legibilidad del código.

   **Ejemplo incorrecto:**
   ```sql
   select name, age from people;
   ```

   **Forma correcta:**
   ```sql
   SELECT name, age
   FROM people;
   ```

### Resumen:
Seguir las mejores prácticas de estilo SQL mejora la claridad y mantenimiento del código. Asegúrate de capitalizar las palabras clave, utilizar punto y coma para finalizar las consultas, y emplear guiones bajos en los nombres de columnas o tablas.