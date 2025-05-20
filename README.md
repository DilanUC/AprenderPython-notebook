# TAREAS
---

# Funciones incorporadas de Python - Resumen explicativo

A continuación se presenta un resumen de las funciones incorporadas más importantes de Python con ejemplos prácticos para facilitar su comprensión.

## Funciones numéricas

### `abs()` - Valor absoluto
Devuelve el valor absoluto (positivo) de un número.
```python
print(abs(-5))  # 5
print(abs(3.7))  # 3.7
```

### `int()`, `float()`, `complex()` - Conversión de tipos numéricos
Convierten valores a números enteros, decimales o complejos.
```python
print(int("123"))  # 123
print(float("3.14"))  # 3.14
print(complex(2, 3))  # 2+3j
```

### `round()` - Redondeo de números
Redondea un número a un número específico de decimales.
```python
print(round(3.75))  # 4
print(round(3.75, 1))  # 3.8
```

### `pow()` - Potencia
Eleva un número a una potencia.
```python
print(pow(2, 3))  # 8 (2³)
```

## Funciones de secuencias y colecciones

### `len()` - Longitud
Devuelve el número de elementos en un objeto.
```python
print(len("Hola"))  # 4
print(len([1, 2, 3]))  # 3
```

### `list()`, `tuple()`, `set()`, `dict()` - Creación de colecciones
Crean o convierten valores a listas, tuplas, conjuntos o diccionarios.
```python
print(list("abc"))  # ['a', 'b', 'c']
print(tuple([1, 2, 3]))  # (1, 2, 3)
print(set([1, 2, 2, 3]))  # {1, 2, 3}
print(dict(a=1, b=2))  # {'a': 1, 'b': 2}
```

### `sorted()` - Ordenación
Devuelve una lista ordenada a partir de un iterable.
```python
print(sorted([3, 1, 2]))  # [1, 2, 3]
print(sorted("bca"))  # ['a', 'b', 'c']
```

### `min()`, `max()` - Valor mínimo y máximo
Devuelven el valor mínimo o máximo de una secuencia.
```python
print(min(5, 3, 8))  # 3
print(max([1, 2, 3]))  # 3
```

### `sum()` - Suma
Suma todos los elementos de un iterable.
```python
print(sum([1, 2, 3]))  # 6
```

## Iteración y generación de secuencias

### `range()` - Generación de secuencias numéricas
Genera una secuencia de números.
```python
print(list(range(5)))  # [0, 1, 2, 3, 4]
print(list(range(2, 5)))  # [2, 3, 4]
print(list(range(0, 10, 2)))  # [0, 2, 4, 6, 8]
```

### `enumerate()` - Enumeración
Devuelve pares de índice y valor de un iterable.
```python
for i, valor in enumerate(['a', 'b', 'c']):
    print(i, valor)
# 0 a
# 1 b
# 2 c
```

### `zip()` - Combinar iterables
Combina elementos de múltiples iterables.
```python
nombres = ['Ana', 'Juan']
edades = [25, 30]
for nombre, edad in zip(nombres, edades):
    print(f"{nombre} tiene {edad} años")
# Ana tiene 25 años
# Juan tiene 30 años
```

### `filter()` - Filtrar elementos
Filtra elementos de un iterable según una función.
```python
def es_par(n):
    return n % 2 == 0

numeros = [1, 2, 3, 4, 5]
pares = list(filter(es_par, numeros))
print(pares)  # [2, 4]
```

### `map()` - Transformar elementos
Aplica una función a cada elemento de un iterable.
```python
def cuadrado(n):
    return n ** 2

numeros = [1, 2, 3]
cuadrados = list(map(cuadrado, numeros))
print(cuadrados)  # [1, 4, 9]
```

## Conversión y representación

### `str()` - Conversión a cadena
Convierte un objeto a su representación como cadena.
```python
print(str(123))  # "123"
```

### `bool()` - Conversión a booleano
Convierte un valor a True o False.
```python
print(bool(0))  # False
print(bool(1))  # True
print(bool(""))  # False
print(bool("hola"))  # True
```

### `bin()`, `hex()`, `oct()` - Representación de números
Convierten números a representación binaria, hexadecimal u octal.
```python
print(bin(10))  # '0b1010'
print(hex(255))  # '0xff'
print(oct(8))  # '0o10'
```

## Entrada/Salida

### `print()` - Mostrar información
Muestra información en la consola.
```python
print("Hola mundo")
print("Hola", "mundo", sep=", ")  # Hola, mundo
```

### `input()` - Obtener entrada del usuario
Lee una línea de la entrada estándar.
```python
nombre = input("¿Cómo te llamas? ")
print(f"Hola {nombre}")
```

### `open()` - Abrir archivos
Abre un archivo para lectura, escritura, etc.
```python
# Leer un archivo
with open("archivo.txt", "r") as f:
    contenido = f.read()
    
# Escribir en un archivo
with open("salida.txt", "w") as f:
    f.write("Hola mundo")
```

## Inspección y reflexión

### `type()` - Tipo de un objeto
Devuelve el tipo de un objeto.
```python
print(type(123))  # <class 'int'>
print(type("hola"))  # <class 'str'>
```

### `isinstance()` - Comprobar tipo
Comprueba si un objeto es instancia de una clase.
```python
print(isinstance(5, int))  # True
print(isinstance("hola", list))  # False
```

### `dir()` - Listar atributos
Lista los atributos y métodos de un objeto.
```python
print(dir("hola"))  # Lista todos los métodos y atributos de una cadena
```

### `help()` - Obtener ayuda
Muestra la documentación de un objeto.
```python
help(print)  # Muestra la documentación de la función print
```

## Evaluación y ejecución

### `eval()` - Evaluar expresiones
Evalúa una expresión Python representada como cadena.
```python
print(eval("2 + 3"))  # 5
```

### `exec()` - Ejecutar código
Ejecuta dinámicamente código Python.
```python
exec("for i in range(3): print(i)")
# 0
# 1
# 2
```

## Otras funciones útiles

### `all()` y `any()` - Comprobación de condiciones
`all()` devuelve True si todos los elementos son verdaderos.
`any()` devuelve True si al menos un elemento es verdadero.
```python
print(all([True, True, True]))  # True
print(all([True, False, True]))  # False
print(any([False, False, True]))  # True
print(any([False, False, False]))  # False
```

### `chr()` y `ord()` - Conversión entre caracteres y códigos Unicode
```python
print(chr(65))  # 'A'
print(ord('A'))  # 65
```

### `getattr()`, `hasattr()`, `setattr()` - Manipulación de atributos
Permiten acceder, comprobar y modificar atributos de objetos.
```python
class Persona:
    nombre = "Ana"

p = Persona()
print(hasattr(p, 'nombre'))  # True
print(getattr(p, 'nombre'))  # 'Ana'
setattr(p, 'edad', 25)
print(p.edad)  # 25
```

### `globals()` y `locals()` - Diccionarios de variables
Devuelven diccionarios con las variables globales o locales.
```python
x = 10
def funcion():
    y = 5
    print(locals())  # {'y': 5}
    print(globals()['x'])  # 10

funcion()
```

Estas son las funciones más comunes y útiles para comenzar. Cada una tiene características adicionales que puedes explorar a medida que avances en tu aprendizaje de Python.
