# Nomenclatura Correcta en Bases de Datos

## Descripción

Cuando se diseña una base de datos, es importante seguir buenas prácticas de **nomenclatura** para garantizar la claridad y el mantenimiento de las tablas a largo plazo. La convención de nombres adecuada ayuda a que los desarrolladores y otros usuarios de la base de datos comprendan de manera intuitiva el propósito de cada tabla y columna.

### Reglas Comunes de Nomenclatura

1. **Nombres en singular**: Generalmente, las tablas suelen nombrarse en singular, ya que cada fila representa una entidad única. Por ejemplo, si estamos almacenando información sobre clientes, la tabla debería llamarse `customer`, no `customers`.

2. **Evitar plurales innecesarios**: Las columnas no deberían usar plurales, ya que cada columna contiene un solo valor para cada registro. Por ejemplo, `phone_num` es preferible a `phone_nums`.

3. **Guion bajo (`_`) entre palabras**: Es común usar guiones bajos para separar palabras en los nombres de columnas. Esto mejora la legibilidad. Por ejemplo, usar `zip_code` en lugar de `zipcodes` o `zipcode`.

## Análisis de las Tablas Presentadas

En la imagen, se nos presentan dos versiones de una tabla que contiene información de clientes. A continuación, analizamos cuál sigue el formato de nomenclatura correcto:

1. **Versión 1**:
   | ids | customers | phone_nums    | zip_codes |
   |-----|-----------|---------------|-----------|
   | 567 | Jelle     | 781-765-2395  | 02476     |
   | 568 | Raushon   | 617-356-7772  | 01132     |
   | 570 | Catalina  | 206-644-0910  | 98112     |

   - **Problemas detectados**:
     - El nombre de la columna `ids` debería estar en singular, `id`.
     - El nombre de la columna `customers` debería estar en singular, `customer`.
     - El nombre de la columna `phone_nums` también debería estar en singular, `phone_num`.
     - El nombre de la columna `zip_codes` debería estar en singular, `zip_code`.

2. **Versión 2**:
   | id  | customer  | phone_num     | zip_code  |
   |-----|-----------|---------------|-----------|
   | 567 | Jelle     | 781-765-2395  | 02476     |
   | 568 | Raushon   | 617-356-7772  | 01132     |
   | 570 | Catalina  | 206-644-0910  | 98112     |

   - **Observaciones**:
     - Los nombres de columnas están correctamente formateados:
       - `id` está en singular, lo cual es correcto.
       - `customer` en singular describe correctamente a cada cliente.
       - `phone_num` está en singular y correctamente separado con guion bajo.
       - `zip_code` sigue la convención de usar guion bajo entre palabras.

### Respuesta Correcta

La tabla que sigue el formato de nomenclatura correcto es la **Versión 2**, que utiliza los nombres de las columnas en singular y emplea guiones bajos para mejorar la legibilidad.