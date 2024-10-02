# Aggregate functions and data types

### **Funciones agregadas en SQL:**
Las funciones agregadas permiten realizar cálculos en un conjunto de valores, devolviendo un solo valor como resultado. Estas son algunas de las más utilizadas:

1. **AVG():** Calcula el promedio de un conjunto de valores.  
   - **Compatible con:** Datos numéricos.
   - Ejemplo: El promedio de precios o salarios.

2. **SUM():** Suma los valores en un conjunto de datos.  
   - **Compatible con:** Datos numéricos.
   - Ejemplo: La suma total de las ventas de un mes.

3. **MIN():** Devuelve el valor mínimo de un conjunto de datos.  
   - **Compatible con:** Varios tipos de datos (números, fechas, etc.).
   - Ejemplo: La fecha más antigua de una lista de fechas.

4. **MAX():** Devuelve el valor máximo de un conjunto de datos.  
   - **Compatible con:** Varios tipos de datos (números, fechas, etc.).
   - Ejemplo: El salario más alto en una lista de salarios.

5. **COUNT():** Cuenta el número de valores (no nulos) en un conjunto de datos.  
   - **Compatible con:** Varios tipos de datos.
   - Ejemplo: El número total de registros en una tabla.

### **Clasificación según tipos de datos:**

#### **Datos numéricos únicamente:**
- **SUM():** Solo funciona con datos numéricos.
- **AVG():** Solo funciona con datos numéricos.

#### **Varios tipos de datos:**
- **MAX():** Funciona con tipos de datos como números, fechas y textos.
- **MIN():** Funciona con tipos de datos como números, fechas y textos.
- **COUNT():** Funciona con cualquier tipo de dato, incluyendo números, cadenas de texto, fechas, etc.

### **Conclusión:**
Este ejercicio permite verificar el conocimiento sobre qué funciones agregadas son compatibles con diferentes tipos de datos. Funciones como **SUM()** y **AVG()** son exclusivas para datos numéricos, mientras que **MAX()**, **MIN()**, y **COUNT()** pueden ser utilizadas con una mayor variedad de tipos de datos.