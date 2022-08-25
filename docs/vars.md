# Variables

Las variables son ubicaciones de memoria reservadas para almacenar valores. Esto significa que cuando se crea una variable, se reserva algo de espacio en memoria.

Según el tipo de dato de una variable, el intérprete asigna memoria y decide qué se puede almacenar en la memoria reservada.

## Nombre de variable

Una variable puede tener un nombre corto (como ser ```x```, ```y```) o ser más descriptivo (ciudad, apellido, total). 

Existen un conjunto de reglas para nominar variables en Python:

- Debe iniciar con una letra (```last_name```) o guión bajo (```_last_name```).
- Solo puede incluir caracteres alfanuméricos y guión bajo (a-z, 0-9, y _).
- Los nombres de las variables son sensibles a mayúsculas y minúsculas (```car```, ```Car``` y ```CAR``` son variables distintas).

## Declaración de una variable

Las variables de Python no necesitan una declaración explícita de tipo para reservar espacio en memoria. La definición de tipo ocurre automáticamente cuando se asigna un valor a una variable, ya que Python es un lenguaje de *tipado dinámico*.

El **operador de asiganción** ```(=)``` se utiliza para asignar valores a las variables. Por ejemplo −

```python
# Sintaxis: Nombre = Valor

# Asignación del valor 3.1461 a la variable 'pi'.
pi = 3.1416

name = 'Eleven'
```