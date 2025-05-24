# Guía de Estructuras en Python

## 1. ESTRUCTURAS CONDICIONALES

### IF, ELSE, ELIF

Las estructuras condicionales permiten ejecutar código según se cumplan ciertas condiciones.

#### Sintaxis básica:
```python
if condicion:
    # código si la condición es verdadera
elif otra_condicion:
    # código si la segunda condición es verdadera
else:
    # código si ninguna condición es verdadera
```

#### Ejemplos prácticos:

**Ejemplo 1: Verificar si un número es positivo**
```python
numero = 5

if numero > 0:
    print("El número es positivo")
elif numero < 0:
    print("El número es negativo")
else:
    print("El número es cero")
```

**Ejemplo 2: Sistema de calificaciones**
```python
calificacion = 85

if calificacion >= 90:
    print("Excelente - A")
elif calificacion >= 80:
    print("Muy bueno - B")
elif calificacion >= 70:
    print("Bueno - C")
elif calificacion >= 60:
    print("Regular - D")
else:
    print("Reprobado - F")
```

**Ejemplo 3: Condiciones múltiples con operadores lógicos**
```python
edad = 25
tiene_licencia = True

if edad >= 18 and tiene_licencia:
    print("Puede conducir")
elif edad >= 18 and not tiene_licencia:
    print("Necesita obtener licencia")
else:
    print("Es menor de edad")
```

## 2. ESTRUCTURAS DE REPETICIÓN

### FOR - Bucle con secuencias

El bucle `for` itera sobre elementos de una secuencia (lista, tupla, string, rango).

#### Sintaxis:
```python
for variable in secuencia:
    # código a repetir
```

#### Ejemplos:

**Ejemplo 1: Iterar sobre una lista**
```python
frutas = ["manzana", "banana", "naranja"]

for fruta in frutas:
    print(f"Me gusta la {fruta}")

# Salida:
# Me gusta la manzana
# Me gusta la banana
# Me gusta la naranja
```

**Ejemplo 2: Usar range() para números**
```python
# Imprimir números del 1 al 5
for i in range(1, 6):
    print(f"Número: {i}")

# Imprimir números pares del 0 al 10
for i in range(0, 11, 2):
    print(f"Número par: {i}")
```

**Ejemplo 3: Iterar con índice usando enumerate()**
```python
colores = ["rojo", "verde", "azul"]

for indice, color in enumerate(colores):
    print(f"Posición {indice}: {color}")

# Salida:
# Posición 0: rojo
# Posición 1: verde
# Posición 2: azul
```

**Ejemplo 4: For anidado**
```python
# Tabla de multiplicar
for i in range(1, 4):
    for j in range(1, 4):
        resultado = i * j
        print(f"{i} x {j} = {resultado}")
    print("---")
```

### WHILE - Bucle con condición

El bucle `while` se ejecuta mientras una condición sea verdadera.

#### Sintaxis:
```python
while condicion:
    # código a repetir
    # importante: modificar la condición para evitar bucle infinito
```

#### Ejemplos:

**Ejemplo 1: Contador simple**
```python
contador = 1

while contador <= 5:
    print(f"Contador: {contador}")
    contador += 1  # Importante: incrementar para evitar bucle infinito

print("Fin del bucle")
```

**Ejemplo 2: Juego de adivinanza**
```python
import random

numero_secreto = random.randint(1, 10)
adivinanza = 0

while adivinanza != numero_secreto:
    adivinanza = int(input("Adivina el número (1-10): "))
    
    if adivinanza < numero_secreto:
        print("Muy bajo")
    elif adivinanza > numero_secreto:
        print("Muy alto")
    else:
        print("¡Correcto!")
```

**Ejemplo 3: Validación de entrada**
```python
edad = -1

while edad < 0 or edad > 120:
    edad = int(input("Ingresa tu edad (0-120): "))
    if edad < 0 or edad > 120:
        print("Edad inválida, intenta de nuevo")

print(f"Tu edad es: {edad}")
```

### BREAK y CONTINUE

**BREAK**: Sale completamente del bucle
```python
for i in range(10):
    if i == 5:
        break  # Sale del bucle cuando i es 5
    print(i)
# Imprime: 0, 1, 2, 3, 4
```

**CONTINUE**: Salta a la siguiente iteración
```python
for i in range(10):
    if i % 2 == 0:
        continue  # Salta los números pares
    print(i)
# Imprime: 1, 3, 5, 7, 9
```

## 3. ESTRUCTURAS DE DATOS

### LISTAS (Arrays en otros lenguajes)

Las listas son colecciones ordenadas y mutables de elementos.

#### Creación de listas:
```python
# Lista vacía
lista_vacia = []
lista_vacia2 = list()

# Lista con elementos
numeros = [1, 2, 3, 4, 5]
frutas = ["manzana", "banana", "naranja"]
mixta = [1, "texto", 3.14, True]
```

#### Operaciones básicas:

**Acceso a elementos:**
```python
frutas = ["manzana", "banana", "naranja"]

print(frutas[0])    # manzana (primer elemento)
print(frutas[-1])   # naranja (último elemento)
print(frutas[1:3])  # ['banana', 'naranja'] (slicing)
```

**Modificación:**
```python
frutas = ["manzana", "banana", "naranja"]

# Cambiar un elemento
frutas[1] = "pera"
print(frutas)  # ['manzana', 'pera', 'naranja']

# Agregar elementos
frutas.append("uva")        # Agregar al final
frutas.insert(1, "kiwi")    # Insertar en posición específica

# Eliminar elementos
frutas.remove("pera")       # Eliminar por valor
elemento = frutas.pop()     # Eliminar y retornar el último
del frutas[0]              # Eliminar por índice
```

**Métodos útiles:**
```python
numeros = [3, 1, 4, 1, 5, 9, 2]

print(len(numeros))           # 7 (longitud)
print(numeros.count(1))       # 2 (cuántas veces aparece 1)
print(numeros.index(4))       # 2 (posición del 4)

numeros.sort()                # Ordenar en su lugar
print(numeros)                # [1, 1, 2, 3, 4, 5, 9]

numeros.reverse()             # Invertir orden
print(numeros)                # [9, 5, 4, 3, 2, 1, 1]
```

### TUPLAS

Las tuplas son colecciones ordenadas e inmutables.

```python
# Creación
coordenadas = (3, 5)
colores = ("rojo", "verde", "azul")
punto = 1, 2, 3  # Sin paréntesis también funciona

# Acceso (igual que listas)
print(coordenadas[0])  # 3
print(colores[-1])     # azul

# No se pueden modificar (son inmutables)
# coordenadas[0] = 10  # Esto daría error

# Útiles para datos que no deben cambiar
dimensiones = (1920, 1080)
```

### DICCIONARIOS

Los diccionarios almacenan pares clave-valor.

```python
# Creación
persona = {
    "nombre": "Juan",
    "edad": 30,
    "ciudad": "Madrid"
}

# Acceso
print(persona["nombre"])           # Juan
print(persona.get("edad"))         # 30
print(persona.get("telefono", "No disponible"))  # Valor por defecto

# Modificación
persona["edad"] = 31               # Cambiar valor existente
persona["telefono"] = "123-456"    # Agregar nueva clave

# Eliminar
del persona["ciudad"]              # Eliminar clave-valor
telefono = persona.pop("telefono") # Eliminar y obtener valor

# Métodos útiles
print(persona.keys())              # Todas las claves
print(persona.values())            # Todos los valores
print(persona.items())             # Pares clave-valor
```

### CONJUNTOS (SETS)

Los conjuntos almacenan elementos únicos sin orden específico.

```python
# Creación
numeros = {1, 2, 3, 4, 5}
letras = set("abcde")

# Operaciones
numeros.add(6)                     # Agregar elemento
numeros.remove(3)                  # Eliminar elemento (error si no existe)
numeros.discard(10)                # Eliminar elemento (sin error si no existe)

# Operaciones de conjuntos
conjunto1 = {1, 2, 3, 4}
conjunto2 = {3, 4, 5, 6}

print(conjunto1.union(conjunto2))        # {1, 2, 3, 4, 5, 6}
print(conjunto1.intersection(conjunto2)) # {3, 4}
print(conjunto1.difference(conjunto2))   # {1, 2}
```

## 4. EJEMPLOS INTEGRADOS

### Ejemplo 1: Lista de tareas con validación
```python
tareas = []

while True:
    print("\n=== LISTA DE TAREAS ===")
    print("1. Agregar tarea")
    print("2. Ver tareas")
    print("3. Marcar como completada")
    print("4. Salir")
    
    opcion = input("Elige una opción: ")
    
    if opcion == "1":
        tarea = input("Ingresa la nueva tarea: ")
        if tarea.strip():  # Verificar que no esté vacía
            tareas.append({"texto": tarea, "completada": False})
            print("Tarea agregada exitosamente")
        else:
            print("La tarea no puede estar vacía")
    
    elif opcion == "2":
        if tareas:
            print("\nTus tareas:")
            for i, tarea in enumerate(tareas):
                estado = "✓" if tarea["completada"] else "○"
                print(f"{i+1}. {estado} {tarea['texto']}")
        else:
            print("No hay tareas")
    
    elif opcion == "3":
        if tareas:
            try:
                numero = int(input("Número de tarea a completar: ")) - 1
                if 0 <= numero < len(tareas):
                    tareas[numero]["completada"] = True
                    print("Tarea marcada como completada")
                else:
                    print("Número de tarea inválido")
            except ValueError:
                print("Por favor ingresa un número válido")
        else:
            print("No hay tareas para completar")
    
    elif opcion == "4":
        print("¡Hasta luego!")
        break
    
    else:
        print("Opción inválida")
```

### Ejemplo 2: Análisis de datos simples
```python
# Datos de ventas por mes
ventas = {
    "enero": [1200, 1500, 1100, 1800],
    "febrero": [1300, 1600, 1400, 1900],
    "marzo": [1100, 1400, 1200, 1700]
}

print("=== ANÁLISIS DE VENTAS ===")

for mes, valores in ventas.items():
    total = sum(valores)
    promedio = total / len(valores)
    maximo = max(valores)
    minimo = min(valores)
    
    print(f"\n{mes.upper()}:")
    print(f"  Total: ${total:,}")
    print(f"  Promedio: ${promedio:,.2f}")
    print(f"  Venta máxima: ${maximo:,}")
    print(f"  Venta mínima: ${minimo:,}")
    
    # Encontrar días con ventas por encima del promedio
    dias_buenos = []
    for i, venta in enumerate(valores):
        if venta > promedio:
            dias_buenos.append(f"día {i+1}")
    
    if dias_buenos:
        print(f"  Días por encima del promedio: {', '.join(dias_buenos)}")
```

## CONSEJOS IMPORTANTES

1. **Indentación**: Python usa espacios (generalmente 4) para definir bloques de código
2. **Condiciones**: Usar `==` para comparar, `=` para asignar
3. **Bucles infinitos**: Siempre asegurar que la condición del `while` pueda cambiar
4. **Índices**: Las listas empiezan en 0, el último elemento es -1
5. **Mutabilidad**: Las listas y diccionarios se pueden modificar, las tuplas y strings no
6. **Buenas prácticas**: Usar nombres descriptivos para variables y funciones