# **Explicación del ejercicio: Orden de ejecución en SQL**

En SQL, la ejecución de las consultas sigue un orden específico, que no siempre es el mismo que el orden en que las escribimos. Esto es importante para que el motor SQL sepa cómo manejar los datos.

Los tres elementos que ves en el ejercicio son:
1. **FROM**: Indica de dónde se obtendrán los datos, es decir, la fuente de datos o tablas.
2. **SELECT**: Indica qué columnas o expresiones serán seleccionadas y devueltas en los resultados.
3. **LIMIT**: Restringe el número de filas devueltas.

### **Orden correcto de ejecución:**

1. **FROM**: Primero, el sistema SQL necesita saber de qué tabla o tablas obtendrá los datos. Este paso siempre es el primero en el proceso de ejecución.
2. **SELECT**: Una vez que el sistema tiene los datos de las tablas, selecciona las columnas específicas que se desean mostrar en los resultados.
3. **LIMIT**: Finalmente, si se quiere limitar el número de resultados, este paso se ejecuta para devolver solo la cantidad de filas especificadas.

### Resumen del orden:

- Primero, **FROM** para indicar de dónde vienen los datos.
- Luego, **SELECT** para escoger qué datos específicos (columnas) mostrar.
- Finalmente, **LIMIT** para restringir el número de filas devueltas.