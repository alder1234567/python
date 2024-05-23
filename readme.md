# Ejercicio Uno: 
# > Escribir un programa para una empresa que tiene salas de juegos para todas las edades
# y quiere calcular de forma automatica el precio que debe cobrar a sus clientes por entrar. 
# El programa debe preguntar al usuario la edad del cliente y mostrar el precio de la entrada.
# Si el cliente es menor de 4 puede entrar gratis, si tiene entre 4 y 18 debe pagar 5 soles, y 
# si es mayor de 18 deberá pagar 10 soles.

# Solicitar la edad del cliente al usuario
edad = int(input("Ingrese la edad del cliente: "))

# Calcular el precio de la entrada según la edad
if edad < 4:
    precio = 0
elif 4 <= edad <= 18:
    precio = 5
else:
    precio = 10

# Mostrar el precio de la entrada por terminal
print("El precio de la entrada es:", precio, "soles")
 
## Ejercicio Dos:
# > Escribir un programa que pida al usuario una palabra y la muestre por pantalla 10 veces

# Solicitar al usuario una palabra
palabra = input("Ingresa una palabra: ")

# Mostrar la palabra 10 veces por terminal
for _ in range(10):
    print(palabra)
 
 
## Ejercicio Tres: 
#  > Escribir un programa que pida al usuario un número entero positivo y muestre por pantalla 
# todos los números impares desde 1 hasta ese número separados por comas.

# Solicitar al usuario un número entero positivo
numero = int(input("Ingrese un número entero positivo: "))

# Mostrar los números desde 1 hasta el número dado
print("Números desde 1 hasta", numero, ":")
for i in range(1, numero + 1):
    print(i, end=" ")
 
## Ejercicio Cuatro: 
# > Escribir un programa que muestre por pantalla la tabla de multiplicar del 1 al 10. 

# Mostrar la tabla de multiplicar del 1 al 10
for i in range(1, 11):
    print(f"Tabla de multiplicar del {i}:")
    for j in range(1, 11):
        resultado = i * j
        print(f"{i} x {j} = {resultado}")
    print()
 
 
## Ejercicio Cinco: 
# > Escribir un programa que pida al usuario una palabra y luego muestre por pantalla una
# a una las letras de la palabra introducida empezando por la última.

# Solicitar al usuario una palabra
palabra = input("Ingresa una palabra: ")

# Mostrar las letras de la palabra introducida empezando por la última
for letra in reversed(palabra):
    print(letra)
 
 
## Ejercicio Seis: 
# > Escribir un programa que pida al usuario un número entero y muestre por pantalla un triángulo 
# rectángulo como el de la imagen adjunta. 
# 1
# 31
# 531
# 7531
# 97531
 
# Solicitar al usuario un número entero
numero = int(input("Ingrese un número entero: "))

# Mostrar un triángulo rectángulo con números en el patrón dado
for i in range(1, numero + 1):
    for j in range(i, 0, -1):
        print(j, end="")
    print()
 
## Ejercicio Siete:
# > Escribir un programa en el que se pregunte al usuario por una frase y una letra, y muestre por
# pantalla el número de veces que aparece la letra en la frase.

# Solicitar al usuario una frase y una letra
frase = input("Ingrese una frase: ")
letra = input("Ingrese una letra: ")

# Contar el número de veces que aparece la letra en la frase
contador = frase.count(letra)
print(f"La letra '{letra}' aparece {contador} veces en la frase.")

## Ejercicio Ocho:
# > Escribir un programa que pida al usuario una palabra y luego muestre por pantalla una a una las 
# letras de la palabra introducida empezando por la última.

# Solicitar al usuario una frase y una letra
frase = input("Ingrese una frase: ")
letra = input("Ingrese una letra: ")

# Contar el número de veces que aparece la letra en la frase
contador = frase.count(letra)
print(f"La letra '{letra}' aparece {contador} veces en la frase.")


## Ejercicio Nueve:
# > Escriba un programa que pregunte cuántos números se van a introducir, luego pida esos números, y
# muestre un mensaje cada vez que un número no sea mayor que el anterior.

cantidad_numeros = int(input("¿Cuántos números vas a introducir? "))

if cantidad_numeros > 0:
    numero_anterior = int(input("Introduce el primer número: "))
    for i in range(1, cantidad_numeros):
        numero_actual = int(input("Introduce el siguiente número: "))
        if numero_actual <= numero_anterior:
            print("El número introducido no es mayor que el anterior.")
        numero_anterior = numero_actual
else:
    print("No se han introducido números.")


## Ejercicio Diez:
# > Escribir un programa en el que se pregunte al usuario por una frase y una letra, y muestre por pantalla 
# el número de veces que aparece la letra en la frase.

# Solicitar al usuario una frase y una letra
frase = input("Ingrese una frase: ")
letra = input("Ingrese una letra: ")

# Contar el número de veces que aparece la letra en la frase
contador = frase.count(letra)
print(f"La letra '{letra}' aparece {contador} veces en la frase.")

## Ejercicio Once:
# > Escriba un programa que pregunte cuantos números se van a introducir, pida los esos números (que puedan ser decimales)
# y calcule su suma, mostrar por terminal la suma de los números introducidos.

# Solicitar al usuario cuántos números va a introducir
cantidad_numeros = int(input("¿Cuántos números vas a introducir? "))

# Inicializar la variable para almacenar la suma de los números
suma = 0

# Pedir los números al usuario y calcular la suma
for i in range(cantidad_numeros):
    numero = float(input("Introduce un número: "))
    suma += numero

# Mostrar la suma de los números introducidos por terminal
print("La suma de los números introducidos es:", suma)

## Ejercicio Doce:
# > Escriba un programa que pregunte cuántos números se van a introducir, pida esos números y escriba cuántos 
# negativos ha introducido.

# Pedir al usuario cuántos números se van a introducir
num_numeros = int(input("¿Cuántos números vas a introducir? "))

# Inicializar contador de números negativos
contador_negativos = 0

# Pedir los números al usuario y contar los negativos
for i in range(num_numeros):
    numero = int(input(f"Introduce el número {i+1}: "))
    if numero < 0:
        contador_negativos += 1

# Mostrar la cantidad de números negativos introducidos
print(f"Has introducido {contador_negativos} números negativos.")
[9:06 p.m., 21/5/2024] Wiliam: *Ejercicio Trece*
##Vamos a diseñar una calculadora que se enciende y hasta que no tecleamos SAL no se apaga.
#
##Esta calculadora funciona de la siguiente manera:
#
##- Recogemos los datos A y B
##- Si operación es 1 calcula la raíz cuadrada de la suma de A y B
##- Si operación es 2 calcula A / B. Vigilamos que B no sea 0...
##- Si la operación es 3 calculamos la siguiente fórmula: ( A * B ) / 2.5

# Función para calcular la raíz cuadrada de la suma de A y B
def calcular_raiz_cuadrada_suma(A, B):
    return (A + B) ** 0.5

# Función para calcular A / B
def calcular_division(A, B):
    return A / B if B != 0 else "Error: No se puede dividir por cero."

# Función para calcular (A * B) / 2.5
def calcular_formula(A, B):
    return (A * B) / 2.5

# Encender la calculadora
while True:
    # Solicitar al usuario los datos A, B y la operación
    A = float(input("Ingresa el valor de A: "))
    B = float(input("Ingresa el valor de B: "))
    operacion = int(input("Selecciona la operación (1: Raíz cuadrada de la suma, 2: División, 3: Fórmula): "))

    # Realizar la operación correspondiente
    if operacion == 1:
        resultado = calcular_raiz_cuadrada_suma(A, B)
    elif operacion == 2:
        resultado = calcular_division(A, B)
    elif operacion == 3:
        resultado = calcular_formula(A, B)
    else:
        resultado = "Operación no válida."

    # Mostrar el resultado de la operación
    print("El resultado de la operación es:", resultado)

    # Verificar si se debe apagar la calculadora
    if input("¿Deseas continuar (SAL para salir)? ") == "SAL":
        break


#*Ejercicio Catorce*
##Tenemos la pantalla del móvil bloqueada. Partiendo de un PIN_SECRETO, intentaremos desbloquear 
# la pantalla. Tenemos hasta 3 intentos. Simula el proceso con Python. En caso de acceder, lanza al 
# usuario login correcto. Sino, llamando ala policía.

pin_secreto:str="2005"
intentos_restantes:int=3
while intentos_restantes >0 :
    pin_usuario:str=input("ingrese un PIN: ")
    if pin_usuario == pin_secreto:
        print("login correcto")
        break
    else:
        intentos_restantes -= 1
        if intentos_restantes >0:
            print(f"te quedan {intentos_restantes} intentos restantes")
        else:
            print("has agotado tus intentos.  Llamando a la policia")

#*Ejercicio Quince*
##Crea un algoritmo para la sucesión de Fibonacci. La sucesión de Fibonacci es la siguiente serie:
#
##0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89
#
##Pista: Empezando por 0 y 1, el siguiente número es la suma de los dos números últimos.

a, b = 0, 1
print(a)
contador = 1
n = 10
while contador < n:
    a, b = b, a + b
    print(a)
    contador += 1
[9:06 p.m., 21/5/2024] Wiliam: #*Ejercicio Dieciséis*
##Desarrolla un programa en Python que permita gestionar una lista de tareas pendientes. El programa
# debe cumplir con los siguientes requisitos:
#
##- Debe permitir agregar nuevas tareas a la lista.
##- Debe permitir marcar tareas como completadas, lo que las eliminará de la lista de tareas pendientes.
##- Debe mostrar la lista actual de tareas pendientes.
##- Debe proporcionar un menú interactivo que permita al usuario seleccionar entre las opciones anteriores 
# y salir del programa.
##El menú debe presentar las siguientes opciones:
#
##- Agregar tarea
##- Marcar tarea como completada
##- Mostrar tareas
##- Salir

# Lista de tareas pendientes
tareas = []

# Menú interactivo
while True:
    print("\nMenú de opciones:")
    print("1. Agregar tarea")
    print("2. Marcar tarea como completada")
    print("3. Mostrar tareas")
    print("4. Salir")

    opcion = input("Seleccione una opción: ")

    if opcion == "1":
        tareas.append(input("Ingrese la nueva tarea: "))
        print("Tarea agregada exitosamente.")
    elif opcion == "2":
        if tareas:
            print("Tareas pendientes:")
            for i, tarea in enumerate(tareas):
                print(f"{i + 1}. {tarea}")
            num_tarea = int(input("Ingrese el número de la tarea completada: "))
            if 1 <= num_tarea <= len(tareas):
                tarea_completada = tareas.pop(num_tarea - 1)
                print(f"Tarea '{tarea_completada}' marcada como completada.")
            else:
                print("Número de tarea inválido.")
        else:
            print("No hay tareas pendientes.")
    elif opcion == "3":
        if tareas:
            print("Tareas pendientes:")
            for i, tarea in enumerate(tareas):
                print(f"{i + 1}. {tarea}")
        else:
            print("No hay tareas pendientes.")
    elif opcion == "4":
        print("¡Gracias por utilizar la lista de tareas pendientes!")
        break
    else:
        print("Opción no válida. Inténtelo de nuevo.")

#*Ejercicio Diecisiete*
##Crea un programa en Python que simule el funcionamiento de un cajero automático. El programa debe permitir
# al usuario realizar las siguientes operaciones:
#
##- Verificar el saldo de su cuenta.
##- Depositar dinero en su cuenta.
##- Retirar dinero de su cuenta.
##- Salir del programa.
##El programa debe iniciar con un saldo inicial predeterminado y mostrar un menú con las siguientes opciones:
#
##- Verificar saldo
##- Depositar dinero
##- Retirar dinero
##- Salir

# Saldo inicial del cajero automático
saldo = 1000

# Menú interactivo del cajero automático
while True:
    print("\nMenú de opciones:")
    print("1. Verificar saldo")
    print("2. Depositar dinero")
    print("3. Retirar dinero")
    print("4. Salir")

    opcion = input("Seleccione una opción: ")

    if opcion == "1":
        print(f"Su saldo actual es: ${saldo}")
    elif opcion == "2":
        monto_deposito = float(input("Ingrese la cantidad a depositar: $"))
        saldo += monto_deposito
        print(f"Se han depositado ${monto_deposito}. Saldo actual: ${saldo}")
    elif opcion == "3":
        monto_retiro = float(input("Ingrese la cantidad a retirar: $"))
        if monto_retiro <= saldo:
            saldo -= monto_retiro
            print(f"Ha retirado ${monto_retiro}. Saldo actual: ${saldo}")
        else:
            print("Saldo insuficiente.")
    elif opcion == "4":
        print("¡Gracias por utilizar el cajero automático!")
        break
    else:
        print("Opción no válida. Inténtelo de nuevo.")

#*Ejercicio Dieciocho*
##Escriba un programa que solicite una contraseña (el texto de la contraseña no es importante) y la vuelva a 
# solicitar hasta que las dos contraseñas coincidan.

# Solicitar y validar la contraseña
while True:
    contraseña1 = input("Ingrese la contraseña: ")
    contraseña2 = input("Confirme la contraseña: ")

    if contraseña1 == contraseña2:
        print("Contraseña confirmada. ¡Contraseñas coinciden!")
        break
    else:
        print("Las contraseñas no coinciden. Inténtelo de nuevo.")