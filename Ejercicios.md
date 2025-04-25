# 1. Ingreso de datos por consola

1. Solicita el nombre y edad del usuario, luego imprime un saludo personalizado que incluya ambos datos.
   
   ```python
   import time
   # PUNTO 1 ------------

   # Parte 1: Saludo con nombre y edad
   print ("¡Hola, queremos saber más de ti!\nCuéntanos....¿Cómo te llamas?")
   nombre = input()

   while True:
    try:
        edad = int(input("\n¿Cuántos años tienes? "))
        break  # Si llegamos aquí, la entrada fue válida, salimos del bucle
    except ValueError:
        print("¡Oops! Debes ingresar un número entero.")

   print(f"\n¡Hey {nombre}! Es un gusto conocerte. Veo que tienes {edad} años, ¡genial!")
   time.sleep(2)
   2. Pide al usuario que ingrese su comida favorita y su color favorito, luego imprime una frase con ambos.
   ```

2. Pide al usuario que ingrese su comida favorita y su color favorito, luego imprime una frase con ambos.

   ```python
    Parte 2: Comida y color favoritos

   print ("\n¿Cuál es tu comida favorita?")
   comida = input()

   print ("\n¿Cuál es tu color favorito?")
   color = input()

   print(f"\nSúper {nombre}, ya tienes claro que el/la {comida} es insuperable. Y ese gusto por el color {color} nos dice mucho de tu estilo.\nGracias por compartirnos un poco sobre ti, cuídate 👋.")
   time.sleep(7)
   ```

3. Solicita un número y muestra su doble y su triple.

   ```python
   # Parte 3: Su doble y su triple

   print (f"\n¡Hola!\nIngresa un número para saber su doble y su triple 🤓:")
   numero = float(input())

   doble = numero*2
   triple = numero*3

   print (f"\nEl doble de {numero} es 👉 {doble:,.2f}")
   print (f"\nEl triple de {numero} es 👉 {triple:,.2f}")
   print (f"\nGracias por tu consulta 🙌")
   ```


# 2. Tipos de datos en Python

1. Declara una variable de cada tipo básico: entero, flotante, cadena y booleano.

   ```python
   import time
   # PUNTO 2 ------------

   # Parte 1: Declarar una variable de cada tipo básico

   # Entero
   while True:
    try:
        entero = int(input("\nPor favor digita un número entero 🤓:"))
        break  # Si llegamos aquí, la entrada fue válida, salimos del bucle
    except ValueError:
        print("¡Oops! No coincide con lo que te pedimos 🫢... Intentemos nuevamente.")
        time.sleep(2)

   print ("\n¡Perfecto! Continuemos...")

   # Flotante
   time.sleep(1)
   while True:
    entrada = input("\nPor favor digita un número decimal 🤓: ")
    try:
        if '.' in entrada:
            flotante = float(entrada)
            break
        else:
            raise ValueError
    except ValueError:
        print("¡Oops! No coincide con lo que te pedimos 🫢... Intentemos nuevamente.")
        time.sleep(2)

   print ("\n¡Perfecto! Continuemos...")

   # Cadena
   time.sleep(1)
   print ("\nPor favor ingresa una cadena de carácteres de tu preferencia 🙂:")
   cadena = str(input())
   time.sleep(1)

   print ("\n¡Perfecto! Continuemos...")
   time.sleep(1)

   # Booleanos
   respuesta = input("\nY por último... ¿Eres coder de Riwi (si/no)? 🤔").strip().lower()
   entrar = respuesta == "si"
   if not entrar:
    print ("\nLo sentimos, no tienes acceso a la plataforma.")
   else:
    print ("\nBienvenid@, revisa las actividades pendientes en Moodle.")
    time.sleep(4)
   ```

2. Convierte una cadena con valor numérico a entero y realiza una suma con otro número.

   ```python
   # Parte 2: Convertir cadena con valor numérico a entero y hacer operación

   numeroTexto = "5"
   print (f"\nEste valor es una cadena: '{numeroTexto}'")
   time.sleep(3)

   numero = int(numeroTexto)
   print (f"Lo convertimos a un número entero: {numero}")
   time.sleep(3)

   suma = 10
   resultado = numero + suma
   print (f"Si sumamos {numero} + {suma}, obtenemos como resultado {resultado}")
   ```

3. Convierte una entrada de texto a número flotante, multiplícala por 2 y muestra el resultado.

   ```python
   # Parte 3: Convertir entrada de texto a flotante y hacer operación

   time.sleep (4)
   while True:
    entradaTexto = input("\nIngresa un número decimal para convertirlo: ").strip()
    
    try:
        dec = float(entradaTexto)
        break
    except ValueError:
        print("Eso no parece un número decimal válido 😬. Intenta de nuevo.")
        time.sleep(2)

   print(f"\nConvertimos '{entradaTexto}' a un número decimal...")
   time.sleep(1.5)
   print(f"Obtenemos: {dec}")

   mult = 2
   restd = dec * mult
   print(f"\nSi multiplicamos {dec} x {mult}, obtenemos como resultado 🤓: {restd:,.2f} ")
   time.sleep(4)
   ```

4. Escribe una función que reciba un string y devuelva `True` si puede convertirse a número y `False` si no.

   ```python
    Parte 4: ¿Se puede convertir a número?

   def convertir(texto):
    try:
        float(texto)
        return True
    except ValueError:
        return False

   print("\nY por último, comprobemos si un texto puede convertir a un número")

   entradaStr = input("Escribe algo y lo analizamos: ").strip()

   time.sleep(1)

   if convertir(entradaStr):
    print(f"\n✅ Sí, '{entradaStr}' se puede convertir a número.")
   else:
    print(f"\n❌ No, '{entradaStr}' NO se puede convertir a número.")
   ```


#  3. Operadores en Python

1. Calcula el área de un rectángulo a partir de base y altura ingresadas por el usuario.

   ```python
   import time
   # PUNTO 3 ------------

   # Parte 1: Calcular área de un rectángulo

   print ("¡Hola coder! 👋 Hallaremos el área de un rectángulo así que:")
   base = float(input("\nIngresa la base del rectángulo: "))
   altura = float(input("\nIngresa la altura del rectángulo: "))

   area = base * altura
   print(f"\nEl área del rectángulo es 👉 {area}")

   time.sleep (3)
   ```

2. Dado un precio y un porcentaje de descuento, muestra el valor final a pagar.
   
   ```python
   # Parte 2: Descuento de producto
   print ("¡Hola coder! 👋 Miraremos el precio final de un producto con descuento:")

   precio = float(input("\nIngresa el precio del producto: $"))

   entrada_descuento = input("¿De cuánto es el descuento?: ")
   entrada_descuento = entrada_descuento.replace("%", "").strip()

   descuento = float(entrada_descuento)

   monto_descuento = precio * (descuento / 100)
   precio_final = precio - monto_descuento

   print(f"\nCon un descuento del {descuento}% el precio final de tu producto es: ${precio_final:,.2f}")
   time.sleep (2)
   ```

3. Calcula el residuo de dividir dos números dados por el usuario.

   ```python
   # Parte 3: Residuo de una división

   print ("\n¡Hola coder! 👋 Haremos una división, entonces...")
   time.sleep(1)

   num1 = int(input("\nIngresa el primer número: "))
   num2 = int(input("\nIngresa el segundo número: "))

   res = num1 / num2
   print(f"\nEl resultado/residuo de dividir {num1} entre {num2} es 👉 {res}")
   time.sleep(3)
   ```

4. Escribe una fórmula que use al menos tres operadores diferentes y muestre el resultado.

   ```python
   # Parte 4: Fórmula con al menos 3 operadores

   print ("\n¡Hola coder! 👋 Haremos una operación con una fórmula (a + b) * c / 2 es")
   time.sleep(1)

   a = float(input("\nIngresa un número para 'a': ")
   b = float(input("Ingresa otro número para 'b': "))
   c = float(input("E ingresa un número para 'c': "))

   resultado = (a + b) * c / 2
   print(f"\nEl resultado de nuestra fórmula (a + b) * c / 2 es 👉 {resultado}")
   ```

# 4. Operadores relacionales

1. Pide dos números e indica cuál es mayor o si son iguales.

   ```python
   import time
   # PUNTO 4 ------------

   # Parte 1: ¿Cuál número es mayor o son iguales?

   print ("¡Hola coder! 👋 Miraremos si un número es mayor, menor o igual a otro, así que...:")

   num1 = float(input("\nIngresa el primer número: "))
   num2 = float(input("Ingresa el segundo número: "))

   if num1 > num2:
    print(f"\n{num1} es mayor que {num2}")
   elif num1 < num2:
    print(f"\n{num2} es menor que {num1}")
   else:
    print("\nAmbos números son iguales")
   time.sleep(2)
   ```
   
2. Solicita una edad y determina si la persona es menor de edad (menor a 18).

   ```python
   # Parte 2: ¿Es menor de edad?

   print ("\n¡Hola coder! 👋 Miraremos miraremos si puedes ingresar al club")
   edad = int(input("\nIngresa tu edad: "))

   if edad < 18:
    print("\nEres menor de edad, no puedes entrar.")
   else:
    print("\nEres mayor de edad, si puedes entrar.")
   time.sleep(2)
   ```
   
3. Escribe un programa que compare dos cadenas de texto e indique si son iguales o distintas.

   ```python
   # Parte 3: ¿Dos cadenas de texto son inguales?

   print ("\n¡Hola coder! 👋 Miraremos si dos cadenas de textos son iguales, así que...")
   time.sleep(1)

   texto1 = input("\nEscribe una palabra o frase: ").strip()
   texto2 = input("\nEscribe otra palabra o frase: ").strip()

   if texto1 == texto2:
    print(f"\nLas cadenas son iguales.")
   else:
    print("f\nLas cadenas son diferentes.")
   ```

# 5. Operadores lógicos 

1. Pide al usuario su edad y si tiene licencia de conducción. Solo si ambas condiciones se cumplen, imprime que puede conducir.

   ```python
   import time
   # PUNTO 5 ------------

   # Punto 1: ¿Puedes conducir? (edad + licencia)

   print ("\n¡Hola coder! 👋 Veremos si puedes conducir, así que...")
   time.sleep(1)

   edad = int(input("\n¿Qué edad tienes?: "))
   licencia = input("¿Tenés licencia para conducir? (si/no): ").strip().lower()

   if edad >= 18 and licencia == "si":
    print("\n¡Perfecto, puedes conducir!")
   else:
    print("\nOops, no cumples con los requisitos para conducir.")
   ```

2. Solicita si una persona tiene experiencia laboral y título universitario. Usa operadores lógicos para decidir si puede aplicar a una oferta de trabajo.

   ```python
   # Punto 2: ¿Puede aplicar a la oferta laboral?

   print ("\n¡Hola coder! 👋 Veremos si puedes aplicar a una oferta laboral, así que...")
   time.sleep(1)

   experiencia = input("\n¿Tienes experiencia laboral? (si/no): ").strip().lower()
   titulo = input("¿Tienes algún título universitario? (sí/no): ").strip().lower()

   if experiencia == "si" and titulo == "si":
    print("\n¿¡Perfecto, puedes aplicar a la oferta laboral! 🤗")
   else:
    print("\n¿Lo sentimos, no cumples con los requisitos 😣")
   time.sleep(2)
   ```

3. Dado un número, determina si está en el rango de 10 a 50 (inclusive).

   ```python
   # Punto 3: ¿Está en el rango de 10 a 50?

   print ("\n¡Hola coder! 👋 Veremos si el número que ingreses está en el rango de 10 a 50, así que...")
   time.sleep(1)

   numero = float(input("\nIngresa un número: "))

   if 10 <= numero <= 50:
    print("\n✅ El número está en el rango de 10 a 50.")
   else:
    print("\n❌ El número está fuera del rango.")
   ```
