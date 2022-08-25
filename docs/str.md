# Strings - Cadenas

Las cadenas en Python se identifican como un conjunto continuo de caracteres representados entre comillas. Python permite pares de comillas simples, dobles o "triples". Por ejemplo −


```python
# Comillas simples.
hello = 'Hola Mundo!'
print(hello)

# Comillas dobles.
hello = "Hola Mundo!"
print(hello)

# Comillas dobles, sin escape de comillas simples.
vader = "Luke, I'm your father"
print(vader)

# Comillas simples con caracter de escape (\).
vader_again = 'Luke, I\'m your father'
print(vader_again)

# Comillas triples para multilínea.
multiline = """Hola 
Mundo!"""
print(multiline)
```

## Concatenación y repetición

El signo más ```(+)``` es el operador de concatenación de cadenas y el asterisco ```(*)``` es el operador de repetición. Por ejemplo −

### Concatenación

```python
# Concatenación de literales.
full_name = "Charles" + " " + "Darwin"
print(full_name)

# Concatenación de variables y literales (espacio).
first_name = 'Linus'
last_name = 'Torvalds'

full_name = first_name + " " + last_name
print(full_name)

# Modificación por concatenación
first_name += " " + last_name
print(first_name)
```

### Repetición

```python
# Número (int) de repeticiones
n = 4
codon = "CGT"
print(codon * n)
```

### Strings are Arrays

Like many other popular programming languages, strings in Python are arrays of bytes representing unicode characters.

Python does not have a character data type, a single character is simply a string with a length of 1.

Square brackets can be used to access elements of the string.

## Slicing

El *slicing* es una operación que extrae un subconjunto de elementos de una lista y los empaqueta como otra lista, posiblemente con un tamaño diferente de la original. Dado que esta operación es de uso bastante frecuente, Python ofrece características nativas que hacen posible construir *slices* de forma sencilla.

The slicing starts with the start_pos index (included) and ends at end_pos index (excluded). The step parameter is used to specify the steps to take from start to end index. 

El *slicing* se describe como ```[inicio:fin:paso]```. Todos los paramétros son opcionales y tienen los siguiente valores por defecto:

| Paramétro  | Valor por defecto |
| ------------- | ------------- |
| Inicio  | 0  |
| Fin  | Tamaño de la cadena ```len(str)``` |
| Paso  | 1 |



|G|r|e|g|o|r||M|e|n|d|e|l|!|cadena|
|--- |--- |--- |--- |--- |--- |--- |--- |--- |--- |--- |--- |--- |--- |--- |
|0|1|2|3|4|5|6|7|8|9|10|11|12|13|índice positivo|
|-14|-13|-12|-11|-10|-9|-8|-7|-6|-5|-4|-3|-2|-1|índice negativo|

### Slicing básico: Inicio y fin

```python
father = 'Gregor Mendel!'

# Slicing positvo.
print(father[0]) 
# 'G'

# Slicing negativo.
print(father[-1]) 
# 'l'

# inicio = 0, fin = 4 (excluido)
print(father[:4]) 
# 'Greg'

# inicio = 0, fin = -10 (excluido)
print(father[:-10]) 
# 'Greg'

# inicio = 4, fin = len(father)
print(father[4:]) 
# 'or Mendel!'
```

### Slicing avanzado: Cambiando el paso

```python
father = 'Gregor Mendel!'

# Slicing con paso positivo de 2.
print(father[::2]) 
# 'Geo edl'

# Slicing con paso negativo de 2.
print(father[::-2]) 
# 'lde oeG'
```

En el primer caso, se extrae toda la cadena con un paso de 2: se parte de la posición 0 y se extraen las letras de la cadena, avanzando de 2 en 2 hasta llegar al final de la cadena. En el segundo caso, el paso es -2: se parte de la última posición y se extraen las posiciones retrocediendo de 2 en 2 hasta llegar al inicio de la cadena.

El tercer parámetro de un *slice* es útil para invertir una cadena. Un *slice* descrito como ```[::-1]``` retorna una cadena invertida.

```python
father = 'Gregor Mendel!'

# Slicing con paso negativo de 1 para invertir la cadena.
print(father[::-1]) 
# '!ledneM rogerG'
```

## Inmutabilidad

In python, the string data types are immutable. Which means a string value cannot be updated. We can verify this by trying to update a part of the string which will led us to an error.

> Un objeto inmutable es aquel que, una vez creado, no puede cambiar en tiempo de ejecución.

```python
rose = "rosalind Franklin"
print(rose)
# rosalind Franklin

rose[0] = rose[0].upper()
# Traceback (most recent call last):
#   File "<stdin>", line 1, in <module>
# TypeError: 'str' object does not support item assignment

# No es posible reasignar el valor de la posición 0!

######## Una solución: slicing ########
rose = rose[0].upper() + rose[1:]
print(rose)
# Rosalind Franklin
```