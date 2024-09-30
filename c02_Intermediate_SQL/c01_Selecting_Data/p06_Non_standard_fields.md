# **Situación:**

Debes seleccionar un campo que tiene el nombre **`facebook likes`**, pero este nombre contiene un espacio, lo que requiere un tratamiento especial para que el motor de SQL lo interprete correctamente.

### **Opción correcta:**
La opción correcta para seleccionar este campo en la consulta SQL sería usar comillas dobles para indicar que es un nombre de campo con un espacio.

```sql
SELECT film_id, "facebook likes"
FROM reviews;
```

### **Explicación:**
1. **Nombres con espacios:** Cuando un campo contiene espacios o caracteres especiales, SQL puede tener dificultades para interpretarlo correctamente. En estos casos, se utilizan comillas dobles (`"`) para delimitar el nombre del campo.
   
2. **Uso de comillas dobles:** Al envolver el nombre del campo `"facebook likes"` con comillas dobles, le estás diciendo al motor SQL que lo trate como un nombre literal, a pesar del espacio.

### **Opción seleccionada:**
La opción correcta que se debe elegir es:
- **`"facebook likes"`** (opción 2).

Esto es necesario para que la consulta se ejecute correctamente y se pueda devolver el valor de ese campo, aunque tenga un espacio en su nombre.