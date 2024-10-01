# LIKE and NOT LIKE

### **Primera consulta:**
```sql
-- Select the names that start with B
SELECT name
FROM people
WHERE name LIKE 'B%';
```

#### Descripción:
- **Propósito:** Seleccionar los nombres que comienzan con la letra "B".
- **Instrucciones:**
   1. **SELECT name:** Selecciona la columna `name` de la tabla.
   2. **FROM people:** Los datos se obtienen de la tabla `people`.
   3. **WHERE name LIKE 'B%':** Filtra los nombres que comienzan con la letra "B". El carácter `%` es un comodín que representa cualquier número de caracteres después de la "B".
- **Resultado esperado:** Nombres que comienzan con la letra "B".

---

### **Segunda consulta:**
```sql
-- Select the names that have r as the second letter
SELECT name
FROM people
WHERE name LIKE '_r%';
```

#### Descripción:
- **Propósito:** Seleccionar los nombres que tienen la letra "r" como segunda letra.
- **Instrucciones:**
   1. **SELECT name:** Selecciona la columna `name`.
   2. **FROM people:** Los datos se obtienen de la tabla `people`.
   3. **WHERE name LIKE '_r%':** El carácter `_` representa cualquier carácter único en la primera posición, seguido de "r" como segunda letra. El `%` representa cualquier número de caracteres después de la "r".
- **Resultado esperado:** Nombres cuya segunda letra es "r".

---

### **Tercera consulta:**
```sql
-- Select the names that don't start with A
SELECT name
FROM people
WHERE name NOT LIKE 'A%';
```

#### Descripción:
- **Propósito:** Seleccionar los nombres que **no** comienzan con la letra "A".
- **Instrucciones:**
   1. **SELECT name:** Selecciona la columna `name`.
   2. **FROM people:** Los datos se obtienen de la tabla `people`.
   3. **WHERE name NOT LIKE 'A%':** Filtra los nombres que no comienzan con la letra "A". Aquí, el operador `NOT LIKE` se usa para excluir aquellos nombres que empiezan con "A".
- **Resultado esperado:** Nombres que no comienzan con la letra "A".

---

### **Resumen del uso de `LIKE` y `NOT LIKE`:**
- **`LIKE`**: Se utiliza para buscar patrones en las cadenas de texto.
- **`NOT LIKE`**: Se usa para excluir los resultados que coinciden con un patrón.
- **Comodines:**
   - **`%`**: Representa cero o más caracteres.
   - **`_`**: Representa un solo carácter.

Estos operadores son útiles cuando se trabaja con datos de texto y se necesita buscar coincidencias parciales o patrones específicos.