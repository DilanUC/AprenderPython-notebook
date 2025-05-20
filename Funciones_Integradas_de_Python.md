# TAREAS
---
# Funciones Integradas de Python: Explicación Simple con Ejemplos

Este documento explica las funciones integradas más comunes de Python con ejemplos sencillos que cualquier persona puede entender, incluso sin experiencia previa en programación.

## Funciones Numéricas y Matemáticas

### `abs()` - Valor absoluto
Convierte cualquier número en positivo.
```python
abs(-10)  # Resultado: 10
abs(5)    # Resultado: 5
```
*Uso práctico:* Calcular la distancia entre dos puntos, independientemente de la dirección.

### `round()` - Redondear números
Redondea un número decimal al entero más cercano o a los decimales especificados.
```python
round(3.7)    # Resultado: 4
round(3.14159, 2)  # Resultado: 3.14
```
*Uso práctico:* Presentar precios o medidas de forma más limpia.

### `sum()` - Sumar elementos
Suma todos los números en una lista.
```python
sum([5, 10, 15, 20])  # Resultado: 50
```
*Uso práctico:* Calcular el total de una lista de gastos o calificaciones.

### `max()` - Valor máximo
Encuentra el valor más grande.
```python
max(10, 5, 20, 15)  # Resultado: 20
max([1, 2, 3, 4])   # Resultado: 4
```
*Uso práctico:* Encontrar la temperatura más alta o la venta mayor del mes.

### `min()` - Valor mínimo
Encuentra el valor más pequeño.
```python
min(10, 5, 20, 15)  # Resultado: 5
min([1, 2, 3, 4])   # Resultado: 1
```
*Uso práctico:* Encontrar el precio más bajo entre varios productos.

### `pow()` - Potencia
Eleva un número a una potencia.
```python
pow(2, 3)  # Resultado: 8 (es decir, 2³ = 2×2×2)
```
*Uso práctico:* Calcular crecimiento exponencial o interés compuesto.

## Conversión de Tipos

### `int()` - Convertir a entero
Convierte un valor a número entero.
```python
int("123")  # Resultado: 123
int(45.67)  # Resultado: 45 (elimina la parte decimal)
```
*Uso práctico:* Convertir la edad de una persona ingresada como texto a un número.

### `float()` - Convertir a decimal
Convierte un valor a número decimal.
```python
float("3.14")  # Resultado: 3.14
float(5)       # Resultado: 5.0
```
*Uso práctico:* Convertir precios ingresados como texto a valores numéricos.

### `str()` - Convertir a texto
Convierte cualquier valor a texto (cadena de caracteres).
```python
str(123)    # Resultado: "123"
str(3.14)   # Resultado: "3.14"
```
*Uso práctico:* Mostrar un número como parte de un mensaje.

### `bool()` - Convertir a booleano
Convierte un valor a True (verdadero) o False (falso).
```python
bool(1)     # Resultado: True
bool(0)     # Resultado: False
bool("")    # Resultado: False (texto vacío)
bool("Hola")  # Resultado: True (texto no vacío)
```
*Uso práctico:* Verificar si una lista de tareas está vacía.

## Manejo de Colecciones y Secuencias

### `len()` - Longitud
Cuenta el número de elementos en una lista, texto u objeto.
```python
len("Hola mundo")     # Resultado: 10 (caracteres)
len([10, 20, 30, 40]) # Resultado: 4 (elementos)
```
*Uso práctico:* Verificar cuántas palabras tiene un texto o elementos hay en una lista.

### `list()` - Crear lista
Crea una lista a partir de un iterable o convierte otros tipos a lista.
```python
list("Hola")        # Resultado: ['H', 'o', 'l', 'a']
list(range(5))      # Resultado: [0, 1, 2, 3, 4]
```
*Uso práctico:* Convertir un conjunto de caracteres en una lista modificable.

### `tuple()` - Crear tupla
Crea una tupla (lista no modificable) a partir de un iterable.
```python
tuple([1, 2, 3])    # Resultado: (1, 2, 3)
```
*Uso práctico:* Almacenar datos que no deben cambiar, como coordenadas.

### `dict()` - Crear diccionario
Crea un diccionario (pares clave-valor).
```python
dict(nombre="Ana", edad=30)  # Resultado: {'nombre': 'Ana', 'edad': 30}
```
*Uso práctico:* Almacenar información de una persona o producto con sus características.

### `set()` - Crear conjunto
Crea un conjunto (colección sin elementos duplicados).
```python
set([1, 2, 2, 3, 3, 3])  # Resultado: {1, 2, 3}
```
*Uso práctico:* Eliminar duplicados de una lista de números o nombres.

### `sorted()` - Ordenar elementos
Devuelve una lista ordenada a partir de cualquier iterable.
```python
sorted([3, 1, 4, 2])         # Resultado: [1, 2, 3, 4]
sorted(["zanahoria", "banana", "manzana"])  # Resultado: ['banana', 'manzana', 'zanahoria']
```
*Uso práctico:* Ordenar una lista de precios o nombres alfabéticamente.

### `reversed()` - Invertir orden
Invierte el orden de los elementos.
```python
list(reversed([1, 2, 3]))    # Resultado: [3, 2, 1]
```
*Uso práctico:* Mostrar los elementos más recientes primero.

## Iteración y Generación de Secuencias

### `range()` - Generar secuencia de números
Genera una secuencia de números.
```python
list(range(5))        # Resultado: [0, 1, 2, 3, 4]
list(range(2, 8))     # Resultado: [2, 3, 4, 5, 6, 7]
list(range(0, 10, 2)) # Resultado: [0, 2, 4, 6, 8]
```
*Uso práctico:* Crear bucles que se repitan un número específico de veces.

### `enumerate()` - Agregar índices
Añade índices (posiciones) a los elementos de una secuencia.
```python
list(enumerate(['a', 'b', 'c']))  # Resultado: [(0, 'a'), (1, 'b'), (2, 'c')]

# Uso común en bucles:
for i, letra in enumerate(['a', 'b', 'c']):
    print(f"Índice {i}: {letra}")
# Imprime:
# Índice 0: a
# Índice 1: b
# Índice 2: c
```
*Uso práctico:* Numerar automáticamente los elementos de una lista.

### `zip()` - Combinar iterables
Combina elementos de dos o más iterables.
```python
nombres = ["Ana", "Juan", "María"]
edades = [25, 30, 22]
list(zip(nombres, edades))  # Resultado: [('Ana', 25), ('Juan', 30), ('María', 22)]

# Uso común en bucles:
for nombre, edad in zip(nombres, edades):
    print(f"{nombre} tiene {edad} años")
# Imprime:
# Ana tiene 25 años
# Juan tiene 30 años
# María tiene 22 años
```
*Uso práctico:* Juntar datos relacionados de diferentes listas.

### `filter()` - Filtrar elementos
Filtra elementos según una condición.
```python
def es_par(numero):
    return numero % 2 == 0

numeros = [1, 2, 3, 4, 5, 6]
list(filter(es_par, numeros))  # Resultado: [2, 4, 6]

# Con función lambda (más corto):
list(filter(lambda x: x % 2 == 0, numeros))  # Resultado: [2, 4, 6]
```
*Uso práctico:* Obtener solo los productos con descuento de una lista.

### `map()` - Transformar elementos
Aplica una función a cada elemento.
```python
def duplicar(numero):
    return numero * 2

numeros = [1, 2, 3, 4]
list(map(duplicar, numeros))  # Resultado: [2, 4, 6, 8]

# Con función lambda (más corto):
list(map(lambda x: x * 2, numeros))  # Resultado: [2, 4, 6, 8]
```
*Uso práctico:* Convertir una lista de precios a otra moneda.

## Entrada/Salida

### `print()` - Mostrar información
Muestra información en la pantalla.
```python
print("Hola mundo")  # Muestra: Hola mundo
print("Hola", "mundo", sep="-")  # Muestra: Hola-mundo
```
*Uso práctico:* Mostrar resultados o mensajes al usuario.

### `input()` - Obtener entrada del usuario
Lee lo que escribe el usuario.
```python
nombre = input("¿Cómo te llamas? ")
print(f"Hola, {nombre}")
```
*Uso práctico:* Recoger información del usuario para procesarla.

### `open()` - Abrir archivos
Abre archivos para leer o escribir.
```python
# Leer un archivo
with open("notas.txt", "r") as archivo:
    contenido = archivo.read()
    print(contenido)

# Escribir en un archivo
with open("saludo.txt", "w") as archivo:
    archivo.write("Hola mundo")
```
*Uso práctico:* Guardar datos de forma permanente o leer información de archivos.

## Inspección y Reflexión

### `type()` - Tipo de dato
Devuelve el tipo de un objeto.
```python
type(123)      # Resultado: <class 'int'>
type("hola")   # Resultado: <class 'str'>
type([1, 2, 3])  # Resultado: <class 'list'>
```
*Uso práctico:* Verificar qué tipo de dato tenemos antes de procesarlo.

### `isinstance()` - Comprobar tipo
Comprueba si un objeto es de un tipo específico.
```python
isinstance(5, int)      # Resultado: True (5 es un entero)
isinstance("hola", str)  # Resultado: True ("hola" es un texto)
isinstance("hola", int)  # Resultado: False ("hola" no es un entero)
```
*Uso práctico:* Validar que una variable contiene el tipo de dato esperado.

### `dir()` - Ver atributos y métodos
Muestra qué operaciones podemos realizar con un objeto.
```python
dir("hola")  # Muestra todos los métodos disponibles para un texto
# Resultado: ['__add__', '__class__', ... 'upper', 'zfill']
```
*Uso práctico:* Descubrir qué podemos hacer con un tipo de dato específico.

### `help()` - Obtener ayuda
Muestra información de ayuda sobre funciones, métodos o módulos.
```python
help(print)  # Muestra documentación de la función print
```
*Uso práctico:* Aprender cómo usar correctamente una función.

## Verificación de Condiciones

### `all()` - Todos verdaderos
Devuelve True si todos los elementos son verdaderos.
```python
all([True, True, True])   # Resultado: True
all([True, False, True])  # Resultado: False
all([1, 2, 3])            # Resultado: True (números no-cero son True)
all([1, 0, 3])            # Resultado: False (0 es False)
```
*Uso práctico:* Verificar que todas las condiciones en una lista se cumplen.

### `any()` - Alguno verdadero
Devuelve True si al menos un elemento es verdadero.
```python
any([False, False, True])  # Resultado: True
any([False, False, False]) # Resultado: False
any([0, "", None, 1])      # Resultado: True (1 es True)
```
*Uso práctico:* Verificar si al menos una condición en una lista se cumple.

## Conversión y Representación

### `bin()`, `hex()`, `oct()` - Conversión de base
Convierten números a representación binaria, hexadecimal u octal.
```python
bin(10)  # Resultado: '0b1010' (binario)
hex(255) # Resultado: '0xff' (hexadecimal)
oct(8)   # Resultado: '0o10' (octal)
```
*Uso práctico:* Trabajar con diferentes sistemas numéricos en programación.

### `chr()` y `ord()` - Caracteres y códigos
Convierten entre caracteres y sus códigos numéricos.
```python
chr(65)   # Resultado: 'A' (carácter con código 65)
ord('A')  # Resultado: 65 (código del carácter 'A')
```
*Uso práctico:* Procesamiento de texto a nivel de caracteres.

## Otros Útiles

### `id()` - Identificador de objeto
Devuelve un identificador único para un objeto.
```python
x = [1, 2, 3]
y = x
id(x) == id(y)  # Resultado: True (son el mismo objeto)

z = [1, 2, 3]  # Una nueva lista con el mismo contenido
id(x) == id(z)  # Resultado: False (son objetos diferentes)
```
*Uso práctico:* Verificar si dos variables apuntan al mismo objeto en memoria.

### `format()` - Formatear texto
Da formato a texto incluyendo valores variables.
```python
"Hola, {}".format("Juan")  # Resultado: "Hola, Juan"
"{} tiene {} años".format("Ana", 25)  # Resultado: "Ana tiene 25 años"
```
*Uso práctico:* Crear mensajes personalizados insertando valores en el texto.

### `getattr()`, `hasattr()`, `setattr()` - Manipulación de atributos
Permiten trabajar con atributos de objetos de forma dinámica.
```python
class Persona:
    nombre = "Ana"

p = Persona()
hasattr(p, 'nombre')  # Resultado: True (tiene el atributo 'nombre')
getattr(p, 'nombre')  # Resultado: 'Ana' (valor del atributo)
setattr(p, 'edad', 25)  # Establece un nuevo atributo
p.edad  # Resultado: 25
```
*Uso práctico:* Manipular propiedades de objetos de forma dinámica.

### `eval()` - Evaluar expresiones
Evalúa una expresión Python representada como texto.
```python
eval("2 + 3")  # Resultado: 5
x = 10
eval("x * 2")  # Resultado: 20
```
*Uso práctico:* Convertir una expresión matemática escrita como texto a su resultado.

### `exec()` - Ejecutar código
Ejecuta código Python representado como texto.
```python
exec("x = 5")
print(x)  # Muestra: 5

exec("for i in range(3): print(i)")
# Muestra:
# 0
# 1
# 2
```
*Uso práctico:* Ejecutar código generado dinámicamente.

## Ejemplo práctico: Analizador de gastos

Este ejemplo combina varias funciones para crear una aplicación útil:

```python
# Registro de gastos semanales
gastos = [
    {"día": "Lunes", "importe": 15.50, "categoría": "Comida"},
    {"día": "Martes", "importe": 30.00, "categoría": "Transporte"},
    {"día": "Martes", "importe": 10.25, "categoría": "Comida"},
    {"día": "Miércoles", "importe": 15.00, "categoría": "Ocio"},
    {"día": "Jueves", "importe": 25.75, "categoría": "Comida"},
    {"día": "Viernes", "importe": 50.00, "categoría": "Ocio"},
    {"día": "Sábado", "importe": 45.30, "categoría": "Comida"},
    {"día": "Domingo", "importe": 10.00, "categoría": "Transporte"}
]

# Calcular gasto total
total = sum(gasto["importe"] for gasto in gastos)
print(f"Gasto total: {total}€")  # 201.8€

# Obtener categorías únicas usando set
categorías = set(gasto["categoría"] for gasto in gastos)
print(f"Categorías: {categorías}")  # {'Comida', 'Transporte', 'Ocio'}

# Filtrar gastos en comida
gastos_comida = list(filter(lambda g: g["categoría"] == "Comida", gastos))
total_comida = sum(gasto["importe"] for gasto in gastos_comida)
print(f"Gasto en comida: {total_comida}€")  # 96.8€

# Día con mayor gasto
día_mayor_gasto = max(gastos, key=lambda g: g["importe"])
print(f"Mayor gasto: {día_mayor_gasto['importe']}€ el {día_mayor_gasto['día']}")  # 50.0€ el Viernes

# Ordenar gastos de mayor a menor
gastos_ordenados = sorted(gastos, key=lambda g: g["importe"], reverse=True)
print("\nGastos ordenados de mayor a menor:")
for i, gasto in enumerate(gastos_ordenados, 1):
    print(f"{i}. {gasto['día']}: {gasto['importe']}€ ({gasto['categoría']})")
```

Este ejemplo muestra cómo puedes usar múltiples funciones integradas de Python (`sum`, `set`, `filter`, `max`, `sorted`, `enumerate`) para analizar datos de gastos de forma práctica y útil.