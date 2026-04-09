¿Qué es una transacción? ¿Para qué se usan?
Una transacción es un conjunto de operaciones que se ejecutan como una sola unidad dentro de una base de datos. Su objetivo es asegurar la consistencia de la información: si todas las operaciones se completan correctamente se guardan los cambios (commit), y si ocurre algún error se deshacen (rollback).
¿Cómo puedo evitar que el comando para crear una tabla falle si es que la tabla ya está creada?
Se utiliza la instrucción:
CREATE TABLE IF NOT EXISTS nombre_tabla (...);
Esto permite crear la tabla solo si no existe, evitando errores.
¿Qué es un trigger o disparador? Da dos ejemplos de cuándo es bueno usarlos.
Un trigger es una acción automática que se ejecuta en la base de datos cuando ocurre un evento como INSERT, UPDATE o DELETE en una tabla.

Ejemplos:

Registrar cambios en una tabla para llevar un historial o auditoría.
Actualizar datos automáticamente, por ejemplo recalcular un total después de insertar un registro.
¿Qué es SQL Injection? ¿Qué implicaciones tiene?
SQL Injection es un ataque en el que se introduce código SQL malicioso en los campos de entrada de una aplicación para manipular la base de datos. Esto puede permitir acceder, modificar o eliminar información sin autorización.
Sus implicaciones incluyen robo de datos, acceso indebido a sistemas, pérdidas económicas y daño a la reputación de las organizaciones.
¿Qué es un ORM y qué diferencias existen con escribir sentencias de SQL comunes?
Un ORM (Mapeo Objeto-Relacional) es una herramienta que permite interactuar con una base de datos mediante objetos del lenguaje de programación, en lugar de escribir consultas SQL directamente.

Diferencias:

ORM: usa clases y métodos, lo que lo hace más sencillo y fácil de mantener.
SQL: permite mayor control y suele ser más eficiente en consultas complejas.
ORM: reduce errores y facilita el desarrollo.
SQL: ofrece mayor flexibilidad y optimización.
