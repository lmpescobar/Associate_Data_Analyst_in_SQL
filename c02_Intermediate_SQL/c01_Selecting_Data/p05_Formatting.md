# **mejores prácticas de formato en SQL**.

### **Consulta original (con mal formato):**
```sql
select person_id, role from roles limit 10
```

### **Errores de formato:**
1. **Capitalización de palabras clave:** Las palabras clave como `SELECT`, `FROM` y `LIMIT` deben estar en mayúsculas.
2. **Formato de las cláusulas:** Cada cláusula (como `SELECT`, `FROM` y `LIMIT`) debe estar en una línea separada para mejorar la legibilidad.

### **Consulta corregida siguiendo las mejores prácticas:**
```sql
-- Rewrite this query following standard SQL formatting
SELECT person_id, role
FROM roles
LIMIT 10;
```

### **Explicación de la corrección:**
1. **Palabras clave en mayúsculas:** Todas las palabras clave (`SELECT`, `FROM`, `LIMIT`) ahora están en mayúsculas, lo cual es una práctica común para que las consultas sean más fáciles de leer.
2. **Cláusulas separadas en líneas diferentes:** Cada cláusula principal se coloca en una línea nueva para que la estructura de la consulta sea más clara, especialmente en consultas más largas o complejas.

Este tipo de formato asegura que el código sea más legible y mantenible para otros desarrolladores o para ti mismo en el futuro.