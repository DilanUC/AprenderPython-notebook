He creado un archivo completo de referencia con todos los métodos de Python organizados por categorías. El documento incluye:

- Todos los métodos de cadenas (strings)
- Métodos de listas
- Métodos de diccionarios
- Métodos de conjuntos (sets)
- Métodos de tuplas
- Métodos personalizados para clases incluyendo todos los métodos mágicos (dunder)
- Métodos para manipulación de archivos
- Decoradores y descriptores
- Métodos de iteradores
- Métodos de gestores de contexto (context managers)

Cada método incluye:

- Una descripción clara
- Un ejemplo de uso con su resultado
- Tablas organizadas para facilitar la consulta

Esta referencia está basada en la documentación oficial de Python, pero presentada de forma más accesible y con ejemplos prácticos.

# Métodos de Python - Referencia Completa

## Métodos de Cadenas (Strings)

Los strings en Python son inmutables, por lo que todos sus métodos devuelven un nuevo string en lugar de modificar el original.

| Método | Descripción | Ejemplo |
|--------|-------------|---------|
| `capitalize()` | Convierte el primer carácter a mayúscula | `"hola mundo".capitalize()` → `"Hola mundo"` |
| `casefold()` | Convierte a minúsculas para comparaciones sin distinción de mayúsculas/minúsculas | `"Hola".casefold()` → `"hola"` |
| `center(width[, fillchar])` | Centra el string en un campo de ancho especificado | `"hola".center(10, '-')` → `"---hola---"` |
| `count(sub[, start[, end]])` | Cuenta apariciones de una subcadena | `"banana".count('a')` → `3` |
| `encode([encoding[, errors]])` | Codifica el string y devuelve una versión de bytes | `"hola".encode('utf-8')` → `b'hola'` |
| `endswith(suffix[, start[, end]])` | Verifica si el string termina con el sufijo | `"archivo.txt".endswith('.txt')` → `True` |
| `expandtabs([tabsize])` | Reemplaza tabuladores por espacios | `"a\tb".expandtabs(4)` → `"a   b"` |
| `find(sub[, start[, end]])` | Encuentra la subcadena y devuelve el índice más bajo | `"hola mundo".find('mundo')` → `5` |
| `format(*args, **kwargs)` | Formatea el string usando placeholders | `"{} tiene {} años".format("Ana", 25)` → `"Ana tiene 25 años"` |
| `format_map(mapping)` | Similar a format() pero usa un mapeo | `"{a} y {b}".format_map({"a": "X", "b": "Y"})` → `"X y Y"` |
| `index(sub[, start[, end]])` | Como find() pero lanza ValueError si no encuentra | `"hola".index('o')` → `1` |
| `isalnum()` | Verifica si todos los caracteres son alfanuméricos | `"abc123".isalnum()` → `True` |
| `isalpha()` | Verifica si todos los caracteres son alfabéticos | `"abc".isalpha()` → `True` |
| `isascii()` | Verifica si todos los caracteres son ASCII | `"hello".isascii()` → `True` |
| `isdecimal()` | Verifica si todos los caracteres son decimales | `"123".isdecimal()` → `True` |
| `isdigit()` | Verifica si todos los caracteres son dígitos | `"123".isdigit()` → `True` |
| `isidentifier()` | Verifica si es un identificador válido en Python | `"variable_1".isidentifier()` → `True` |
| `islower()` | Verifica si todos los caracteres están en minúsculas | `"abc".islower()` → `True` |
| `isnumeric()` | Verifica si todos los caracteres son numéricos | `"123".isnumeric()` → `True` |
| `isprintable()` | Verifica si todos los caracteres son imprimibles | `"Hola\n".isprintable()` → `False` |
| `isspace()` | Verifica si todos los caracteres son espacios | `"   ".isspace()` → `True` |
| `istitle()` | Verifica si es un título (primera letra de cada palabra en mayúscula) | `"Hola Mundo".istitle()` → `True` |
| `isupper()` | Verifica si todos los caracteres están en mayúsculas | `"ABC".isupper()` → `True` |
| `join(iterable)` | Une elementos de un iterable con el string como separador | `"-".join(["a", "b", "c"])` → `"a-b-c"` |
| `ljust(width[, fillchar])` | Justifica a la izquierda en un campo de ancho especificado | `"hola".ljust(10, '*')` → `"hola******"` |
| `lower()` | Convierte todos los caracteres a minúsculas | `"HOLA".lower()` → `"hola"` |
| `lstrip([chars])` | Elimina espacios en blanco a la izquierda | `"  hola  ".lstrip()` → `"hola  "` |
| `maketrans(x[, y[, z]])` | Crea una tabla de traducción para translate() | `str.maketrans("abc", "123")` |
| `partition(sep)` | Divide en 3 partes (antes, separador, después) | `"a-b".partition('-')` → `('a', '-', 'b')` |
| `removeprefix(prefix)` | Elimina prefijo si existe | `"TestCase".removeprefix('Test')` → `"Case"` |
| `removesuffix(suffix)` | Elimina sufijo si existe | `"filename.txt".removesuffix('.txt')` → `"filename"` |
| `replace(old, new[, count])` | Reemplaza subcadenas | `"banana".replace('a', 'e')` → `"benene"` |
| `rfind(sub[, start[, end]])` | Encuentra el índice más alto de una subcadena | `"banana".rfind('a')` → `5` |
| `rindex(sub[, start[, end]])` | Como rfind() pero lanza ValueError si no encuentra | `"banana".rindex('a')` → `5` |
| `rjust(width[, fillchar])` | Justifica a la derecha | `"hola".rjust(10, '*')` → `"******hola"` |
| `rpartition(sep)` | Divide en 3 partes desde la derecha | `"a-b-c".rpartition('-')` → `('a-b', '-', 'c')` |
| `rsplit([sep[, maxsplit]])` | Divide desde la derecha | `"a-b-c".rsplit('-', 1)` → `['a-b', 'c']` |
| `rstrip([chars])` | Elimina espacios en blanco a la derecha | `"  hola  ".rstrip()` → `"  hola"` |
| `split([sep[, maxsplit]])` | Divide el string en una lista | `"a,b,c".split(',')` → `['a', 'b', 'c']` |
| `splitlines([keepends])` | Divide por líneas | `"a\nb\nc".splitlines()` → `['a', 'b', 'c']` |
| `startswith(prefix[, start[, end]])` | Verifica si comienza con el prefijo | `"hola".startswith('ho')` → `True` |
| `strip([chars])` | Elimina espacios en blanco al inicio y final | `"  hola  ".strip()` → `"hola"` |
| `swapcase()` | Invierte mayúsculas/minúsculas | `"Hola".swapcase()` → `"hOLA"` |
| `title()` | Convierte a formato título | `"hola mundo".title()` → `"Hola Mundo"` |
| `translate(table)` | Traduce usando una tabla de mapeo | `"abc".translate(str.maketrans("abc", "123"))` → `"123"` |
| `upper()` | Convierte a mayúsculas | `"hola".upper()` → `"HOLA"` |
| `zfill(width)` | Rellena con ceros a la izquierda | `"42".zfill(5)` → `"00042"` |

## Métodos de Listas

Las listas en Python son mutables, por lo que muchos métodos modifican la lista original.

| Método | Descripción | Ejemplo |
|--------|-------------|---------|
| `append(x)` | Añade un elemento al final | `l = [1, 2]; l.append(3)` → `l = [1, 2, 3]` |
| `clear()` | Elimina todos los elementos | `l = [1, 2]; l.clear()` → `l = []` |
| `copy()` | Devuelve una copia superficial | `l = [1, 2]; l2 = l.copy()` → `l2 = [1, 2]` |
| `count(x)` | Cuenta apariciones de un valor | `[1, 2, 1, 3].count(1)` → `2` |
| `extend(iterable)` | Extiende con elementos de un iterable | `l = [1, 2]; l.extend([3, 4])` → `l = [1, 2, 3, 4]` |
| `index(x[, start[, end]])` | Devuelve el índice del primer valor x | `[1, 2, 3].index(2)` → `1` |
| `insert(i, x)` | Inserta x en la posición i | `l = [1, 3]; l.insert(1, 2)` → `l = [1, 2, 3]` |
| `pop([i])` | Elimina y devuelve el elemento en la posición i | `[1, 2, 3].pop(1)` → `2` |
| `remove(x)` | Elimina la primera aparición de x | `l = [1, 2, 1]; l.remove(1)` → `l = [2, 1]` |
| `reverse()` | Invierte el orden de los elementos | `l = [1, 2, 3]; l.reverse()` → `l = [3, 2, 1]` |
| `sort([key][, reverse])` | Ordena los elementos | `l = [3, 1, 2]; l.sort()` → `l = [1, 2, 3]` |

## Métodos de Diccionarios

Los diccionarios son estructuras clave-valor mutables.

| Método | Descripción | Ejemplo |
|--------|-------------|---------|
| `clear()` | Elimina todos los elementos | `d = {'a': 1}; d.clear()` → `d = {}` |
| `copy()` | Devuelve una copia superficial | `d = {'a': 1}; d2 = d.copy()` → `d2 = {'a': 1}` |
| `fromkeys(iterable[, value])` | Crea un diccionario con las claves y un valor por defecto | `dict.fromkeys(['a', 'b'], 0)` → `{'a': 0, 'b': 0}` |
| `get(key[, default])` | Devuelve el valor de una clave o default si no existe | `{'a': 1}.get('b', 0)` → `0` |
| `items()` | Devuelve una vista de pares (clave, valor) | `{'a': 1}.items()` → `dict_items([('a', 1)])` |
| `keys()` | Devuelve una vista de las claves | `{'a': 1, 'b': 2}.keys()` → `dict_keys(['a', 'b'])` |
| `pop(key[, default])` | Elimina y devuelve el valor de una clave | `d = {'a': 1}; d.pop('a')` → `1` y `d = {}` |
| `popitem()` | Elimina y devuelve un par (clave, valor) | `d = {'a': 1}; d.popitem()` → `('a', 1)` y `d = {}` |
| `setdefault(key[, default])` | Devuelve el valor si existe, sino inserta key:default y lo devuelve | `d = {}; d.setdefault('a', 1)` → `1` y `d = {'a': 1}` |
| `update([other])` | Actualiza el diccionario con pares de otro diccionario | `d = {'a': 1}; d.update({'b': 2})` → `d = {'a': 1, 'b': 2}` |
| `values()` | Devuelve una vista de los valores | `{'a': 1, 'b': 2}.values()` → `dict_values([1, 2])` |

## Métodos de Conjuntos (Sets)

Los conjuntos son colecciones no ordenadas de elementos únicos.

| Método | Descripción | Ejemplo |
|--------|-------------|---------|
| `add(elem)` | Añade un elemento | `s = {1, 2}; s.add(3)` → `s = {1, 2, 3}` |
| `clear()` | Elimina todos los elementos | `s = {1, 2}; s.clear()` → `s = set()` |
| `copy()` | Devuelve una copia superficial | `s = {1, 2}; s2 = s.copy()` → `s2 = {1, 2}` |
| `difference(*others)` | Devuelve los elementos que están en este set pero no en los otros | `{1, 2, 3}.difference({2, 3, 4})` → `{1}` |
| `difference_update(*others)` | Elimina los elementos que están en otros | `s = {1, 2, 3}; s.difference_update({2, 3})` → `s = {1}` |
| `discard(elem)` | Elimina un elemento si existe | `s = {1, 2}; s.discard(2)` → `s = {1}` |
| `intersection(*others)` | Devuelve los elementos comunes | `{1, 2, 3}.intersection({2, 3, 4})` → `{2, 3}` |
| `intersection_update(*others)` | Actualiza el set con la intersección | `s = {1, 2, 3}; s.intersection_update({2, 3, 4})` → `s = {2, 3}` |
| `isdisjoint(other)` | Verifica si no hay elementos comunes | `{1, 2}.isdisjoint({3, 4})` → `True` |
| `issubset(other)` | Verifica si este set es subconjunto de otro | `{1, 2}.issubset({1, 2, 3})` → `True` |
| `issuperset(other)` | Verifica si este set es superconjunto de otro | `{1, 2, 3}.issuperset({1, 2})` → `True` |
| `pop()` | Elimina y devuelve un elemento aleatorio | `s = {1, 2}; s.pop()` → `1` o `2` |
| `remove(elem)` | Elimina un elemento, error si no existe | `s = {1, 2}; s.remove(2)` → `s = {1}` |
| `symmetric_difference(other)` | Devuelve elementos que están en uno u otro set pero no en ambos | `{1, 2, 3}.symmetric_difference({2, 3, 4})` → `{1, 4}` |
| `symmetric_difference_update(other)` | Actualiza el set con la diferencia simétrica | `s = {1, 2, 3}; s.symmetric_difference_update({2, 3, 4})` → `s = {1, 4}` |
| `union(*others)` | Devuelve la unión de sets | `{1, 2}.union({3, 4})` → `{1, 2, 3, 4}` |
| `update(*others)` | Actualiza el set con la unión | `s = {1, 2}; s.update({3, 4})` → `s = {1, 2, 3, 4}` |

## Métodos de Tuplas

Las tuplas son secuencias inmutables.

| Método | Descripción | Ejemplo |
|--------|-------------|---------|
| `count(x)` | Cuenta apariciones de un valor | `(1, 2, 1, 3).count(1)` → `2` |
| `index(x[, start[, end]])` | Devuelve el índice del primer valor x | `(1, 2, 3).index(2)` → `1` |

## Métodos Personalizados (Clases)

Python permite definir métodos personalizados en clases. Aquí hay algunos métodos especiales comunes:

### Métodos Mágicos (Dunder Methods)

| Método | Descripción | Ejemplo |
|--------|-------------|---------|
| `__init__(self, ...)` | Constructor, inicializa un nuevo objeto | `def __init__(self, x): self.x = x` |
| `__str__(self)` | Representación de string para usuario | `def __str__(self): return f"Valor: {self.x}"` |
| `__repr__(self)` | Representación de string para desarrollador | `def __repr__(self): return f"{self.__class__.__name__}({self.x})"` |
| `__len__(self)` | Implementa len() | `def __len__(self): return len(self.items)` |
| `__getitem__(self, key)` | Implementa self[key] | `def __getitem__(self, key): return self.data[key]` |
| `__setitem__(self, key, value)` | Implementa self[key] = value | `def __setitem__(self, key, value): self.data[key] = value` |
| `__delitem__(self, key)` | Implementa del self[key] | `def __delitem__(self, key): del self.data[key]` |
| `__iter__(self)` | Hace que el objeto sea iterable | `def __iter__(self): return iter(self.data)` |
| `__next__(self)` | Implementa el iterador | `def __next__(self): ...` |
| `__contains__(self, item)` | Implementa in (pertenencia) | `def __contains__(self, item): return item in self.data` |
| `__call__(self, ...)` | Hace que el objeto sea llamable | `def __call__(self, x): return self.process(x)` |
| `__add__(self, other)` | Implementa self + other | `def __add__(self, other): return self.__class__(self.x + other.x)` |
| `__sub__(self, other)` | Implementa self - other | `def __sub__(self, other): return self.__class__(self.x - other.x)` |
| `__mul__(self, other)` | Implementa self * other | `def __mul__(self, other): return self.__class__(self.x * other)` |
| `__truediv__(self, other)` | Implementa self / other | `def __truediv__(self, other): return self.__class__(self.x / other)` |
| `__eq__(self, other)` | Implementa self == other | `def __eq__(self, other): return self.x == other.x` |
| `__lt__(self, other)` | Implementa self < other | `def __lt__(self, other): return self.x < other.x` |
| `__gt__(self, other)` | Implementa self > other | `def __gt__(self, other): return self.x > other.x` |
| `__le__(self, other)` | Implementa self <= other | `def __le__(self, other): return self.x <= other.x` |
| `__ge__(self, other)` | Implementa self >= other | `def __ge__(self, other): return self.x >= other.x` |
| `__enter__(self)` | Parte del protocolo de gestor de contexto | `def __enter__(self): return self` |
| `__exit__(self, exc_type, exc_val, exc_tb)` | Parte del protocolo de gestor de contexto | `def __exit__(self, *args): self.cleanup()` |

### Ejemplo de Clase con Métodos Personalizados

```python
class Vector:
    def __init__(self, x, y):
        self.x = x
        self.y = y
    
    def __str__(self):
        return f"Vector({self.x}, {self.y})"
    
    def __repr__(self):
        return f"Vector({self.x}, {self.y})"
    
    def __add__(self, other):
        return Vector(self.x + other.x, self.y + other.y)
    
    def __sub__(self, other):
        return Vector(self.x - other.x, self.y - other.y)
    
    def __mul__(self, scalar):
        return Vector(self.x * scalar, self.y * scalar)
    
    def __eq__(self, other):
        return self.x == other.x and self.y == other.y
    
    def magnitude(self):
        return (self.x**2 + self.y**2)**0.5
    
    @classmethod
    def from_polar(cls, r, theta):
        import math
        x = r * math.cos(theta)
        y = r * math.sin(theta)
        return cls(x, y)
    
    @staticmethod
    def dot_product(v1, v2):
        return v1.x * v2.x + v1.y * v2.y
```

## Métodos para Manipulación de Archivos

| Método | Descripción | Ejemplo |
|--------|-------------|---------|
| `close()` | Cierra el archivo | `f = open('archivo.txt'); f.close()` |
| `read([size])` | Lee el archivo | `open('archivo.txt').read()` → contenido completo |
| `readline([size])` | Lee una línea | `open('archivo.txt').readline()` → primera línea |
| `readlines()` | Lee todas las líneas en una lista | `open('archivo.txt').readlines()` → lista de líneas |
| `write(string)` | Escribe una cadena | `f.write('Hola mundo')` → escribe en el archivo |
| `writelines(lines)` | Escribe una lista de líneas | `f.writelines(['línea1\n', 'línea2\n'])` → escribe líneas |
| `seek(offset[, whence])` | Mueve el cursor | `f.seek(0)` → mueve al inicio del archivo |
| `tell()` | Devuelve la posición actual | `f.tell()` → posición actual del cursor |
| `flush()` | Fuerza escritura del buffer | `f.flush()` → garantiza que se escriban los datos |

## Decoradores y Descriptores

Los decoradores y descriptores son características avanzadas para manipular métodos y atributos.

### Decoradores

```python
# Decorador para medir tiempo de ejecución
import time
def timer(func):
    def wrapper(*args, **kwargs):
        start_time = time.time()
        result = func(*args, **kwargs)
        end_time = time.time()
        print(f"Tiempo de ejecución: {end_time - start_time} segundos")
        return result
    return wrapper

@timer
def operacion_lenta():
    time.sleep(2)
    return "Completado"
```

### Descriptores

```python
class Validador:
    def __init__(self, minimo=0, maximo=100):
        self.minimo = minimo
        self.maximo = maximo
        self.nombre = None
    
    def __set_name__(self, owner, name):
        self.nombre = name
    
    def __get__(self, instance, owner):
        if instance is None:
            return self
        return instance.__dict__.get(self.nombre, None)
    
    def __set__(self, instance, value):
        if not isinstance(value, (int, float)):
            raise TypeError(f"{self.nombre} debe ser un número")
        if value < self.minimo or value > self.maximo:
            raise ValueError(f"{self.nombre} debe estar entre {self.minimo} y {self.maximo}")
        instance.__dict__[self.nombre] = value

class Producto:
    precio = Validador(0, 1000)
    cantidad = Validador(0, 50)
    
    def __init__(self, nombre, precio, cantidad):
        self.nombre = nombre
        self.precio = precio
        self.cantidad = cantidad
```

## Métodos de Iteradores

| Método | Descripción | Ejemplo |
|--------|-------------|---------|
| `__iter__(self)` | Método que hace iterable a un objeto | `def __iter__(self): return self` |
| `__next__(self)` | Devuelve el siguiente elemento | `def __next__(self): ...` |

```python
class Contador:
    def __init__(self, inicio, fin):
        self.inicio = inicio
        self.fin = fin
        self.valor = inicio - 1
    
    def __iter__(self):
        return self
    
    def __next__(self):
        self.valor += 1
        if self.valor > self.fin:
            raise StopIteration
        return self.valor

# Uso
for num in Contador(1, 5):
    print(num)  # Imprime 1, 2, 3, 4, 5
```

## Métodos de Context Manager

| Método | Descripción | Ejemplo |
|--------|-------------|---------|
| `__enter__(self)` | Se ejecuta al entrar en el bloque with | `def __enter__(self): return self` |
| `__exit__(self, exc_type, exc_val, exc_tb)` | Se ejecuta al salir del bloque with | `def __exit__(self, *args): self.close()` |

```python
class TempFile:
    def __init__(self, nombre):
        self.nombre = nombre
        self.archivo = None
    
    def __enter__(self):
        self.archivo = open(self.nombre, 'w')
        return self.archivo
    
    def __exit__(self, exc_type, exc_val, exc_tb):
        if self.archivo:
            self.archivo.close()
        if exc_type is None:
            print("Operación completada con éxito")
        else:
            print(f"Ocurrió un error: {exc_val}")
        return False  # Propaga excepciones

# Uso
with TempFile("temp.txt") as f:
    f.write("Contenido temporal")
# El archivo se cierra automáticamente al salir del bloque with
```