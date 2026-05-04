# Normalización de bases de datos

La normalización es un proceso que se utiliza en bases de datos para organizar la información de forma eficiente, evitando redundancias y mejorando la integridad de los datos.

## Objetivo principal
El objetivo de la normalización es:
- Evitar duplicidad de información
- Reducir errores en los datos
- Facilitar el mantenimiento de la base de datos

## Formas normales

### Primera Forma Normal (1FN)
- Elimina datos repetidos
- Cada campo debe tener un valor único (no listas)

Ejemplo: En lugar de tener varios actores en una misma celda, se separan en filas.

---

### Segunda Forma Normal (2FN)
- Aplica cuando hay llaves compuestas
- Elimina dependencias parciales

Ejemplo: Si una tabla depende solo de parte de la llave, se separa en otra tabla.

---

### Tercera Forma Normal (3FN)
- Elimina dependencias transitivas
- Los campos dependen solo de la llave primaria

Ejemplo: separar país de usuarios en otra tabla.

---

## Comparación con lo visto en clase

En clase vimos ejercicios similares donde:
- Separábamos entidades como usuarios, películas y actores
- Usábamos relaciones mediante llaves foráneas
- Evitábamos repetir información (por ejemplo, países en cada usuario)

El modelo del ejercicio de películas ya está normalizado porque:
- Cada entidad está en su propia tabla
- Se usan relaciones (JOINs) en lugar de duplicar datos
- Se evita redundancia

---

## Conclusión

La normalización permite tener bases de datos más limpias, organizadas y eficientes, facilitando consultas y reduciendo errores.
