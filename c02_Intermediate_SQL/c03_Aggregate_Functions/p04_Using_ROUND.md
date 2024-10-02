# Using ROUND()

```sql
-- Redondea el promedio de facebook_likes a un decimal
SELECT ROUND(AVG(facebook_likes), 1) AS avg_facebook_likes
FROM reviews;
```

### Explicación:
1. **AVG(facebook_likes)**: Esta función calcula el promedio de la columna `facebook_likes` de la tabla `reviews`, que almacena la cantidad de "me gusta" de Facebook que tienen las películas.
   
2. **ROUND(AVG(facebook_likes), 1)**: La función `ROUND()` redondea el resultado del promedio (`AVG`) a un decimal. El número `1` especifica que queremos redondear a un decimal.

3. **AS avg_facebook_likes**: Le asigna el alias `avg_facebook_likes` al resultado, que será el nombre de la columna en el resultado final.

Este tipo de redondeo es útil para presentar valores que tengan muchos decimales de forma más clara y comprensible. En este caso, los likes de Facebook están siendo redondeados a un solo decimal para mejorar la legibilidad.